# python_flask_uwsgi_nginx_multiple_subdomains
2 subdomains deployed in microservices fashion

->1 container runs nginx . The 2 other containers have flask app + uwsgi in each.
->edit /etc/hosts for flask1.localhost and flask2.localhos pointing to 127.0.0.1 .
->clone this repo , then do a 'docker-compose build' followed by 'docker-compose up -d' . This will get all 3 containers up and running.
-> now visit 'flask1.localhost' and 'flask2.localhost' in the browser.

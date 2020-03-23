DOMAIN=ssl3.running-blue.com
EMAIL=karl.yogi.xu@gmail.com
BASE_COMMAND=docker run -it --rm --name letsencrypt \
		-v "/etc/letsencrypt:/etc/letsencrypt" \
		-v "/var/lib/letsencrypt:/var/lib/letsencrypt" \
		-v "$(CURDIR)/src:/code" \
		quay.io/letsencrypt/letsencrypt:latest \

SUB_COMMAND=delete
CERTNAME=ssl3.running-blue.com

compose:
	docker-compose up --build -d

certbot-create:
	$(BASE_COMMAND) certonly --webroot -w /code -d $(DOMAIN) -m $(EMAIL) --agree-tos

certbot-ls:
	$(BASE_COMMAND) certificates

certbot-delete:
	$(BASE_COMMAND) delete --cert-name $(CERTNAME)

certbot-help:
	$(BASE_COMMAND) --help $(SUB_COMMAND)

certbot-renew:
	$(BASE_COMMAND) renew --cert-name $(CERTNAME) --force-renewal

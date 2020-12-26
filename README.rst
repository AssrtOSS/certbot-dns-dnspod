DNSPOD DNS Authenticator plugin for Certbot
-------------------------------------------
.. image:: https://travis-ci.com/AssrtOSS/certbot-dns-dnspod.svg?branch=master
    :target: https://travis-ci.com/AssrtOSS/certbot-dns-dnspod
.. image:: https://coveralls.io/repos/github/AssrtOSS/certbot-dns-dnspod/badge.svg?branch=master
    :target: https://coveralls.io/github/AssrtOSS/certbot-dns-dnspod?branch=master


Use the certbot client to generate a certificate using dnspod.

Install certbot and plugin
==========================

.. code-block:: bash

    pip install certbot-dns-dnspod


Create a credentials file
=========================

.. code-block:: ini

    certbot_dns_dnspod:dns_dnspod_email = "DNSPOD-EMAIL"
    certbot_dns_dnspod:dns_dnspod_api_id = "DNSPOD-API-TOKEN-ID"
    certbot_dns_dnspod:dns_dnspod_api_token = "DNSPOD-API-TOKEN"


Generate a certificate
======================

.. code-block:: bash

    certbot certonly -a certbot-dns-dnspod:dns-dnspod \
        [--certbot-dns-dnspod:dns-dnspod-credentials PATH-TO-CREDENTIAL-FILE]
        -d REPLACE-WITH-YOUR-DOMAIN

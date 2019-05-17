This repository is archived

Using docker-compose, many of moov's published services can be brought down to
run, without much setup:

- [PayGate](https://github.com/moov-io/paygate), ACH payment gateway
- [ach](https://github.com/moov-io/ach) - Base ACH library
- [customers](https://github.com/moov-io/customers) - Customer accounts/ledger
- [Fed](https://github.com/moov-io/fed) - Federal Bank lookup
- [watchman](https://github.com/moov-io/watchman) - AML/CTF/KYC/OFAC Search of global watchlist, sanctions, and politically exposed person (PEP)

1. Install docker-compose
2. `$ git clone https://github.com/tgunnoe/paygate-services`
3. `$ docker-compose up -d`

conf/config.yaml would normally be secret, but it's mostly copied from Moov's
example config anyways.  Git-crypt protects some `htpasswd` I was using for the
demo, though.

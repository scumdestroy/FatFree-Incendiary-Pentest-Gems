#TRANSACTION RISK API (first 2 required)
transaction_id
transaction_time
primary.name
	.firstname
	.lastname
	.businessname
secondary.name (etc.)
primary.address.street_line_1
primary.address.city
		.postal_code (state_code, country_code)
primary.phone
primary.email_address
ip_address

# Account Signup (first 5 required)
account_signup_time
account_signup_id
email_address
ip_address
phone 
name, firstname, lastname
address.city, address.state_code address.country_code

# Reverse Phone API - receive all types of data just from phonenumber#
phone
# reverse email API
email_address	

# reverse address API
street_line_1
street_line_2
city
postal_code
state_code
country_code

##EXAMPLES
```
https://api.ekata.com/1.0/transaction_risk?api_key=XXXXX&primary.name=Waidong+L+Syrws&primary.phone=2069735100&primary.email_address=waidong%40gmail.com&primary.address.street_line_1=100+Syrws+St&primary.address.street_line_2=Ste+1&primary.address.city=Lynden&primary.address.state_code=WA&primary.address.postal_code=98264&primary.address.country_code=US&ip_address=54.190.251.42&secondary.firstname=Waanataa&secondary.lastname=Labarrete&secondary.address.line_1=1+Syrws+St%2C+Lynden%2C+WA&secondary.address.country_code=US
https://api.ekata.com/1.0/account_opening?api_key=XXXXX&account_signup_id=95285489a80b059a7f0be7147ba211f1&account_signup_time=2020-12-31+13%3A45&name=Lukas+Schmidt&phone=7785732875&email_address=lukas%40schmidt.com&address.street_line_1=2+Roman+Way&address.street_line_2=&address.city=London&address.postal_code=N7+8XG&address.state_code=&address.country_code=GB&ip_address=54.190.251.42
https://api.ekata.com/3.1/phone?api_key=XXXXX&phone=2069735100
https://api.ekata.com/4.1/email?api_key=XXXXX&email_address=waidong%40gmail.com
https://api.ekata.com/3.0/location?api_key=XXXXX&street_line_1=100+Syrws+St&street_line_2=Ste+1&city=Lynden&state_code=WA&postal_code=98264&country_code=US
https://api.ekata.com/4.0/location_intel?api_key=XXXXX&street_line_1=Winsstra%C3%9Fe+68&street_line_2=&city=Berlin&state_code=&postal_code=10405&country_code=DE
```

#API KEYS: 
id check: 0510c76a14834971848b3dfd6b7f0aa2
phone intel: e9ed183daa0040b5b8652df12feffb8b
address risk: fe15dee010234218a77edc4730152537


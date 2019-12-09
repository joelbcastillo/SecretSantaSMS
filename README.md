# Secret Santa SMS
Using [Twilio API](https://www.twilio.com/), send each Santa their Santee's name directly to their phone. Supports no-match 1-way and 2-way.

![SMS](https://i.imgur.com/0GZKWz5.jpg)

### No Match 1-Way
  ['Chris', 'Johnny']
  
  Chris, the Santa, will not be given Johnny as their Santee. However, Johnny as a Santa can get Chris as a Santee. The purpose of this is to not get a repeat of a previous year(s) match.
  
### No Match 2-Way
  ['Jordan', 'Johnny']
  
  Jordan and Johnny are brothers, will not be given each other at all.

# Configuration

SMS Python QuickStart https://www.twilio.com/docs/sms/quickstart/python

Register on Twilio, add funds to the wallet. Purchase a phone number, create Programmable SMS project. Account SID and Auth Token are required for this to function along with the phone number.

Copy `config.yml.example` to `config.yml`  and update it with twilio account_sid, auth token, and phone numberparticipants, 1-way and 2-way blocks. Line `114` in `santa.py` has the SMS message, feel free to customize as you find fit.

Put `[]` in `config.yml` >> `DONT-REPEAT` and `DONT-PAIR` if you do not want to have any blocks.

# Running

#### Depending on how Python is configured...
`python3 santa.py --send` OR `python santa.py --send` to actually send out the SMS

`python3 santa.py` OR `python santa.py` to test it locally and NOT send out the SMS


# Credits

This code was derived from https://github.com/iHydra/SecretSantaSMS and modified to load API credentials from a config file.

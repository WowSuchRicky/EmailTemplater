# Script written for MadHacks 2015 sponsor email generation.

######Usage:
`python main.py`


Invariants:
* Must have python 2.7 (might work with 3? no idea)

* Must have "sponsors.csv" file in the data/ folder. Our script currently checks column 0, 1 and 3 for the fields Company Name, Contact Person Name, and Contact Email respectively. I really want to make this more robust eventually, but it isn't right now. 

* Must have "template.txt" in the root directory. This is simply the email that you want to send to your sponsors. The script will replace "[RECRUITER NAME]" with the contact name, and [COMPANY NAME] with the company's name. Also, it'll send the email to the email address stored as well.

* Must have "keys.py" file with two functions: getlogin() and getkey() that return the username and password for a gmail account. Otherwise, you must replace the lines that call these two functions with a hard-coded user and pass, although I don't recommend this.

Right now, the script requires manual confirmation (y/n) before sending each email. This is for rate-limiting as well as making sure we aren't sending shitty emails. This can very easily be removed - if you can't figure it out, ask me (but you probably shouldn't be using the script at that point until you understand it). Also, if any of the three fields are missing/invalid (name, contact name, email), right now we're just skipping that sponsor. 

Please see the Issues for all currently in progress features as well as bugs. This script is a constant WIP, and thus I have no guarantee or warranty from its use. Please be responsible, and don't come to me saying you accidentally emailed 5000 sponsors the wrong thing. 


Let me know if there are any issues, or fork+fix. Thanks!

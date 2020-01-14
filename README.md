# frc-mentor-tools
Tools and scripts to help FRC mentors

So far, there's just one script here:

## bin/html2contacts

This little tool converts the Firstinspires.org mentor dashboard's
page of student contacts into a CSV file that can be imported into a
spreadsheet.  I use it frequently in the runup to kickoff and events
to make sure that all of our students have had their parents accept
the Consent & Release form.

### Installation

This script is written in perl, and is known to work on linux and on windows
uning cygwin.

* Clone this repository, or download the script bin/html2contacts.
* install the perl package JSON from any of these sources:
**  for Centos and Fedora linux: sudo yum install perl-JSON
**  for cygwin, I think the package is also called perl-JSON
**  or install directly from CPAN:  https://metacpan.org/release/JSON

### Usage

* log into your FIRST dashboard as a lead mentor
* select the desired team, if you have more than one
* Under "Team Contacts/Roster" pull down the "Contact Options" menu
* Select "manage Contacts".  you should be familiar with this page already.
* Download HTML source to this page.  
** Using firefox, right click and select "Save Page As"
** give the file a better name, such as "contacts-13-jan-2020.html"
** choose "web page, HTML only", and select SAVE.

* then, find the saved file using the command line.
* run html2contacts on the html:

	html2contacts contacts-13-jan-2020.html > tims-13-jan-2020.csv

* look at the CSV and see if it looks reasonable.
* then load the CSV into a spreadsheet such as google docs or LibreOffice Calc.
* Get your team organized a little more easily.



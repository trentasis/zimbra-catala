README
======



- How to download this language package?
+ You can download it in two ways:
	1. Direct download. Using this URL ( https://github.com/btactic/zimbra-catala/zipball/master )  and extracting it into an empty folder.
	2. Using GIT. To clone this repository use:

		git clone https://github.com/btactic/zimbra-catala.git zimbra-catala

- How to deploy the translation package ?
+ On a new terminal type "sudo ./deploy.sh"

When you execute deploy.sh it makes a new directory called backup, where it backups the old Catalan translations.


This Catalan language pack contains:

AjxKeys.properties
AjxMsg.properties
I18nMsg.properties
CHANGELOG
deploy.sh
l18nMsg.properties
README
ZabMsg.properties
ZaMsg.properties
ZbMsg.properties
ZhMsg.properties
ZmKeys.properties
ZmMsg.properties
ZMsg.properties
ZmSMS.properties



Both administration and user pages are translated.

This translation has been possible thanks to the support of the Department of Culture of the Generalitat of Catalonia.

Aquesta traducció ha sigut possible gràcies al suport del Departament de Cultura de la Generalitat de Catalunya.

![alt text](https://github.com/btactic/zimbra-catala/raw/master/images/Generalitat_de_Catalunya.jpg)
-----------------------------------------------------------------------------

OLD README
==========
- In order to deploy this translation, you first need to convert it from UTF-8 to ASCII, which is the encoding zimbra uses. You may do it with the following command (change according to new versions of the jdk)
/opt/zimbra/java/bin/native2ascii -encoding UTF-8 ZmMsg.properties ZmMsg_ca.properties
- Note that if you want to use an ISO-8859-1 encoded file, you have to change the command accordingly

- Then, we make a backup of the zimbra language file, if there is any
cp /opt/zimbra/jetty/webapps/zimbra/WEB-INF/classes/messages/ZmMsg_ca.properties ./ZmMsg_ca.properties.old
- And last, we copy our file in place
cp ZmMsg_ca.properties /opt/zimbra/jetty/webapps/zimbra/WEB-INF/classes/messages/ZmMsg_ca.properties

- Remember, in order to update the language strings, you have to
	- zmcontrol stop
	- zmcontrol start
	- Clean your browser's cache

Good luck!

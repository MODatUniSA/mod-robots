# NAO robot

Documentation for the NAO robot at MOD.

## Removing software

* Login to the [Cloud section](https://cloud.aldebaran-robotics.com/application/) of SoftbankRobotics.
* Select: My Apps
* Select: Uninstall All Apps
* Login to NAO by tapping on its chest button to get its IP address.
* Click the `Updates` button, and update/remove apps.

## Updating the system image

* Login to the [Community section](https://community.ald.softbankrobotics.com) of SoftbankRobotics.
* Select: [Resources > Software > NAO](https://community.ald.softbankrobotics.com/en/resources/software/language/en-gb/robot/nao-2).
* Scroll to “1 - Upgrading your NAO View archives”
* Download the NAOQI OS `2.x.x atom system image`
* Open the `Choregraphe` app on your computer, and connect to NAO.
* From the menu select: Connection > Advanced > Update robot system.
* Enter the login details (username is `nao`).
* After the image has uploaded, hold down NAO’s chest button to turn it off, and then turn it on by holding the chest button for ~5 seconds, releasing it when the blue ring lights up.
* NAO will take ~10 minutes to update, and restart automatically.

## Re-installing the basics

* Login to the [Cloud section](https://cloud.aldebaran-robotics.com/application/) of SoftbankRobotics.
* Select: Applications
* Install: Dialog greetings, The dialog, Dialog lexicon.

## Factory reset

* Login to the [Community section](https://community.ald.softbankrobotics.com) of SoftbankRobotics.
* Select: [Resources > Software > NAO](https://community.ald.softbankrobotics.com/en/resources/software/language/en-gb/robot/nao-2).
* Scroll to “1 - Upgrading your NAO View archives”
* Download the NAOQI OS `2.x.x atom system image`
* Flash the image to a USB stick using the [image flasher app](https://community.ald.softbankrobotics.com/en/resources/software/8-troubleshooting).
* Plug the USB into the back of NAO’s head.
* Hold NAO’s chest button in for ~5 seconds until the blue ring lights up.
* The blue ring should flash quickly, signifying the reset has started.

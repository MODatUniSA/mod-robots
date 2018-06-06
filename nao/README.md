# NAO robot

Documentation for the NAO robots at MOD. To get started, follow the official [NAO documentation online](http://doc.aldebaran.com/1-14/index.html).

## MOD. programs

To run any of these programs, install [Choreographe](http://doc.aldebaran.com/1-14/software/installing.html). Then File > Open project > Select the `.pml` file in the project folders below.

Then to connect to the NAO:

* Make sure you’re both on the same WiFi network (or have the NAO plugged into your computer via ethernet into the back of NAO’s head).
* Tap the green ‘Connect to’ icon in Choreographe.
* Select your NAO, and tap ‘Select’.
* Once connected, you can press the green ‘Upload to the robot and play’ button that looks like a Play symbol.
* To see what NAO is hearing, tap: View > Dialog. This will show what NAO is hearing, and give you a chance to also type in words that you want NAO to respond to so that you can test without having to talk to NAO.

We’ve written some naive implementations of programs for the NAO for various marketing and engagement events. So while none of these programs are robust, they may be useful as starting points for future programming.

* [conversation_marketing](conversation_marketing) - a conversation with the UniSA marketing department.
* [conversation_with_the_vc](conversation_with_the_vc) - a conversation with the UniSA Vice Chancellor.
* [kaurna-hello-goodbye](kaurna-hello-goodbye) - a prototype to see if the NAO can speak Kaurna, responding to hello in English with the Kaurna hello. And similar for goodbye.
* [Lost_NAO](Lost_NAO) - a prototype for a future exhibition at MOD.
* [move-plaque](move-plaque) - a program run on two NAO robots to carry two parts of a plaque together on stage for the UniSA CRI building launch.
* [handout-maps](handout-maps) - a program to get NAO to handout maps for MOD. Tap her head for her to grip a map, say ‘thanks’ or ‘thank you’ and she’ll let it go.

## Troubleshooting

If your NAO can’t connect to WiFi for some reason, follow the instructions in the [Connection Management](http://doc.aldebaran.com/1-14/software/choregraphe/connection_widget.html) documentation.

We’ve found using a battery powered 4G WiFi router useful, as you can connect to the router and easily see the IP address that the NAO has been assigned.

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

[Instructions](http://doc.aldebaran.com/2-1/software/naoflasher/naoflasher.html#naoflasher-upgrade) from the Aldebaran website.

* Login to the [Community section](https://community.ald.softbankrobotics.com) of SoftbankRobotics.
* Select: [Resources > Software > NAO](https://community.ald.softbankrobotics.com/en/resources/software/language/en-gb/robot/nao-2).
* Scroll to “1 - Upgrading your NAO View archives”
* Download the NAOQI OS `2.x.x atom system image`
* Flash the image to a USB stick using the [image flasher app](https://community.ald.softbankrobotics.com/en/resources/software/8-troubleshooting).
* Plug the USB into the back of NAO’s head.
* Hold NAO’s chest button in for ~5 seconds until the blue ring lights up.
* The blue ring should flash quickly, signifying the reset has started.

## Writing a system image to a USB on MacOS

Open Terminal, insert the USB and enter these commands to write the image. To see progress tap `control + t`.

```Bash
$ diskutil list
$ diskutil unmountDisk /dev/disk<disk# from diskutil>
$ sudo dd bs=1m if=image.opn of=/dev/rdisk<disk# from diskutil>
```

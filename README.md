# PixieBoardIoTCoreExample
This example shows how you can send your GPS Location to the IoT Core Service on Google. This example was done to show case PixieBoards capabilities.

## How to clone and install
```sh
$ sudo git clone --recurse-submodules https://github.com/pixierepo/PixieBoardIoTCoreExample.git
``` 
After you have downloaded the repo you should install the python dependencies with:
```sh
$ sudo pip install -r requirements.txt
```
## Requirements
Before you start you should already have the PixieBoards modem enabled. You can do that by typing:
```sh
$ sudo enablePixieModem
``` 
Wait around 30 seconds and then check with this command:
```sh
$ mmcli -L
output: Found 1 modems:
	/org/freedesktop/ModemManager1/Modem/0 [QUALCOMM INCORPORATED] QUECTEL Mobile Broadband Module
``` 
If so you can start using the PixieBoardGPSLocation class.

If you are not familiar with the information above I recommend you take a look at our [Medium](https://medium.com/pixieboard) page that has a [Getting Started Guide](https://medium.com/pixieboard/getting-started-with-pixieboard-7e977ee6d276) and a [Enable PixieBoards Modem](https://medium.com/pixieboard/enabling-the-cellular-modem-on-the-pixieboard-3644ca03369) guide.

You should have base-devel, python, pip and socat installed:
```sh
$ sudo pacman -S base-devel python, python-pip socat
``` 

## How to use the MQTTExample
Assuming you have already generated the registry on the Google Cloud Console and the private and public keys here is an example on how to execute the file:
```sh
$ sudo python MQTTExample.py --registry_id=<registry_id> --cloud_region=<cloud-region> --project_id=<project_id> --device_id=<device_id> --algorithm=RS256 --private_key_file=<private_key.pem> --num_messages 10
``` 
If you are not familiar with the above take a look at this guide that show to set up the cloud enviornment: [PixieBoard + Google's IoT Core](https://medium.com/pixieboard/pixieboard-googles-iot-core-42a3f837e571)


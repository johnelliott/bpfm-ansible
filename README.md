# BPFM installation

This is for setting up a raspberry pi to act as a hands-free device to support bluetooth audio input for use on a streaming server.

Path of audio:

mobile phone -> bluetooth A2DP -> pi -> node.js -> client browser

Hardware plan:

Raspberry Pi with bluetooth and wifi, set up as an access point serving a page to all web requests.

Client plan:

The page will use browser-native apis to deliver the audio stream.
## Setup thus far

* we did a key pair, we called the Raspberry pi user pi
* we set up an ssh config called 'pi'
* we made sure the laptop knew about the pi hostname
* we installed the ansible script

## Deploying
edit the `inventory` file with the ssh Host to deploy install to
run `$ ansible-playbook make-nohands.yml -i inventory --ask-sudo-pass`


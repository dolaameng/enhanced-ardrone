# How to play
1. Register a Clarifai API and create a project, for computer vision capability
	1. Put your clientId and clientSecret in the file `public/clarifai_key.js` as the below
	```javascript
	var CLIENT_ID = 'your ID here';
	var CLIENT_SECRET = 'your secret here';
	```
2. Connect drone to internet using ardrone-wpa2
	1. `cd ardrone-wpa2` and connect to drone network, i.e., "ardone"
	2. run `script/install`
	3. run `script/connect` <essid> -p <password> -a <address>`
		where <essid> is your home wifi name, 
		<password> is the WPA2 password, 
		and <address> is the ip located to drone in your home wifi, e.g., "192.168.0.211"
	4. get connected to your home wifi
3. Start the server
	1. get back to the root folder
	2. create env variable with the IP you have assigned to the drone, e.g., `export DRONE_IP=192.168.0.211`
	3. start server by `node server.js`
	4. after it starts, visit the page at http://localhost:3001/

# Implementation
I was piping up different APIs. Credits are to the original writers.
- [ardrone-wpa2](https://github.com/daraosn/ardrone-wpa2) to connect drone to the internet
- [google speech recognition API](https://github.com/GoogleChrome/webplatform-samples/tree/master/webspeechdemo) for speech control
- [drone-browser](https://github.com/functino/drone-browser) for the frontend and drone communication
- [clarifai api](https://github.com/Clarifai/clarifai-javascript) for computer vision - it is a little slow in my experiment, I haven't fingered out if it is because I have a free account.

# youtube video
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=X9nEhS5XSRA)
# Project Title

## Hue Home Lights App 

Here is a project I started so that I could learn React and the Hue bridge api.  

This app will query the Hue bridge for all groups then filter out the group type of 'room' then display those rooms in a room component.  Hue-home-lights app is currently using the Gestalt component library from Pinterest for most of the atom controls and the rc-slider slide control to change the brightness.  

<img src="./src/images/three-rooms.png"
     alt="Markdown Monster icon"
     style="padding: 25px; width: 394px; height:280px" />


## Getting Started

The instructions below will get you a copy of the project running on your local machine for development. 

**Cloning and running the project**
```zsh
git clone https://github.com/vherrin/hue-home-lights.git
yarn 
yarn start
``` 

### ENV file
This project expects an environment file, .env file, in the root of the project.  This file currently only has one line which contains the bridge IP and the unique user name that you generated in the following steps below.  Please note this file is only read in when starting the app so if you created it while the app is already running then it will not work.  Just restart the app to read it in. 

.env (file in the root of project)
```
REACT_APP_SERVICE_URL=http://YOUR_HUE_BRIDGE_IP/YOUR_UNIQUE_USER_NAME_FROM_BRIDGE/
```

### Prerequisites

First you need to find the hue bridge ip so that you can create a unique user name that the bridge will accept.  This can be done several ways. Below is a flow in the hue app version to get the ip.  There are also some links to the other ways I have discovered below. 

Open the hue app on your mobile device.  The pictures show the iPhone version.
  - Go to settings tab
  - Select Hue Bridges
  - Select the information icon and get the ip 
  - Select Network Settings to edit the information such as making the hue bridge have a static IP

<p float="left">
  <img src="./src/images/img-5059.png" width=24% />
  <img src="./src/images/img-5060.png" width=24% />
  <img src="./src/images/img-5062.png" width=24% />
  <img src="./src/images/img-5063.png" width=24% />
</p>

### Other ways to discover

This link will discover your hue bridge and display the IP
https://discovery.meethue.com/

This site shows several ways to discover
https://developers.meethue.com/develop/application-design-guidance/hue-bridge-discovery/


### Getting to know the Hue bridge API 

Once you get the IP then you need to generate a user name so that you can use the Hue bridge API.  This is simple enough and you can find the instructions in the link below.  Basically it requires you to hit a specific call to the bridge when the bridge button has been pushed to generate a user name.  There is a simple test web app built into every Hue bridge which lets you directly input commands and send them to the lights.  I personally used insomnia the free version to create and save off the api calls from learning and testing.

Here is a quick picture of the built-in bridge test app

<img src="https://developers.meethue.com/wp-content/uploads/2018/02/response.png" style="margin: 8px; width: 400px; height:440px">


[Getting started with Hue development](https://developers.meethue.com/develop/get-started-2/)

[Insomnia API Client](https://insomnia.rest/)

### Future Work Planned

* add scenes so that each room can drill down and set a defined scene
* add color loop to a specific light and not just a room
* visual updates and clean-up

## Authors

* *Vince Herrin* - *Initial work* - [Vince](https://github.com/vherrin)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details



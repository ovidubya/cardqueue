# Overview

This repository will be used to write test automations for Opinionlab Products. Framework used is Webdriver.io. 

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

<img src = "http://webdriver.io/images/webdriverio.png" height = "100">
<br>


<img height = "200" src="https://cdn-images-1.medium.com/max/1600/1*TKt92huSBbSnbRNuAVTx_A.jpeg">


# Installation

### Step 1
Clone the repo in your dev folder
```sh
$ git clone https://github.com/opinionlab/wall-of-awesome.git
```
OR
extract the the zip `olAutomation.zip` in to your dev folder.


### Step 2

Once you have the folder installed, navigate to the root directory, and type

```sh
$ npm install
```
```sh
$ npm run build
```
## That's it. 

# Getting started with Comment Card tests

### Step 1 (one time process)
Once your in the root directory, open the `evars.sh` file and place your browserstack USER and KEY in the file, so it would look something like this:

```sh
export USER=ovadiashalom24 #NOT A REAL USER
export KEY=EsQFGaguwXfaswxHpmJL #NOT A REAL KEY
```

Then run the command in terminal:
```sh
$ . ./evars.sh
```

### Step 2

In your terminal, type
```sh
$ export CC=http://www.extranet.opinionlab.com
```

You can change CC to whatever comment card referer you want to test. 

By default, thank you window screenshots is set to false, to enable thank you card screenshot type

```sh
export TY=true
```
**If TY is set to true, then you will need to spam out the submissions on the portal!**

### Step 3

To screenshot iOS:
```sh
$ npm run ccios
```

To screenshot android:
```sh
$ npm run ccandroid
```

To screenshot windows:
```sh
$ npm run ccwindows
```

To screenshot mac:
```sh
$ npm run ccmac
```

Results of screenshot will be in the 

`Results\cc_results\` folder.


# Getting started with ticket testings


### Step 1

Type:
```sh
$ . ./evars.sh
```

Next,
Export the ticket name and the extranet link for testing:
```sh
export LINK=https://extranet2.opinionlab.com/Testing/ovadia/clientDemo/demo.html
export TICKET=IMP-9999
```

### Step 2

Type 

```sh
$ node ticketHelper.js
```

Answer the questions

### Step 3

To screenshot iOS:
```sh
$ npm run ticketios
```

To screenshot android:
```sh
$ npm run ticketandroid
```

To screenshot windows:
```sh
$ npm run ticketwindows
```

To screenshot mac:
```sh
$ npm run ticketmac
```

To screenshot all devices:
```sh
$ npm run ticketall
```

Results of screenshot will be in the 

`Results\ticket_results\` folder.

# Getting started with writing your own test
To get an idea of how webdriver.io works, let's use it's REPL feature. REPL stands for `Read-Eval-Print-Loop` its a shell interface which allows us to run our tests on our local machines before we start writing our tests on browserstack. 

First, were gonna need two terminals.

In terminal one, type:
```
$ npm run server
```
This will run the selenium stand alone server. If you see it erroing out, than that means the server is either already running on your computer or the drivers are not installed. To install the drivers, type
```
$ npm run build
```


In 2nd terminal, type:
```
$ npm run repl
```

This will prompt a chrome window. You should now be able to type commands in the terminal to automate your browser. For instance, try typing the following line:

`browser.url('https://www.opinionlab.com')`

After running that command, you should be prompted to the opinionlab website.

Now there is a alot of things we can do at this point, for all the posibelites check out the webdriver api here: http://webdriver.io/api.html

Right now, let's click on the tab thats on the website. 
Type `browser.click('#oo_tab')`

A comment should pop up. After it pops up type:

`browser.switchTab(browser.getTabIds()[1])`

This will switch the the browser object to the new pop up window. getTabIds() returns an array of all the windows/tabs availble. 

# Archtiecture 

## TODO 



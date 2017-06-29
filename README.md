### Prerequisites
##### Notes: 
### Installing
#### Mac OS X and Linux
#### Windows
## Running the tests

## Built With
## Authors
* **Udacity** - *Initial work* - [AIND-Recognizer](https://github.com/udacity/AIND-Recognizer)
* **Jonathan Sulivan**

## Acknowledgments
* Hackbright Academy
* Udacity
 
### Additional Information
##### Provided Raw Data

# Artificial Intelligence Engineer Nanodegree
## Intro to Computer Vision
### Project: Mimic Me!
## Overview

In this project, you will learn to track faces in a video and identify facial expressions using Affectiva. As a fun visualization, you will tag each face with an appropriate emoji next to it. You will then turn this into a game where the player needs to mimic a random emoji displayed by the computer!


## Getting Started

I used [Affectiva](http://www.affectiva.com/)’s Emotion-as-a-Service API for this project. You can visit their [Developer Portal](http://developer.affectiva.com/) and try out some of the sample apps. Affectiva makes it really easy to extract detailed information about faces in an image or video stream. If you want better a sense for what information you can obtain, check out the [Metrics](http://developer.affectiva.com/metrics/) page.

### Project files
Main project files:
- **mimic.js**: Javascript file with code that connects to the Affectiva API and processes results.
- **index.html**: Dynamic webpage that displays the video feed and results.
- **mimic.css**: Stylesheet file that defines the layout and presentation for HTML elements.

There are two additional files provided for serving the project as a local web application: 

- **serve.py**: A lightweight Python webserver required to serve the webpage over HTTPS, so that we can access the webcam feed.
- **generate-pemfile.sh**: A shell script you’ll need to run once to generate an SSL certificate for the webserver.

## Deployment

In order to access the webcam stream, modern browsers require you to serve your web app over HTTPS. To run locally, you will need to generate a SSL certificate (this is a one-time step):

- Open a terminal or command-prompt, and ensure you are inside the `AIND-CV-Mimic/` directory.
- Run the following shell script: `generate-pemfile.sh`

This creates an SSL certificate file named `my-ssl-cert.pem` that is used to serve over https.

Now you can launch the server using:

```
python serve.py
```

_Note: The `serve.py` script uses Python 3._

Alternately, you can put your HTML, JS and CSS files on an online platform (such as [JSFiddle](https://jsfiddle.net/)) and develop your project there.

### Running and implementing the game

Open a web browser and go to: [https://localhost:4443/](https://localhost:4443/)

- Hit the Start button to initiate face tracking. You may have to give permission for the app to access your webcam.
- Hit the Stop button to stop tracking and Reset to reset the detector.
- When you’re done, you can shutdown the server by pressing `Ctrl+C` at the terminal.

_Note: Your browser may notify you that your connection is not secure - that is because the SSL certificate you just created is not signed by an SSL Certificate Authority‎. This is okay, because we are using it only as a workaround to access the webcam. You can suppress the warning or choose "Proceed Anyway" to open the page._



## Affectiva Resources

You may have to refer to resources in Affectiva's [JS SDK documentation](https://affectiva.readme.io/docs/getting-started-with-the-emotion-sdk-for-javascript) for more information abot the code.

Other references:

- [Affectiva Developer portal](http://developer.affectiva.com/index.html)
- [Demo](https://jsfiddle.net/affectiva/opyh5e8d/show/) that this project is based on
- Tutorials:
 [Camera stream](https://affectiva.readme.io/docs/analyze-the-camera-stream-3), [video](https://affectiva.readme.io/docs/analyze-a-video-frame-stream-4), [photo](https://affectiva.readme.io/docs/analyze-a-photo-3)


<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>. Please refer to [Udacity Terms of Service](https://www.udacity.com/legal) for further information.

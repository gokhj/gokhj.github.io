---
layout: post
title:  "London Loo Codes: Get The Toilet Codes of Cafés in London"
date:   2020-05-02 12:00:00 +0000
categories: projects
tags: react javascript python lambda node webapp
---
[Live Project Link](https://loocode.co.uk) | 
[Github Repo](https://github.com/gokhj/LondonLooCodes)

Inspired by this [Twitter Account](https://twitter.com/ldnloocodes), I decided to develop something helpful for others. Initially, I used their [Google Spreadsheet Data](https://docs.google.com/spreadsheets/d/1NZc0IPV9SV_Wy9xoDckHbVDgJyeW2Str231Uz_e0Mg4/edit#gid=0), and converted that into JSON (well, in my case BSON) fields.

This web app was developed with serverless stack, though in the long run, it might be best to go with a dedicated API. However, this is a toy project, so I wanted to keep everything as simple as possible.

Besides, using serverless stack is not costing me a single penny. I store this application on Netlify and implemented the backend logic with AWS Lambda and API Gateway services.

The stack of this project is React, Node, Python and MongoDB.

This is the main page of the application, it is showing you the details of every toilet around the city. Comfy.

![Main page](/assets/londonloocodes/main.png)

A user can contribute since the data is open-sourced.

![Contribute](/assets/londonloocodes/contribute.png)

The map view of the current codes across the city.

![Map View](/assets/londonloocodes/map.png)

Below you can find the explanations of the folders and what they do.

---
## /aws-lambda/
This folder has the functions for server-side logic. Currently, there are 3 functions, 2 of them are written with Python and 1 of them is written with NodeJS. Feel free to use the endpoints if you want to develop something on your own; they are in ```/react-app/src/util/Data.js```.

The functions are running at AWS Lambda service, and the endpoints were created with AWS API Gateway.

### get_data
This is the Python function to access the Mongo database and return the JSON data of the relevant query.

### convertGeoJson
This is the NodeJS function to communicate with endpoints and prepares another JSON field for OpenStreetMap API using a library called LeafletJS.

### post_data
This is the Python function to store form data submitted from the React app.

---

## /data/

This folder has the initial Google Spreadsheet Data and the Python script to convert the fields for the database. For more info, check comments on ```/data/csv_to_db.py```.

---

## /react-app/

This is the main front-end interface; please check its own ```README.md``` file for running instructions.
There are currently three distinct components and one utility service. I developed most of the components with classes, but I used hooks whenever I feel that it's necessary.

Check ```/react-app/src/App.js``` for the main interface.

PS: I used Netlify to host the whole app. ```public/_redirects``` is a necessary file for react-router integration.

---


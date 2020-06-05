---
layout: post
title:  "Your Spotify History and Recommendations: mySpotify.me"
date:   2020-02-03 12:00:00 +0100
categories: projects
tags: projects
---
[Live Project Link](https://myspotify.me/) |
[GitHub Repo](https://github.com/gokhj/mySpotify.me)

This is a React.JS project where people can see their top songs & artists by logging in with their respective Spotify accounts. The user can also create playlists with their top tracks, including in the last month, over the previous 6 months and account lifetime.

It's a serverless app, meaning there is no backend, and it doesn't store any information, initiated with create-react-app by Facebook.

**To run:**
```
yarn install
yarn start
```

**Known Issues**
- Logout is not properly working at this point, clicking the logout button deletes the access token cookie stored on the browser, however, the user needs to go to Spotify's website and logout from there as well. This is the only way to login with other Spotify accounts at the moment. Logout link https://www.spotify.com/logout/

## Screenshots:

### Main page && the buttons are disabled until login

![Readme%20md/Untitled.png](/assets/myspotify/1.png)

### Getting all time artist info

![Readme%20md/Untitled%201.png](/assets/myspotify/2.png)

### Mobile version of the app

![Readme%20md/Untitled%202.png](/assets/myspotify/3.png)

### Displaying track information && save as a playlist button

![Readme%20md/Untitled%203.png](/assets/myspotify/4.png)

### Created playlist on Spotify

![Readme%20md/Untitled%204.png](/assets/myspotify/5.png)
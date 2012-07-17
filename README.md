# furry-lana

What is the fewest number of steps which a developer could add image mangement to their site?

The role of this app is to make it so easy for devs to do file management the right way, that they wouldnt consider doing it any other way.

This includes:

* Native CDN support
* Long TTL
* Resize to sizes used in browser
  * Mobile specific sizes/compression (retna)


## Upload a user avatar

Needs:

* Image size and fill properties
* Url for hosted files
* Upload mechanism

Flow: Scenario upload avatar

* Sign up
* Server generates private key used for signing clientside parameters
* Create avatar bucket
* Optional: alter/add sizing options to bucket
  * fill, fit, stretch
  * dimensions
  * format (jpg, gif, png)
  * quality
* Optional: change bucket default image
* Add javascript to page
  * bucket
  * key (user id) - used with post upload callback so that the client can link the image to the uplaoder
  * signature
* User uploads file
* Callback hits callbackurl with
  * key - passed by the client in initial javascript
  * unique filename
* Reference file with http://domain/user-avatars/UX1FxR3/thumbnail.jpg
* Bonus: interface to allow user to alter image


Flow: Introduce new user avatar size

* Go to bucket in admin interface
* Add new size
* Watch progress


## Upload files for a blog post



# Implementation

## Javascript widget

## Client API

## File hosting

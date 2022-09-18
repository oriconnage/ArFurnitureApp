# AR App Design Document
### Team 16
### Ori Connage- @K1720485
### James Burke- @K1811535
### (Funiture AR)

Buying Furniture online is typically a leap of faith, we aim to help you make the right decision.

GitLab (https://gitlab.kingston.ac.uk/CI6330-2020-21-TeamApp16/TeamApp16_FurnitureAR.git)


## The Concept
Our client wants us to commission an app for home goods and furniture sellers using AR functionality to allow their customers to plan their interior layouts/designs.

## Business Requirements
What is the purpose of the app, what are we trying to accomplish?
Our app would be classed as a home improvement app, we want to use AR technology to place the piece of furniture that the user has selected from our catalogue and then see how it would look in the surroundings where they intend to put it in reality.

We want the user to use our app to style their room and figure out the desired layout before they ever buy a piece of furniture.

## What is the current problem(s) it will solve?

Buying furniture online is often a hit or miss, it either too small or too large for the space you wanted to put it in. with this app we aim to eliminate this problem as we will be able to render true to scale 3D products. This would also remove the tedious task of measuring for the customer.

## What should the app be able to do? What is the product's core functionality?
Should allow the user to browser a selection of furniture.
Should allow the user to use AR to place furniture in their room.
Should allow the user to manipulate object placed in their rooms.
Should allow the user to share on social media.
## What features will it need?
Ideally our app should be an ecommerce app like eBay/ Ikea where we would have seller upload a product and customers to buy the products, but due to the time constraints and learning curve creating a backend in a short period of time would be unlikely, so I have downsized this app for this coursework. Removing the ecommerce aspect from the app and limiting the catalogue to bedrooms items.

## MoSCoW

| Must Have                                                                                                                             | Should Have                        | Could Have                          | Wont Have         |   |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|-------------------------------------|-------------------|---|
| AR functionality:Ability to locate a surface.Ability to add some furniture to the surface.Must have depth – I.e., if behind an object | Dimension scanning                 | Cloud storage – to reduce App size. | Database of users |   |
| Catalogue of bedroom furniture                                                                                                        | Registration / Login functionality |                                     |                   |   |
| The ability to snap a photo.                                                                                                          |                                    |                                     |                   |   |
## Monetization business model
As this app idea would ideally be suitable for an ecommerce business, a way to monetize this app would be to add additional feature to create a furniture marketplace similar to eBay we can take a commission, listing fees, premium listing fees, selling fees etc.

But if we don't go down that route and keep to strictly an interior design app the way to monetize this app would be subscription, we could charge the customer monthly to use are app.

## Target audience
Our ideal user would be someone who would pay a subscription monthly for our app and that would be a tech savvy Interior designer/ decorator.

We are also targeting new homeowners that want to decorate their rooms.

Our app will be AR required which limits the types of devices that can download our app, google play store makes AR required app available to only devices that support ARCore. You can check the devices supported here: https://developers.google.com/ar/discover/supported-devices#google_play_csv

| | AR Required | AR Optional | | --- | --- | --- | | AR Feature usage | Your app needs ARCore for basic functionality. | ARCore augments your app's functionality. Your app can run without ARCore support. | | Play Store visibility | Your app is only listed in the Play Store on devices with ARCore support. | Your app follows normal listing procedures. | | Google Play Services for AR installation method | The Play Store installs Google Play Services for AR alongside your app. | Your app uses ArCoreApk.requestInstall() to download and install ARCore. | | Android minSdkVersion requirements | Android 7.0 (API Level 24) | Android 4.0 (API Level 14) |

## Development Methodology
### Progression
Team 16 will progress with this project by using the Gantt chart to know our schedule coupled with the MoSCoW table we should be able to determine the priority of the task. we will use the MoSCow table to see if we can implement a feature if we have time within our schedule.

### development
For this furniture AR application, team 16 will be using the Agile scrum methodology as it is perfect for a duo project while being inexpensive to implement. Scrum uses a method that break our targets into segment to be completed within an allocated timespan. This would allow us to implement the important mechanic first, review if it works then go onto implementing the 'should', 'could' and 'not' from the MoSCoW chart if there is enough time.

### Gantt's chart
In a separate documentation.





## Credits
Assets:

"Antique room furniture" (https://skfb.ly/6RVOn) by sadcats is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Round Bar Table" (https://skfb.ly/6WZI8) by TabbieCat is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Common Table And Chair" (https://skfb.ly/6VryQ) by mandragorasprout is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Four Modern Bookshelves" (https://skfb.ly/6wOzH) by Newsome Interactive is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Round Table" (https://skfb.ly/6SvGE) by shedmon is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Antique Desk" (https://skfb.ly/6vVrv) by Timothy Ahene is licensed under Creative Commons Attribution-NonCommercial (http://creativecommons.org/licenses/by-nc/4.0/).

"Gaming Chair [FREE DOWNLOAD]" (https://skfb.ly/6QZop) by Karlos is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

Android ARCore SDK - CameraPermissionHelper

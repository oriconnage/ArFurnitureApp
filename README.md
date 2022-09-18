AR App Design Document
Team 16
Ori Connage- @K1720485
James Burke- @K1811535
(Funiture AR)

Buying Furniture online is typically a leap of faith, we aim to help you make the right decision.

GitLab (https://gitlab.kingston.ac.uk/CI6330-2020-21-TeamApp16/TeamApp16_FurnitureAR.git)

Table of Contents
The concept 3

Business Requirements 3

What is the purpose of the app, what are we trying to accomplish? 3

What should the app be able to do? What is the product's core functionality? 3

What features will it need? 3

Monetization business model 4

Target audience 4

Development Methodology 5

Progression 5

development 5

Gantt's chart 5

Design plan 5

Navigation/ Screens 5

Dictionary 5

Relations 5

Catalogue Screen 5

Item Screen 5

AR Screen 6

Implementation 6

Gradle 6

Dependencies 6

Android 7

Catalogue Screen 8

Product Class 8

Recycler View 9

Click events for RecyclerView views 12

Layout 13

Item Screen 13

Implementing the AR Functionality 14

Setting up Session 14

Implementing Ar 15

Credits 15

The concept
Our client wants us to commission an app for home goods and furniture sellers using AR functionality to allow their customers to plan their interior layouts/designs.

Business Requirements
What is the purpose of the app, what are we trying to accomplish?
Our app would be classed as a home improvement app, we want to use AR technology to place the piece of furniture that the user has selected from our catalogue and then see how it would look in the surroundings where they intend to put it in reality.

We want the user to use our app to style their room and figure out the desired layout before they ever buy a piece of furniture.

What is the current problem(s) it will solve?

Buying furniture online is often a hit or miss, it either too small or too large for the space you wanted to put it in. with this app we aim to eliminate this problem as we will be able to render true to scale 3D products. This would also remove the tedious task of measuring for the customer.

What should the app be able to do? What is the product's core functionality?
Should allow the user to browser a selection of furniture.
Should allow the user to use AR to place furniture in their room.
Should allow the user to manipulate object placed in their rooms.
Should allow the user to share on social media.
What features will it need?
Ideally our app should be an ecommerce app like eBay/ Ikea where we would have seller upload a product and customers to buy the products, but due to the time constraints and learning curve creating a backend in a short period of time would be unlikely, so I have downsized this app for this coursework. Removing the ecommerce aspect from the app and limiting the catalogue to bedrooms items.

MoSCoW

Must Have	Should Have	Could Have	Wont Have
AR functionality:Ability to locate a surface.Ability to add some furniture to the surface.Must have depth – I.e., if behind an object	Dimension scanning	Cloud storage – to reduce App size.	Database of users
Catalogue of bedroom furniture	Registration / Login functionality		
The ability to snap a photo.			
| | | Great easy to use UX. | User profiles / dashboard | Share to social media function. | | | Search / filtering functionality | | | | | Seamless navigation | | | | | Ability to Favourite. | | | | | Ability to place furniture into a room. | | | | | Ability to manipulate furniture. | | | |

Monetization business model
As this app idea would ideally be suitable for an ecommerce business, a way to monetize this app would be to add additional feature to create a furniture marketplace similar to eBay we can take a commission, listing fees, premium listing fees, selling fees etc.

But if we don't go down that route and keep to strictly an interior design app the way to monetize this app would be subscription, we could charge the customer monthly to use are app.

Target audience
Our ideal user would be someone who would pay a subscription monthly for our app and that would be a tech savvy Interior designer/ decorator.

We are also targeting new homeowners that want to decorate their rooms.

Our app will be AR required which limits the types of devices that can download our app, google play store makes AR required app available to only devices that support ARCore. You can check the devices supported here: https://developers.google.com/ar/discover/supported-devices#google_play_csv

| | AR Required | AR Optional | | --- | --- | --- | | AR Feature usage | Your app needs ARCore for basic functionality. | ARCore augments your app's functionality. Your app can run without ARCore support. | | Play Store visibility | Your app is only listed in the Play Store on devices with ARCore support. | Your app follows normal listing procedures. | | Google Play Services for AR installation method | The Play Store installs Google Play Services for AR alongside your app. | Your app uses ArCoreApk.requestInstall() to download and install ARCore. | | Android minSdkVersion requirements | Android 7.0 (API Level 24) | Android 4.0 (API Level 14) |

Development Methodology
Progression
Team 16 will progress with this project by using the Gantt chart to know our schedule coupled with the MoSCoW table we should be able to determine the priority of the task. we will use the MoSCow table to see if we can implement a feature if we have time within our schedule.

development
For this furniture AR application, team 16 will be using the Agile scrum methodology as it is perfect for a duo project while being inexpensive to implement. Scrum uses a method that break our targets into segment to be completed within an allocated timespan. This would allow us to implement the important mechanic first, review if it works then go onto implementing the 'should', 'could' and 'not' from the MoSCoW chart if there is enough time.

Gantt's chart
In a separate documentation.

Design plan
Navigation/ Screens
Dictionary
We will have three screens:

Catalogue Screen – List view of each furniture item
Item Screen – Screen to show the details of any item of the catalogue (additionally, may display previous screenshots the user has taken using the AR functionality)
AR Screen – Camera view screen, likely an implementation of ARCore which covers the AR requirements (placing and manipulating furniture items)
Relations
Catalogue Screen -> Item screen

Item screen <-> AR Screen

AR Screen -> Share screenshot

Catalogue Screen
The user must be able to choose from a range of options in this app- in context, there must be multiple choices of furniture items the user can pick from with the intent to view in augmented reality.

It would therefore be important to provide an interface which displays a scrollable list of options, so as to be scalable and efficient through the means these options are presented. Furthermore, the user should be able to select which option they want by simply tapping on the specific item.

Each listed item should be presented with their respective name and image.

Item Screen
After selecting their desired item from the catalogue, the user should be presented with a new screen. This resultant screen will act as an interface to display further information about the item they have selected, such as a description, dimensions, etc. In addition, extra functionalities, such as sharing (to the internet), will be present on the item screen.

For this prototype, only the basic details (the item name and image) will be shown. Then the core AR functionality will be provided as a button on the screen. [Text Wrapping Break]

AR Screen
After toggling the AR mode the user has an option to view the furniture in 3d mode which mean that the user will see the model in the 3d viewer if the user stays in the AR mode, they would be prompted to find a surface this is so they can place the 3d object in the location they desired. On this screen the user should be able to take a picture, rotate the object and move it around.

Implementation
Gradle
Dependencies


We started off by adding the dependencies that we will be using for our application. From the Screen shot you can see we will be using:

glide
Google AR Core
JavaGL
RecyclerView
Android


As mention earlier in this document ARCore is only available on certain android mobile devices

"Android 7.0 (API Level 24)"

So, within the default config I changed the minSdkVersion to 24

We will also be using data binding library and view binding library in our application, so I enabled them.

Data Binding is a library that allow us to bind UI components in our layout to data sources in our app using declarative format rather than programmatically – this saves time and reduces the amount we have to code.

For example,

TextView textview = findViewByID(R.id.Image_name);

Textview.setText(viewModel.GetProductName());

Has been reduce to this.



Catalogue Screen
Product Class
We created a product class to bundle all the related data and functionality in one place.The product class has 5 attributes.

In the MainActivity file we implemented a method called getProductList where we insantiate products push the product into a list and returns that list

an example – in this screen shot you can see we added Sofa Arm Chair item to our product list

the reason why we are using URI for the image and AR URI is because we wanted to minimise the storage space that our app could potential take up if we had to install all the asset onto the device. As these 3D models file are quite large, I figured that uploading the assets in a GitHub folder and drawing the asset from there at runtime would be better than packaging it in the APK.

The only downside is this would require the user to have access to Wi-Fi / data to use this app.

Recycler View
T  o implement a list into the activity, we have opted for the use of the RecyclerView as it is a very efficient way to display long lists of information. This would make the app scalable if many items were to be added. In comparison to a similar view – the ListView – RecyclerView is more performant and versatile in that it has more features.

RecyclerView uses an Adapter to map data with UI components of each respective item. The Adapter contains the ViewHolder which handles this, where each instance in the list will have their own ViewHolder.

In order to achieve this, a java class was created to house the RecyclerView adapter.



Attributes are declared and the Array of product is initialised.



This function handles the view holder creation and view inflation.



This function is responsible for binding data to the child views of the view holder. Here, we get the position of the product in furniture list and we are binding the data to the layout listed item binding.

The view holder is an encapsulated class within the adapter class. The ViewHolder provides an object which describes a single item's view and metadata. We declared two binding attribute layout Listed Item Binding and Activity Item Screen Binding this removed the need for use to locate each item by id.

Shape1



Back to the Recycler view adapter, in the view holder, is a definition of a click event. This means that each item object is clickable.

I  n the main activity java class, on create method we use view binding. Which in hindsight wasn't that worth while as we only instantiate one object – The Recycler view, if we had multiple object to instantiate it would be more beneficial



You can see in the Initialize recycler view method the benefits of the view binding is that it removes the need to find view by id and calls the object directly .

Click events for RecyclerView views
To accommodate for click events, a public interface is defined in the adapter class. This will be implemented in the 'MainActivity' (catalogue screen).



See that in line 24, the class implements the interface that we defined in the adapter class.

In the main activity class, this function is implemented to account for what occurs when an item is clicked/tapped on. An intent is initialised and provided with data to pass on before the new activity is started.



Back in the recycler view adapter class, within the view holder class, it is described that when the user clicks on a specific view, this function is called.

Accessing images from the internet

In order to show the user photos of items, the external Glide framework is used- this allows URLs to be used to display images.



On line 48, Glide is used. Most importantly notice that it loads the image of a provided URL into the ImageView of a respective view holder.

Layout


Here's a look at the layout used by each recycled view holder. The IDs of each view are what the ViewHolder refers to.



Item Screen
Following the click of a listed item, the main activity handles Intent (described above) to start this activity. Note that it shows the item's associated name and image of what the user has selected. There is also a button at the bottom which will start the AR functionality of this app.

Implementing the AR Functionality
Setting up Session
We need to be able to manage the AR system state and lifecycle so we have implemented a function called onStart() here we check if ARCore is installed or/and up to date if ARcore isn't installed or up to date the session will fail to be created.



We also check if the app has permission to use the camera, using CameraPermissionHelper script part of google ARCore SDK.



Here are the possible exception that could happen when checking if ARCore is installed.

Implementing Ar
While researching we found out there are multiple methods of implementing Ar after trying a few methods we concluded that using the Scene viewer was the best and easily implementable method. The scene viewer is an immersive viewer that enables 3d and ar experience on android mobile devices and only needs a few lines of code to implement.



Credits
Assets:

"Antique room furniture" (https://skfb.ly/6RVOn) by sadcats is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Round Bar Table" (https://skfb.ly/6WZI8) by TabbieCat is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Common Table And Chair" (https://skfb.ly/6VryQ) by mandragorasprout is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Four Modern Bookshelves" (https://skfb.ly/6wOzH) by Newsome Interactive is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Round Table" (https://skfb.ly/6SvGE) by shedmon is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

"Antique Desk" (https://skfb.ly/6vVrv) by Timothy Ahene is licensed under Creative Commons Attribution-NonCommercial (http://creativecommons.org/licenses/by-nc/4.0/).

"Gaming Chair [FREE DOWNLOAD]" (https://skfb.ly/6QZop) by Karlos is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

Android ARCore SDK - CameraPermissionHelper

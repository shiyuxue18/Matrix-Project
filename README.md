# Matrix-Project
This project aims to help people post alerts to the map and examine it within the map.

## High level prject structure
ToolBar, ViewPager, MainFragment, LoginFragment and NavigationView.

## Control Panel
Control Panel is a container with everything mentioned in the last section inside.

|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
|    ToolBar   |   ControlPanel.java   |ControlPanel includes Toolbar|
||res/layout/activity_control_panel.xml|ControlPanel includes Toolbar|
|NavigationView|ControlPanel.java|ControlPanel includes NavigationView|
||res/layout/activity_control_panel.xml|ControlPanel includes NavigationView|
||res/layout/nav_header.xml|The layout of navigationview header, at the top|
||res/menu/drawer_view.xml|The menu item below navigationview header, includes settings & homes|

## LoginFragment
Login Fragment enables user to register, login and logout to app (with the assistance of Firebase Database).

|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
| LoginFragment|   ControlPanel.java   |ControlPanel contains LoginFragment|
||LoginFragment.java|Login Fragment logic java file|
||res/layout/fragment_login.xml|Login Fragment main UI container|
||res/layout/login.xml|Login UI xml for user to login and is included by fragment_login.xml|
||res/layout/logout.xml|Logout UI xml if user has logged in and is included by fragment_login.xml|

## MainFragment
Main user interface. There are several features.
### 1. Main feature
It shows Google Map and events on screen.

|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
| MainFragment |   ControlPanel.java   |ControlPanel contains MainFragment|
||MainFragment.java|Main Fragment logic java file|
||res/layout/fragment_main.xml|Main Fragment main UI container|
||res/raw/style_json|Styling Google map|

### 2. Upload Event to Firebase
Click button on right-bottom corner of picture above.

|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
|MainFragment(Upload events)|MainFragment.java|Main Fragment contains upload event feature|
||res/layout/dialog.xml|Main layout container|
||res/layout/report_event_spec.xml|The second page of upload event, set event details|
||res/layout/report_event_type.xml|The first page of upload event, set event type|
||ReportRecyclerViewAdapter.java|Recycler view adapter for setting up event type|
||res/layout/recyclerview_item.xml|Recycler view child view that is going to adapt to recycler view|

### 3. Display Event details in BottomSheet
Click any event on screen。

|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
|MainFragment(Bottom Sheet)|MainFragment.java|Main Fragment contains upload bottom sheet|
||res/layout/fragment_main.xml|Bottom Sheet layout container|

## Helper Classes
|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
|Helper|Item.java|Holds all item attributes, this is used to show ReportRecyclerViewAdapter|
||TrafficEvent.java|Holds all traffic event attributes|
||User.java|Holds all user attributes|
||LocationTracker.java|Get longitude and latitude of current location|
||Config.java|Temperary Configurations|
||Utils.java|Store util functions|

## Firebase Notifications
These files are used related to firebase cloud messaging, firebase cloud function and firebase database.

|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
|Firebase Cloud Messaging|MyFirebaseInstanceIDService.java|Get token from FCM|
||MyFirebaseMessagingService.java|Main Receiver of Firebase Cloud Messaging|
||CustomApplication|Help to register Firebase Cloud Messaging token when application boots|

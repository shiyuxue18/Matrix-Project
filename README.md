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
Login Fragment enables user to register, login and logout to app.

|     Part     |     Files related     |     Description     |
|--------------|-----------------------|---------------------|
| LoginFragment|   ControlPanel.java   |ControlPanel contains LoginFragment|
||LoginFragment.java|Login Fragment logic java file|
||res/layout/fragment_login.xml|Login Fragment main UI container|
||res/layout/login.xml|Login UI xml for user to login and is included by fragment_login.xml|
||res/layout/logout.xml|Logout UI xml if user has logged in and is included by fragment_login.xml|


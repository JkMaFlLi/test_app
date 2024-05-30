# Flipper Zero Sample App

This is a sample application for the Flipper Zero microcontroller, showcasing how to create a simple app with menus and popups using the Flipper Zero SDK.

## Features

- Main menu with two selectable items
- Two popups that display different messages
- Logging for tracing application flow

## Installation

1. Clone this repository to your local machine:
    ```sh
    git clone https://github.com/your-username/flipper-zero-sample-app.git
    ```

2. Navigate to the project directory:
    ```sh
    cd flipper-zero-sample-app
    ```

3. Build the project using the Flipper Zero SDK tools.

## Code Overview

The application consists of several key components:

### Main Menu

The main menu displays two options:
- `1st Submenu`
- `2nd Submenu`

Selecting either option will trigger a popup to be displayed.

### Popups

There are two popups:
- **Popup One**: Displays "I am GROOT!" with an icon.
- **Popup Two**: Displays "I am GROOT...too" with the same icon.

### Application Structure

#### Enums and Structs

- `TestAppScene`: Enum for different scenes in the app.
- `TestAppView`: Enum for different views in the app.
- `TestApp`: Struct for the app context, containing the scene manager, view dispatcher, menu, and popup.

#### Main Menu Scene

- `test_app_menu_callback_main_menu`: Callback for menu item selection.
- `test_app_scene_on_enter_main_menu`: Initializes and displays the main menu.
- `test_app_scene_on_event_main_menu`: Handles events for the main menu.
- `test_app_scene_on_exit_main_menu`: Cleans up when exiting the main menu.

#### Popup Scenes

- `test_app_scene_on_enter_popup_one`: Initializes and displays the first popup.
- `test_app_scene_on_event_popup_one`: Handles events for the first popup.
- `test_app_scene_on_exit_popup_one`: Cleans up when exiting the first popup.
- `test_app_scene_on_enter_popup_two`: Initializes and displays the second popup.
- `test_app_scene_on_event_popup_two`: Handles events for the second popup.
- `test_app_scene_on_exit_popup_two`: Cleans up when exiting the second popup.

### Event Handlers

- `test_app_scene_event_handlers`: Collection of all scene handlers.
- `test_app_scene_manager_custom_event_callback`: Handles custom events.
- `test_app_scene_manager_navigation_event_callback`: Handles navigation events.

### Initialization and Cleanup

- `test_app_scene_manager_init`: Initializes the scene manager.
- `test_app_view_dispatcher_init`: Initializes the views and view dispatcher.
- `test_app_init`: Initializes the app context, scene manager, and view dispatcher.
- `test_app_free`: Frees all resources used by the app.

### Entry Point

- `test_app_app`: The main function that sets up the app, runs the main loop, and cleans up on exit.

## Logging

The app uses the Flipper Zero logging system to log messages at various log levels. In the development environment, the log level is set to `Trace`, and in other environments, it is set to `Info`.

## Usage

Compile and upload the application to your Flipper Zero device. Navigate through the menu and interact with the popups to see how the application works.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- The Flipper Zero team for their excellent SDK and documentation.
- The open-source community for their contributions and support.

---

This is a basic overview and setup for your Flipper Zero sample app. Customize the README file further based on your specific needs and any additional features you may add to your application.

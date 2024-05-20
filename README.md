# Venezuelan EID Authentication Plugin

## Overview
The Venezuelan EID Authentication Plugin is a custom authentication plugin designed to integrate with the Plone content management system. Its primary function is to authenticate users based on their Venezuelan electronic identification, providing a secure and efficient means to validate user credentials.

## Features
- **EID Authentication**: Authenticate users through their Venezuelan electronic ID.
- **Plone Integration**: Seamlessly integrates with Plone.
- **Skin Setup**: Custom skins for the authentication process.
- **Extensive Testing**: Includes unit tests to ensure reliability.
- **Pluggable Authentication**: Support for pluggable authentication modules.

## Installation Instructions
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Yuriy/VenezuelanEidAuthPlugin.git
    ```
2. **Navigate to the Plugin Directory**:
    ```bash
    cd VenezuelanEidAuthPlugin
    ```
3. **Install Required Dependencies**:
    Ensure you have Plone installed and then add the plugin to your Plone installation:
    ```bash
    pip install -r requirements.txt
    ```
4. **Install the Plugin in Plone**:
    - Go to the Plone control panel.
    - Navigate to the "Add-on Products" section.
    - Install the "Venezuelan EID Authentication Plugin" from the list of available add-ons.

## Usage Examples
To activate the plugin within a Plone site:

1. Go to the Plone site setup.
2. Select the "Users and Groups" option.
3. Choose the "Plugin Configuration" tab.
4. Activate the "Venezuelan EID Authentication Plugin".

To verify active authentication plugins, you can use the following Python script:
```python
plugins = context.acl_users.plugins
auth_plugins = plugins.getAllPlugins(plugin_type='IAuthenticationPlugin')
print(list(auth_plugins['active']))
```

## Code Summary
The code structure is as follows:
- `config.py`: Configuration settings for the plugin.
- `VenezuelanEidAuthPlugin.py`: Main script for the plugin functionalities.
- `__init__.py`: Initialization file, making the directory a module.
- `Extensions/Install.py`: Handles the installation process in Plone, including setting up skins.
- `skins/VenezuelanEidAuthPlugin/checkActivatedPlugins.py`: Script to check active authentication plugins.
- `tests/`: Directory containing unit tests to ensure the robustness of the plugin.
  - `BaseVenezuelanEidAuthPluginTestCase.py`: Base test case setup.
  - `framework.py`: Framework setup for running tests.
  - `runalltests.py`: Script to run all tests.
  - `testAllVenezuelanEidAuthPlugin.py`: Individual test cases for the plugin.
  - `__init__.py`: Initialization file for the tests module.

## Contributing Guidelines
1. **Fork the Repository**: Create a personal fork of the repository on GitHub.
2. **Clone Your Fork**: 
    ```bash
    git clone https://github.com/<your-username>/VenezuelanEidAuthPlugin.git
    ```
3. **Create a Feature Branch**:
    ```bash
    git checkout -b feature/your-feature-name
    ```
4. **Make Changes**: Implement your feature or fix.
5. **Add and Commit Changes**:
    ```bash
    git add .
    git commit -m "Add your commit message here"
    ```
6. **Push to GitHub**:
    ```bash
    git push origin feature/your-feature-name
    ```
7. **Create a Pull Request**: Open a pull request to merge your changes back into the main repository.

## License
This project is licensed under the GNU General Public License v2.0. You are free to use, modify, and distribute this software under the terms of the GPL 2.0 or any later version. For more details, visit the [GPL License page](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html).
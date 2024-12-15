# Logi Options Plus Mini
[中文版本](README.md) | [English Version](README_EN.md)

**Logi Options Plus Mini** is a streamlined version of Logi Options Plus that only supports keyboards and mice, making Logitech keyboards and mice more efficient to use.
<img width="1518" alt="image" src="https://github.com/Qetesh/logi-options-plus-mini/assets/4559341/d4c503a9-51d8-4a18-af90-a3f3be508e8b">
<img width="1518" alt="image" src="https://github.com/Qetesh/logi-options-plus-mini/assets/4559341/14a85961-b022-4fc9-99bf-6e30b071f54c">
<img width="1518" alt="image" src="https://github.com/Qetesh/logi-options-plus-mini/assets/4559341/bf97e703-d5d5-43d6-9236-6e1d06b7c0c8">
<img width="806" alt="image" src="https://github.com/user-attachments/assets/66f8d2d7-5981-4085-9829-25c0189804a8">
<img width="928" alt="image" src="https://github.com/user-attachments/assets/4d555a79-9f95-455b-8ad4-a415f607c475">

## Project Overview
Refer to the official [Mass installation and configuration of Logitech Options+ software](https://prosupport.logi.com/hc/zh-cn/articles/6046882446359-Logitech-Options-软件的批量安装和配置)
This project is implemented through a shell script `logi-options-plus-mini.command`, which downloads the official installer and streamlines it by removing all functions except for keyboard and mouse.

## Features

- Only supports keyboards and mice
- Automatically retain configuration when uninstalling and upgrading
- Removes unnecessary features to improve software performance
  - analytics: user sharing of application usage and diagnostic data
  - flow
  - sso: user login 
  - update: application updates
  - dfu: device firmware updates
  - logivoice: Logitech voice 
  - aipromptbuilder: AI Prompt Builder (macOS only)
  - smartactions
  - device-recommendation: device recommendation (macOS only)
- Easy-to-use shell script
  - You can modify the installation options in the shell file to add needed features

## Usage

1. Clone this project locally
    ```bash
    git clone https://github.com/Qetesh/logi-options-plus-mini.git
    cd logi-options-plus-mini
    ```

2. Run the shell script (requires `sudo` permission to uninstall the old version)
  - macOS
    ```bash
    chmod u+x logi-options-plus-mini.command
    ./logi-options-plus-mini.command

    ##############################################################
    2024年12月15日 星期日 23时32分33秒 +08 | Starting install of Logi Options+
    ##############################################################
    
    Please select the features you want to keep(e.g. 2 6, default is none):
    1. analytics:             Shows or hides choice for users to opt in to share app usage and diagnostics data.
    2. flow:                  Shows or hides the Flow feature. Default value is Yes
    3. sso:                   Shows or hides ability for users to sign into the app.
    4. update:                Enables or disables app updates.
    5. dfu:                   Enables or disables device firmware updates.
    6. backlight:             Enables or disables keyboard backlight on the supported keyboards.
    7. logivoice:             Enables or disables LogiVoice feature.
    8. aipromptbuilder:       Enables or disables AI Prompt Builder feature.
    9. device-recommendation: Enables or disables device recommendation feature.
    10. smartactions:         Enables or disables Smart Actions feature.
    11. all
    Press enter for none
    
    Enter your choices: 
    ```
  - Windows (Requires running the `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned` command once in an administrator terminal)

    Right-click on the ps1 script and "Run with PowerShell"

  The script will automatically download the official installer and perform a streamlined installation.

## System Requirements

- macOS
- Windows
- Internet connection to download the official installer

## FAQ
- Some Macs cannot be uninstalled using the official method, and a third-party tool is required for uninstallation and then re-running. It has been tested that after using `Pearcleaner` for uninstallation, it can run normally after installation.

## Contributing

Feel free to submit issues and requests. You can contribute code as follows:

1. Fork this repository
2. Create your branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the [Apache License](LICENSE).

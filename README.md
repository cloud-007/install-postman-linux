1. Go to the Postman app download page at [https://www.getpostman.com/apps](https://www.getpostman.com/apps). You can choose the OS version from the drop-down: x64 for 64-bit Operating System and x86 for 32-bit based Linux.

2. Open the terminal and go to the directory where you have downloaded the tar file. If you have downloaded it in the Downloads folder:

    ```bash
    cd ~/Downloads/
    ```

3. Run the following commands:

    ```bash
    sudo rm -rf /opt/Postman/
    ```
    
    Extract the compressed file with the command below or use the GUI option:
    
    ```bash
    sudo tar xvf Postman-<your version>.tar.gz -C /opt/
    sudo ln -sf /opt/Postman/app/Postman /usr/bin/postman
    ```

4. Create a file for the desktop entry so you can easily search for the Postman app like any other app on your computer:

    ```bash
    nano ~/.local/share/applications/postman.desktop
    ```

5. Write the following in the file:

    ```plaintext
    [Desktop Entry]
    Encoding=UTF-8
    Name=Postman
    X-GNOME-FullName=Postman API Client
    Exec=/usr/bin/postman
    Icon=/opt/Postman/app/resources/app/assets/icon.png
    Terminal=false
    Type=Application
    Categories=Development;
    ```

# Configuration Kitty Terminal
### Installing zsh and kitty
1. Run the following command to install zsh using `dnf` package manager:
```bash
    sudo dnf install zsh
```
2. Run the following command to install kitty using `dnf` package manager::
```bash
     sudo dnf -y install kitty
```
### Changing default shell
3. To change the default shell for both the root user and a user with lower privileges, follow these steps:
    - 3.1. Check the current default shell:
    ```bash
        echo $SHELL
    ```
    - 3.2. Switch to the superuser:
    ```bash
        sudo su
    ```
    - 3.3. Change the shell for the low-privilege user (replace `alonso` with the actual username):
    ```bash
        usermod --shell /usr/bin/zsh alonso
    ```
    - 3.4. Change the shell for the root user:
    ```bash
        usermod --shell /usr/bin/zsh root
    ```
### Configuring `~/.zshrc`
4. To configure your `~/.zshrc` file based on the `zshrc.example` file in this repository.
### Installing zsh-syntax-highlighting
5. To install zsh-syntax-highlighting, follow these steps:
    - 5.1. Run the following command to install zsh-syntax-highlighting using `dnf` package manager:
    ```bash
        sudo dnf install zsh-syntax-highlighting
    ```
    - 5.2.Use the `locate` command to find the absolute path of `zsh-syntax-highlighting`:
    ```bash
        locate zsh-syntax-highlighting.zsh
    ```
    - 5.3. Add the following line to your `~/.zshrc` file to enable zsh-syntax-highlighting:
    ```bash
        source /usr/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
    ```
### Installing zsh-autosuggestions
6. To install zsh-autosuggestions, follow these steps:
    - 6.1. Run the following command to install zsh-autosuggestions using `dnf` package manager:
    ```bash
        sudo dnf install zsh-autosuggestions
    ```
    - 6.2.Use the `locate` command to find the absolute path of `zsh-autosuggestions`:
    ```bash
        locate zsh-autosuggestions.zsh
    ```
    - 6.3. Add the following line to your `~/.zshrc` file to enable zsh-autosuggestions::
    ```bash
        source /usr/share/zsh-autosuggestions/zsh-autosuggestions.zsh
    ```
### Installing zsh-sudo
7. To install zsh-sudo, follow these steps:
    - 7.1. Switch to the superuser:
    ```bash
        sudo su
    ```
    - 7.2. Navigate to the `/usr/share` directory::
    ```bash
        cd /usr/share
    ```
    - 7.3. Create a directory named `zsh-sudo`:
    ```bash
        mkdir zsh-sudo
    ```
    - 7.4. Change the ownership of the `zsh-sudo` directory to your user (replace `alonso` with your username):
    ```bash
        chown alonso:alonso zsh-sudo/
    ```
    - 7.5. Change into the `zsh-sudo` directory:
    ```bash
        cd zsh-sudo/
    ```
    - 7.6. Download the `sudo.plugin.zsh` file from the ohmyzsh repository:
    ```bash
        wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/plugins/sudo/sudo.plugin.zsh
    ```
    - 7.7. Add the following line to your `~/.zshrc` file to enable zsh-sudo:
    ```bash
        source /usr/share/zsh-sudo/sudo.plugin.zsh
    ```
### Installing lsd
8. Run the following command to install lsd using `dnf` package manager:
```bash
   sudo dnf install lsd
```
### Installing bat
9. Run the following command to install bat using `dnf` package manager:
```bash
   sudo dnf install bat
```
### Downloading and Installing `Hack Nerd Font`
10. To download and install `Hack Nerd Font`, follow these steps:
    - 10.1. Visit the [Hack Nerd Font download page](https://www.nerdfonts.com/font-downloads) and download the font package.
    - 10.2. Switch to the superuser:
    ```bash
        sudo su
    ```
    - 10.3. Navigate to the system fonts directory:
    ```bash
        cd /usr/share/fonts
    ```
    - 10.4. Move the downloaded `Hack.zip` file to the fonts directory. Adjust the path if necessary:
    ```bash
        mv ~/Downloads/Hack.zip .
    ```
    - 10.5. Unzip the `Hack.zip` file:
    ```bash
        unzip Hack.zip
    ```
    - 10.6. Remove the downloaded `Hack.zip` file:
    ```bash
        rm Hack.zip
    ```
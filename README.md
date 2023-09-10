### Docker Installation Guide

This guide provides step-by-step instructions for installing Docker on different operating systems. Docker is a popular platform for developing, shipping and running container applications.
### Installation

#### macOS

Docker Desktop (Recommended):
1. Download Docker Desktop for Mac.
2. Double-click the downloaded .dmg file to install.
3. Follow the on-screen instructions to complete the installation.
4. After installation, you can start Docker Desktop from your     Applications folder.

Homebrew (Alternative):
1. Install Homebrew if you don't have it already by following the instructions on the Homebrew website.
2. Open a terminal and run the following command to install Docker:

```bash
  brew install --cask docker
```
3. Follow the on-screen instructions to complete the installation.
    

#### Windows

Docker Desktop (Recommended):
1. Download Docker Desktop for Windows.
2. Double-click the downloaded installer (usually .exe) to install Docker Desktop.
3. Follow the on-screen instructions to complete the installation.
4. Once installed, Docker Desktop will run in the background.

Docker Toolbox (Legacy):
1. Download Docker Toolbox.
2. Double-click the downloaded installer (usually .exe) to install Docker Toolbox.
3. Follow the on-screen instructions to complete the installation.


#### Linux (Ubuntu as an example)
Using APT (Ubuntu/Debian):
1. Open a terminal.
2. Update the package index:

```bash
sudo apt-get update
```
3. Install the required packages to allow APT to use a repository over HTTPS:

```bash
    sudo apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
````
4. Add the Docker GPG key:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
````

5. Add the Docker repository:

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
````
6. Update the package index again:

```bash
sudo apt-get update
````
7. Install Docker:

```bash
sudo apt-get install -y docker-ce docker-ce-cli containerd.io
````

#### Post-Installation Steps

After installing Docker, you may need to add your user to the "docker" group and restart your system or restart the Docker service. Please refer to the official Docker documentation for post-installation steps and further configuration.

#### Verification

To verify that Docker is installed correctly, open a terminal and run:

```bash
docker --version
````
You should see the installed Docker version printed on the console.


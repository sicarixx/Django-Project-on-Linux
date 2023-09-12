## Django Project on Linux (Debian based distributions)
### 1- Required
We must have the following programs installed
1. Python3 `sudo apt install python3`
2. Pip `sudo apt install python3-pip`
3. [Visual Studio Code](https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64)

To install VS Code `.deb` we must go to the folder where VS Code was downloaded and execute 
```bash
sudo dpkg -i package-name.deb
```

### 2- Virtual environment and Django
Now we will create the folder where we will store the virtual environment and after that we will install it there
1. We create the project folder and move there
```bash
mkdir djangoproject
cd djangoproject
```
2. We install VirtualEnv `pip install virtualenv`
3. We create the virtual environment `virtualenv venv`
4. We activate the virtual environment `source venv/bin/activate`
5. We install Django `pip install django`

### 3- Creating the project
Now we will create the project and run it in our code editor which will be VS Code
1. `django-admin startproject nombre_del_proyecto .`
2. We run it with VS Code `code .`

### 4- Creating the app
Now we must create the application from the VS Code terminal

```bash
python3 manage.py startapp app_name
```

### 5- Localhost
```bash
python3 manage.py runserver
```
If everything has gone well, we must enter the localhost with the default port it uses [127.0.0.1:8000](http://127.0.0.1:8000) or if we want to occupy a different port, we will execute
```bash 
python3 manage.py runserver 3000
```
[127.0.0.1:3000](http://127.0.0.1:3000)
#### Notice
If we press `Ctrl + C` we can stop the local server

If you want to raise the server in your local network, you must first get the ip assigned to Eth0 or Wlan0
```bash
ifconfig
```
And then run the server on local ip plus the port (the port is if you want) check this example
```bash
python3 manage.py runserver 192.168.xxx.xxx 5000
```
#### Important information about local ip address
You must edit the `settings.py` file in your project, in the `ALLOWED_HOSTS` section, the default setting is like this
```bash
ALLOWED_HOSTS = []
```
We must add the local ip like this
```bash
ALLOWED_HOSTS = [192.168.xxx.xxx]
```
### 6- Links
- Django [djangoproject.com/](https://www.djangoproject.com/)
- Python [python.org/](https://www.python.org/)
- Visual Studio Code [code.visualstudio.com/](https://code.visualstudio.com/)

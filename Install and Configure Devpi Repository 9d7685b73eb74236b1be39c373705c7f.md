# Install and Configure Devpi Repository

# **1.Install and configure the necessary dependencies**

```bash
sudo apt install sqlite3 libsqlite3-dev wget gcc libssl-dev libbz2-dev libffi-dev
```

# 2.To download Python 3.7.0 using wget, you can use the following command:

```bash
wget https://www.python.org/ftp/python/3.7.0/Python-3.7.0.tgz
```

# 3.extract the contents of the Python 3.7.0 compressed file

```bash
tar xzf Python-3.7.0.tgz
```

# 4.change directory to python 3.7.0

```bash
cd python-3.7.0/
```

# 5.compiling Python from source code with optimizations enabled

```bash
./configure --enable-optimizations
```

# 6.The command **`make altinstall`** is used after configuring and compiling Python from source code to install it on your system as an alternative installation

```bash
make altinstall
```

# 7.get-pip.py

Download the script, from [https://bootstrap.pypa.io/get-pip.py](https://bootstrap.pypa.io/get-pip.py)

```bash
curl [https://bootstrap.pypa.io/get-pip.py](https://bootstrap.pypa.io/get-pip.py)
```

# 8.`cd` to the folder containing the `get-pip.py` file and run:

```bash
python get-pip.py
```

and

```bash
python3 get-pip.py
```

# 9.installs or updates the devpi-server package using pip for Python 3.7

```bash
python3.7 -m pip install -U devpi-server
```

# 10.installs or updates the devpi-client package using pip for Python 3.7

```bash
python3.7 -m pip install -U devpi-client
```

# 11.installs or updates the devpi-web package using pip for Python 3.7

```bash
python3.7 -m pip install -U devpi-web
```

# 12.To check the version of **`devpi-server`**, you can run the following command in your terminal:

```bash
devpi-server --version
```

# 13.initialize a new Devpi server

```bash
devpi-init
```

# 14.It appears you're trying to generate a Devpi server configuration file with specific port and host settings using the **`devpi-gen-config`** command

```bash
devpi-gen-config --port 4040 --host 0.0.0.0
```

# 15.To install Supervisor using pip, you can run the following command

```bash
python -m pip install supervisor
```

# 16.To start Supervisor with a specific configuration file, you can use the following command

```bash
supervisord -c gen-config/supervisord.conf
```

# 17.stop the firewalld service on a system using systemd as its init system

```bash
systemctl stop firewalld
```

- **Browse to the hostname**

```bash
localhost:4040
```
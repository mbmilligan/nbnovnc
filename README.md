# nbnovnc

**nbnovnc** provides Jupyter server and notebook extensions to proxy a notebook-side VNC session using noVNC, enabling users to run non-web applications within their Jupyter notebook server. This is mostly useful for hosted Jupyter environments such as JupyterHub or Binder.

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/mbmilligan/nbnovnc-demo/master)

![Screenshot](screenshot.png)

## Installation

### Install Dependencies
The extension requires [nbserverproxy](https://github.com/jupyterhub/nbserverproxy) and currently uses an opinionated VNC environment comprised of Xvfb, x11vnc, noVNC, and websockify.

On Debian/Ubuntu:
```
apt install xvfb x11vnc novnc websockify
```

### Install nbnovnc 
Install the library:
```
pip install git+https://github.com/ryanlovett/nbnovnc
```

Either install the extensions for the user:
```
jupyter serverextension enable  --py nbnovnc
jupyter nbextension     install --py nbnovnc
jupyter nbextension     enable  --py nbnovnc
```

Or install the extensions for all users on the system:
```
jupyter serverextension enable  --py --sys-prefix nbnovnc
jupyter nbextension     install --py --sys-prefix nbnovnc
jupyter nbextension     enable  --py --sys-prefix nbnovnc
```

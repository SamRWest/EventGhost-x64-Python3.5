# EventGhost

This is a test version of EventGhost. It is a work in progress.
This test version runs on Python 3.5 x64

## build requirements

* visual c >= 14.0 \*
* winows sdk >= 8.1
* cx_Freeze >= 5.1.1
* requests >= 2.19.1
* agithub >= 2.1
* pycurl >= 7.43.0.2
* qrcode >= 6.0
* tornado >= 5.1
* psutil >= 5.4.7
* websocket-client-py3 >= 0.15.0
* CommonMark >= 0.7.5
* comtypes >= 1.1.7
* future >= 0.16.0
* Pillow >= 5.2.0
* PyCrypto >= 2.6.1
* Sphinx >= 1.8.0b1
* wxPython >= 4.0.3
* pywin32 >= 223
* setuptools >= 40.2

\* Visual C is also comes with Visual Studio. You will need Visual Studio >= 2015

## build command

    python setup.py build_exe

## Setup

- Install Visual Studio 2017 Professional (to match python 3.5) from https://visualstudio.microsoft.com/vs/older-downloads/. Select:
    - 'Desktop development with C++' workload and
    - 'Python development' workload > 'Python native development tools' component.
![img.png](img.png)
- Install python dependencies, (in CMD shell):

```shell
python\python -m venv .venv
.venv\Scripts\activate

pip install cx_Freeze==5.1.1 requests==2.19.1 agithub==2.1 qrcode==6.0 tornado==5.1 psutil==5.4.7 websocket-client-py3==0.15.0 CommonMark==0.7.5
comtypes==1.1.7 future==0.16.0 Pillow==5.2.0 Sphinx==1.8.0b1 wxPython==4.0.3 pywin32==223 setuptools==40.2

pycurl==1.43.0 PyCrypto==2.6.1 pycurl==1.43.0 #TODO figure out how to install these ones
```

- Build eventghost
```powershell
set PATH=C:\Users\wes148\code\EventGhost-x64-Python3.5\Scripts;C:\Users\wes148\code\EventGhost-x64-Python3.5\libs; C:\Users\wes148\code\EventGhost-x64-Python3.5\include;%PATH%
python setup.py build_exe
```

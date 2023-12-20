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

## TODO
- CI build
- Fix startup exceptions
- Check old CI script for missing steps
- Copy built extension DLLs into final build dir
- Try poetry build
- Try with just minimal C++ build tools instead of whole VS install

## Setup

- Install Visual Studio 2017 (aka version 15.0) to match python 3.5 from https://visualstudio.microsoft.com/vs/older-downloads/.
  - Select:
      - 'Desktop development with C++' workload and
      - 'Python development' workload > 'Python native development tools' component.
      ![vs2015_setup.png](docs/vs2015_setup.png)
- Install the Windows Driver Kit (WDK) for [your version](https://stackoverflow.com/a/61378093) of Visual Studio 2017
- Install [Stackless Python 3.5](https://github.com/stackless-dev/stackless/wiki/Archives) to `.\python\`
- Install [InnoSetup 5.5.8](https://files.jrsoftware.org/is/5/)
- Install [MS HTML Help Compiler/Workshop](http://web.archive.org/web/20160201063255/http://download.microsoft.com/download/0/A/9/0A939EF6-E31C-430F-A3DF-DFAE7960D564/htmlhelp.exe)
- Install python dependencies, (in CMD shell):
    ```shell
    python\python -m pip install --upgrade pip
    python\python.exe -m pip install cx_Freeze==5.1.1 requests==2.19.1 agithub==2.1 qrcode==6.0 tornado==5.1 psutil==5.4.7 websocket-client-py3==0.15.0 CommonMark==0.7.5 comtypes==1.1.7 future==0.16.0 Pillow==5.2.0 Sphinx==1.8.0b1 wxPython==4.0.3 pywin32==223 setuptools==40.2 pywin32==223 comtypes==1.1.3 Pillow==3.4.2 pycryptodome==3.4.4 wxPython==4.0.3

    # Pycurl no longer supported, just install downloaded binaries from https://www.lfd.uci.edu/~gohlke/pythonlibs/
    python\python.exe -m pip install deps\pycurl-7.43.0.3-cp35-cp35m-win_amd64.whl

    PyCrypto==2.6.1 pycurl==1.43.0.2 #TODO figure out how to install these ones
    ```

- Build eventghost
```powershell
python\python.exe setup clean
python\python.exe setup build_exe
```

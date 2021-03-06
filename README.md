# open Platform of Universal Board Game
>A RPI SD&D Project

Team:
Boning Dong, Ziniu Yu, Shenrui Zhang, Tianxin Zhou

**open Platform of Universal Board Game** (a.k.a. openPubg) is an open text-based gaming platform that allows users to host their own servers and play different games through text messages or emails. This platform is designed to be powerful and  modularized, and also allows game developers to implement their own games through APIs for this platform.


## Installation
#### Run from binary
The pre-built binary can be run in Linux systems without any pre-installation. The user can simply download the binary files from the [release page](https://github.com/Erebuxy/openPubg/releases).

#### Run from source code
The user can also choose to run the server from Python source code. The server requires Python 3 (3.5 or above) and Google Gmail Python API. The user can either manually install all the requirements or run the automatic installation script that is included in the repository:
```shell
./install.sh
```

#### Build from source code
For more advanced usages, the user can also build openPubg from source. The Python binary is built through [`pyinstaller`](). So, the user needs install `pyinstaller` first and then build openPubg:
```shell
pip3 install pyinstaller
pyinstaller ./src/openPubg.py

```
This commands will generate a `dist` folder, and the bundled app can be found in the folder.


## Usage
To start the server, the user can run the binary:
```shell
./openPubg/openPubg
```
or run the source code:
```shell
./src/openPubg.py
# or
python3 ./src/openPubg.py
```
Then, the program will redirect the user into a web browser that allows the user to login a Gmail account. The Gmail account that the user login will be the address of the server. If the user has previously used the server on the current machine, the program will automatically login the previous account. The user can simply delete the `.credentials` folder to make the server forget the old account,

#### Commands
After lunching the server, the user will see the openPubg command line interface. There are several commands can be used in the command line:

| Command       | Description                                        |
|---------------|----------------------------------------------------|
|echo [message] |Print the given message                             |
|list           |List all the current running rooms                  |
|send           |Send a short message to given phone number or email |
|info           |Show the info log of the server                     |


## License
[MIT License](https://github.com/Erebuxy/openPubg/blob/master/LICENSE)


## Contribution summary
Boning Dong: Testing, fixing bugs, implementing the roomManager, textManager and data plumbing etc., writing code review, project documentation on Github.

Ziniu Yu: Testing, implementing the second game (PigDice), roomManager, writing the testing documents.

Shenrui Zhang: Testing, implementing the first (TicTacToe) and second game (PigDice), final release document.

Tianxin Zhou: Testing, fixing bugs, implementing the textManager, writing the testing documents, code review, final testing results.


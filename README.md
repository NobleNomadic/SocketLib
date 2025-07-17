# SocketLib
Library to automate and simplify socket connections in C.
Currently only supports TCP sockets, UDP coming soon.

## Using SocketLib
You can use SocketLib by copying the files within this repository (not the README) into your project, and then including the header files.
Check the header file for a quick reference of each function and what they do.

## Disclaimer
The functions in this library are meant to work with projects that use the [nomadic project structure](https://github.com/NobleNomadic/CPlate).
This is my personal way of coding hobby projects which uses a program state variable in each function.
This library and my standard of C programming are for my personal hobby projects, and this might not be the right way to handle sockets for your project.

## Example Usage
```c
#include "socketlib.h"

int main() {
  int *programState;
  int socketFD = TCPClientConnect(programState, "127.0.0.1", 22, 3);
  TCPClose(socketFD);
}
```

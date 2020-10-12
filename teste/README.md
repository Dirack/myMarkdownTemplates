## Welcome to Try it on docker Madagascar Environment!

This is a docker container with Madagascar package installed and pre-configured designed as a "try on" experience. 
This container has minimum resources configuration to allow portability, you can install other packages with apt-get if you need with
the following user account:

- Your user is: tryitondocker
- Your password is (sudo included): 12345

#### About Madagascar

Madagascar is an open-source software package for multidimensional data analysis and reproducible computational experiments. You can get more
details in [http://www.ahay.org](http://www.ahay.org/wiki/Main_Page).

#### About your local Madagascar installation

- The Madagascar binaries are installed in the directory identified by your RSFROOT environment variable.
You can show its variable content with the following comand:

```sh
~$ echo $RSFROOT
```

- The Madagascar source code is installed in the directory identified by your RSFSRC environment variable.
You can show its variable content with the following comand:

```sh
~$ echo $RSFRSC
```

- The Madagascar data binaries that you generate will be stored in the directory identified by your DATAPATH environment variable.
You can show its variable content with the following comand:

```sh
~$ echo $DATAPATH
```

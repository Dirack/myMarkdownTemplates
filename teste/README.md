## Welcome to Try it on docker Madagascar Environment!

This is a docker container with Madagascar package version 3.0 installed and pre-configured designed as a "try on" experience. 
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

#### How to add new programs on my local version of Madagascar?

If you need to install new programs in your local Madagascar package you should know where Madagascar binaries and
source code is installed: Usually, Madagascar keeps the path of your local copy source files in the $RSFSRC environment variable.
You can show that on a bash terminal using 'echo' command:

```sh
~$ echo "$RSFSRC"
```

And Madagascar will install executable files on your $RSFROOT directory. You can show that environment variable
with 'echo' too:

```sh
~$ echo "$RSFROOT"
```

Madagascar stores user programs in $RSFSRC/user directory. So, you can create a new directory or put this
repository inside that directory. In this repository, such as every user's repository in Madagascar, we have a compilation 
[SConstruct](https://github.com/Dirack/vfsa/blob/master/SConstruct) that compile the C programs.
Run 'scons' on your $RSFSRC/user/creGatherInterpolation repository to compile it:

```shell
~$ scons
```

And run 'scons install' in the top directory of your local Madagascar installation 
(the directory path in your $RSFSRC variable):

```shell
~$ sudo scons install
```

For more details, please check out the Madagascar official documentation wiki in the section 
["Adding new programs to Madagascar"](http://www.ahay.org/wiki/Adding_new_programs_to_Madagascar)

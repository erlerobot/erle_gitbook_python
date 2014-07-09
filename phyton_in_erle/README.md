# Phyton in Erle
---
Open a Erle terminal and try typing:
```
python
```
If Python gets initialized, you are ready. Jump to the last paragraph of this page *Compiling code*.
If not, follow the steps bellow:

##### Installing and configuring Phyton

For installing and running Python in Erle, the first thing you should do is downloading python for Linux from the ofiicial website (it is free):
https://www.python.org/download/

```
Python 3.4.1 compressed source tarball (for Linux, Unix or Mac OS X)

Python 3.4.1 xzipped source tarball (for Linux, Unix or Mac OS X, better compression)
```
This two files are avaliable for Linux, so choose one.

You can donwload it directly in Erle, using the command line:
```
wget http://www.python.org/ftp/python/3.4.1/Python-3.4.1.tgz
```
The other option is to download it to your computer and then using `scp `command copy it to Erle. You can find the instructions [in this tutorial](https://www.gitbook.io/book/erlerobotics/erle_gitbook_unixintroduction), more specifically ,[in this section](http://erlerobotics.gitbooks.io/erle_gitbook_unixintroduction/annex_iii_network_connection_with_erle/README.html).

After that you need to extract the files, doing for example:
```
tar -xzf Python-3.4.1.tgz
```
You should configure the path and type:
```
./configure
make
sudo make install
sudo apt-get install python
```


For more information, or more detailed explanations, you can read this short [tutorial](http://erlerobotics.gitbooks.io/erle_gitbook_unixintroduction/tutorial_7/README.html).

#####Compiling code

After having Python installed, for compilling a code you have two possibilities:

- Store the code in a python_file.py, and running it by typing:

```
python python_file.py
```
- Typing:

```
python
```
And after that type the code.You can use `quit()` to exit.

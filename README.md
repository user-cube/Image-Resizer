# Image Resizer
A simple python tool to resize multiple (or single) images.

## Setup
To run this resizer you should create a virtual environment (or install depedencies system wide).
If your default interpreter is python 3:
```bash
$ python -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```
If your default interpreter is python 2 and you have python 3 installed:
```bash
$ python3 -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```
If you are using Windows:
```shell
$ python -m venv venv
$ venv\Scripts\activate.bat
$ pip install -r requirements.txt
```

## Using resizer
The resizer has multiple options to work with.
You can check all of your options using:
```bash
$ python resizer.py --help
usage: conv.py [-h] [--single SINGLE] [--filter FILTER] [--content CONTENT]
               [--out OUT] [--h H] [--w W] [--ext EXT]

optional arguments:
  -h, --help         show this help message and exit
  --single SINGLE    Only converts a simple image file
  --filter FILTER    1- NEAREST 2-BILINEAR 3-BICUBIC 4-ANTIALIAS
  --content CONTENT  File or directory to convert
  --out OUT          Output directory
  --h H              HEIGHT
  --w W              WIDTH
  --ext EXT          Output extension file

```
Take in consideration:
* **--single** is, by default, 0, if your want use to multiple files user `--single 1 --content your_path`;
* **--filter** is, by default, 1,  you don't need to write the filter name, just the number;
* **--h** is, by default, 500px;
* **--w** is, by default, 500px.
* **--ext** is, by default, `.png`
* **--content** if you want use an entire directory make sure that you are using ``--single 1``

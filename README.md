# Torch

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/movor/torch/blob/master/LICENSE)

### Lightweight LAMP vagrant box mainly intended for web development using Laravel

*Torch is lightweight Vagrant box (below `600MB`) based on `Ubuntu` OS, with `PHP` and `Apache` as a HTTP server.
It was initially created for in-house development. After many hours using it, we decided - why not share it 
publicly. Hope some of you will find it useful.*

---

## Requirements

To be able to use this box you'll need `Virtualbox` and `Vagrant`. 
You can find more info and installation instructions in the following links:
[MacOS](https://medium.com/@JohnFoderaro/macos-sierra-vagrant-quick-start-guide-2b8b78913be3),
[Ubuntu](http://www.codebind.com/linux-tutorials/install-vagrant-ubuntu-16-04/) or follow
[Official Installation Docs](https://www.vagrantup.com/docs/installation/)

## Compatibility

| Torch      | Laravel           | PHP      | Apache  | MySql  | Box OS 
| ---------- | ----------------- | -------- | ------- | ------ | ------------
| **v0.1.x** | **>= 5.1, < 5.6** | 7.0.30   | 2.4.18  | 14.14  | Ubuntu 16.04

## Software Included

Beside software from the table above, all versions of Torch includes:

- Composer 
- Node
- NVM
- Yarn
- Git

## Setup The Box

If you did not clone this repo already

```bash
git clone https://github.com/movor/torch.git

# ... and navigate to created project directory
cd torch
```

Depending of the Larvel/PHP version you want to use, you need to checkout specific
Torch version/tag (see "Compatibility" section above).

First, list all tags with

```bash
git tag

# Should output something like:
v0.1.0
v0.1.1
v0.2.0
v0.3.0
```

So, if your intent is to use e.g. Laravel 5.5, you should switch to latest v0.1 version, 
in this case `v0.1.1`

```bash
git checkout v0.1.1

# It will warn you that you're in "detached HEAD" state, but don't worry
```

## Light The Torch

To start a Torch Vagrant box, type

```bash
vagrant up
```

and wait for a while. Box is being downloaded, installed and powered up.

After all of this is completed, we can ssh into the box itself with

```bash
vagrant ssh
```

## Running Laravel Project On Torch Box

To keep this README as clean and short as possible, we dedicated entire
[blog post on our web site](https://movor.io/article/running-laravel-55-on-torch-vagrant-box)
and wrote step by step instructions on how to setup Laravel project in there. 

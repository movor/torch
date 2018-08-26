# Torch

[![Github All Releases](https://img.shields.io/github/downloads/movor/torch/total.svg)]()
[![License](https://poser.pugx.org/movor/torch/license)](https://packagist.org/packages/movor/torch)

### Lightweight LAMP vagrant box mainly intended for web development using Laravel

*Torch is lightweight Vagrant box (below `600MB`) based on `Ubuntu` OS, with `PHP` and `Apache` as a webserver.
It was initially created for in house development. After many hours of using it, we decided - why not share
it publicly. We hope some of you will find it usefull.*

---

## Requirements

To be able to use this box you'll need Vagrant and Virtualbox. 
You can find more info and installation instructions in the links below

- [MacOS - using Homebew](https://medium.com/@JohnFoderaro/macos-sierra-vagrant-quick-start-guide-2b8b78913be3)
- [Ubuntu](http://www.codebind.com/linux-tutorials/install-vagrant-ubuntu-16-04/)
- [Other - Official Installation Docs](https://www.vagrantup.com/docs/installation/)

## Compatibility

| Torch      | Laravel          | PHP    | Box OS 
| ---------- | ---------------- | ------ | ------------
| **v0.0.1** | **>= 5.1 < 5.6** | v7.0   | Ubuntu 16.04

## Software Included

All versions of Torch includes:

- Apache
- MySQL
- Node.js
- Composer
- Git
- NVM
- Yarn

## Setup The Box

If you did not clone this repo already

```bash
git clone git@github.com:movor/torch
```

Navigate to created directory

```bash
cd torch
```

Here, you'll need to edit Vagrantfile with your favorite editor, 
mine is Vim

```bash
vim Vagrantfile
```

There is only one line you'll need to change

```ruby
config.vm.synced_folder "~/Development/web", "/var/www", :mount_options => ["dmode=777", "fmode=777"]
```

Actually, only `~/Develompent/web` needs to be replaced by you web projects dir.
Vagrant itself will mount this directory internally to `/var/www`, so every project you have in there
will be accessible from within this box and Apache can serve them all - direclty to your browser.

## Run The Box

Now, only thing we need to do is 

```bash
vagrant up
```

and wait for a while - box is being downloaded, installed and powered up.

After all of this is completed, we can ssh into the box itself

```bash
vagrant ssh
```

## Setting Up Apache To Serve Our Project
TODO













# Torch

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/movor/torch/blob/master/LICENSE)

### Lightweight LAMP vagrant box mainly intended for web development using Laravel

*Torch is lightweight Vagrant box (below **500MB**) based on **Ubuntu** server, with **PHP** and **Apache** as a HTTP server. It was initially created for in-house development. After many hours using it, we decided - why not share it publicly. Hope some of you will find it useful.*

---

## Requirements

To be able to use this box you'll need **Virtualbox** and **Vagrant**. 
You can find more info and installation instructions in the following links:
[MacOS](https://medium.com/@JohnFoderaro/macos-sierra-vagrant-quick-start-guide-2b8b78913be3),
[Ubuntu](http://www.codebind.com/linux-tutorials/install-vagrant-ubuntu-16-04/) or follow
[Official Installation Docs](https://www.vagrantup.com/docs/installation/)

## Compatibility

| Torch      | Laravel           | PHP  | Apache  | MySql  | Box OS 
| ---------- | ----------------- | ---- | ------- | ------ | ------------
| **v0.1**   | **>= 5.1, < 5.6** | 7.0  | 2.4     | 14.14  | Ubuntu 16.04
| **v0.2**   | **>= 5.6**        | 7.1  | 2.4     | 14.14  | Ubuntu 16.04
| **v0.3**   | **>= 5.6**        | 7.2  | 2.4     | 14.14  | Ubuntu 16.04

## Software Included

Beside software from the table above, all versions of Torch includes:

- Composer
- Node
- NPM
- NVM
- Yarn
- Git

If your're curious about exact versions of above software, checkout our official 
[Vagrant Cloud Repo](https://app.vagrantup.com/movor/boxes/torch)

## Setup The Box

If you did not clone this repo already

```bash
git clone https://github.com/movor/torch.git

# ... and navigate to created project directory
cd torch
```

Depending of the Laravel and PHP version you want to use, you need to checkout specific
Torch branch (see "Compatibility" section above).

Let's say we want to use **Laravel 5.5**, in this case we'll need to switch to branch `0.1`.

```bash
git checkout 0.1
```

## Light The Torch

We're ready to light the torch!

There is actually 2 roads from here. 

### Vagrant Apprentice Road

At this point, you might need some further info about setting up Laravel project with the Torch box.

We dedicated entire blog post on our website:
[Running Laravel On Torch Vagrant Box](https://movor.io/article/running-laravel-on-lightweight-torch-vagrant-box#light-the-torch)

### Vagrant Master Road

If you know what should be done, and you're using vagrant for a while, start with inspecting `Vagrantfile` and check
details about assigned operating memory, number of cores, shared folders etc.

Finally run 

```bash
vagrant up
```

Vagrant will download, install and power up the Torch box.

After this process is finished, type

```bash
vagrant ssh
```

aaaannd your're in :beers:

---

Happy coding and vagranting,

[Movor](https://movor.io/) team

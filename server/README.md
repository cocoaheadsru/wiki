# CocoaHeads Server

This is the root path for [CocoaHeads Server](https://github.com/cocoaheadsru/server) documentation. Server side api for CocoaHeads Russia app. It was built with Swift and backed by Vapor.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

What things you need to install the software and how to install them. At first verify swift installation:

```
eval "$(curl -sL check.vapor.sh)"
```

### Installing

A step by step series of examples that tell you have to get a development env running


#### Add Homebrew Tap

```
brew tap vapor/homebrew-tap
brew update
```

#### Install Vapor

```
brew install vapor
```

#### Install MySQL

```
brew install mysql
```
Start mysql server

```
mysql.server start
```
Create database

```
mysql -u root
CREATE DATABASE cocoaheads
```

#### Create project

```
vapor new server --template=cocoaheadsru/server
```

#### Build project

Change directory

```
cd server
```
Create xcode project

```
vapor xcode
```



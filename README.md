![U-ASK](./logo.svg)
# U-ASK Custom Forms
U-ASK is a solution that allows users to develop complex custom forms. It has two main components :
 - [U-ASK Management System](https://github.com/u-ask/uask-sys#readme): a backend server and a client library.
 - [U-ASK Web Application](https://github.com/u-ask/uask-app#readme): a frontend web application.
 
This repository's goal is to demonstrate the fonctionning of U-ASK. For a more advanced usage, refer to the dedicated documentation of the two components linked above.

For demonstration purpose the repositories of the backend and frontend are mounted to this one as submodules.

The demo is organized in five steps :
  - [Install](#install): install the dependencies of both components.
  - [Configure](#configure): set the environment.
  - [Build](#build): build the static frontend (with the configured environment).
  - [Database setup](#database-setup): create the backend database tables.
  - [Start](#start): start backend and frontend.

# Install
Initialize the repositories locally :
```
git clone https://github.com/u-ask/uask.git
cd uask
npm run inst
```
This will initialize the submodules and install dependencies for each.

The relevant sections for install steps in submodule documentations are :
 - [Install server](https://github.com/u-ask/uask-sys#install-the-server).
 - [Install web app](https://github.com/u-ask/uask-app#install-the-application).

# Configure
Cofiguration leverage multiple environment variables that are described in submodule documentations. For testing purpose we will use [dotenv](https://github.com/motdotla/dotenv#readme) configuration files. In production, host level environment variables MUST be used. The following will copy `.env` files in submodule directories.
```
npm run config
```

The relevant sections for configuration steps in submodule documentations are :
 - [Configure server](https://github.com/u-ask/uask-sys#server-configuration).
 - [Configure web app](https://github.com/u-ask/uask-app#application-configuration).

# Build
This will build the web application according to the environment. Backend server is already built.
```
npm run build
```

The relevant sections for build steps in submodule documentations are :
 - [Build web app](https://github.com/u-ask/uask-app#build-the-application).

# Database setup
The system has been tested and developped on [Postgres SQL database](https://www.postgresql.org/). The present demo runs on [SQLite](https://www.sqlite.org/index.html) for simplicity.
```
npm run db
```

The relevant sections for database setup steps in submodule documentations are :
 - [Set up server database](https://github.com/u-ask/uask-sys#database-initialization).

# Start the demo
```
npm run start
```
Now navigate to the demo application : http://localhost:8080/Demo-eCRF.

The relevant sections for start steps in submodule documentations are :
 - [Start server](https://github.com/u-ask/uask-sys#starting-the-server).
 - [Start web app](https://github.com/u-ask/uask-app#serve-the-application).

_*Node:*_ a demo specific login screen is displayed: choose the role to connect with. A regular authorization code flow is used in production mode.

For a (very) brief introduction to the U-ASK web application see the [How to use section of U-ASK Web Application](https://github.com/u-ask/uask-app#how-to-use).
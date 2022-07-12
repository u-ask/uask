![U-ASK](./logo.svg)
# U-ASK Custom Forms
U-ASK is a solution that allows users to develop complex custom forms. It has two main components :
 - [U-ASK Management System](https://github.com/u-ask/uask-sys#readme): a backend server and a client library.
 - [U-ASK Web Application](https://github.com/u-ask/uask-app#readme): a frontend web application.
 
This repository's goal is to demonstrate the fonctionning of U-ASK. For a more advanced usage, refer to the documentation of the component repositories given above.

For demonstration purpose the component repositories above are linked to this one as submodules.

# Install
Initialize the repositories locally :
```
git clone https://github.com/u-ask/uask.git
cd uask
npm run inst
```
This will initialize the submodules and install dependencies for each.

The relevant sections for install steps in submodule documentations are :
 - [U-ASK Management System](https://github.com/u-ask/uask-sys#install-the-server): a backend server and a client library.
 - [U-ASK Web Application](https://github.com/u-ask/uask-app#install-the-application): a frontend web application.

# Configure
Cofiguration leverage multiple environment variables that are described in submodule documentations. For testing purpose we will use [dotenv](https://github.com/motdotla/dotenv#readme) configuration files. In production, host level environment variables MUST be used. The following will copy `.env` files in submodule directories.
```
npm run config
```

The relevant sections for configuration steps in submodule documentations are :
 - [U-ASK Management System](https://github.com/u-ask/uask-sys#server-configuration): a backend server and a client library.
 - [U-ASK Web Application](https://github.com/u-ask/uask-app#application-configuration): a frontend web application.

# Build
This will build the web application according to the environment. Backend server is already built.
```
npm run build
```

The relevant sections for build steps in submodule documentations are :
 - [U-ASK Web Application](https://github.com/u-ask/uask-app#build-the-application): a frontend web application.

# Database setup
The system has been tested and developped on [Postgres SQL database](https://www.postgresql.org/). The present demo runs on [SQLite](https://www.sqlite.org/index.html) for simplicity.
```
npm run db
```

The relevant sections for database setup steps in submodule documentations are :
 - [U-ASK Management System](https://github.com/u-ask/uask-sys#database-initialization): a backend server and a client library.

# Start the demo
```
npm run start
```
Now navigate to the demo application : http://localhost:8080/Demo-eCRF.

The relevant sections for start steps in submodule documentations are :
 - [U-ASK Management System](https://github.com/u-ask/uask-sys#starting-the-server): a backend server and a client library.
 - [U-ASK Web Application](https://github.com/u-ask/uask-app#serve-the-application): a frontend web application.

_*Node:*_ a demo specific login screen is displayed: choose the role to connect with. A regular authorization code flow is used in production mode.

For a (very) brief introduction to the U-ASK web application see the [How to use section of U-ASK Web Application](https://github.com/u-ask/uask-app#how-to-use).
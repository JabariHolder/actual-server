This is the main project to run [Actual](https://github.com/actualbudget/actual), a local-first personal finance tool. It comes with the latest version of Actual, and a server to persist changes and make data available across all devices.

### Getting Started
Actual is a local-first personal finance tool. It is 100% free and open-source, written in NodeJS, it has a synchronization element so that all your changes can move between devices without any heavy lifting.

If you are interested in contributing, or want to know how development works, see our [contributing](https://actualbudget.org/docs/contributing/) document we would love to have you.

Want to say thanks? Click the ⭐ at the top of the page.

### Documentation 

We have a wide range of documentation on how to use Actual. This is all available in our [Community Documentation](https://actualbudget.org/docs/), including topics on [installing](https://actualbudget.org/docs/install/), [Budgeting](https://actualbudget.org/docs/budgeting/), [Account Management](https://actualbudget.org/docs/accounts/), [Tips & Tricks](https://actualbudget.org/docs/getting-started/tipstricks) and some documentation for developers.

### Feature Requests
Current feature requests can be seen [here](https://github.com/actualbudget/actual/issues?q=is%3Aissue+label%3A%22needs+votes%22+sort%3Areactions-%2B1-desc). Vote for your favorite requests by reacting 👍 to the top comment of the request.

To add new feature requests, open a new Issue of the "Feature Request" type.

## Running via Docker

To run using a Docker container you can use following commands;

```
git clone https://github.com/actualbudget/actual-server.git
cd actual-server
docker build -t actual-server .
docker run --restart=unless-stopped -d -p 5006:5006 -v ${pwd}/data:/data --name holderfinance actual-server
docker-compose -p actual-server up
```

PI
```
sudo route -n
sudo route add default gw 10.0.0.1

curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
npm install -g yarn pm2
sudo pm2 start yarn --name holderfinance -- start
sudo pm2 startup
sudo pm2 save --force
 ```
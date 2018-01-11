First we will install the latest NodeJS, the best way to make it easy and correct is to use NVM -  **Node Version Manager**

To minimize chances of permissions errors, you can configure npm to use a different directory. In this example, it will be a hidden directory on your home folder.

Install nvm:
```sh
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
$ bash install_nvm.sh
```

1. Make a directory for global installations:
```sh
mkdir ~/.npm-global
```
2. Configure npm to use the new directory path: 
```sh
npm config set prefix '~/.npm-global'
```
3. Open or create a ~/.profile file and add this line: 
```sh
export PATH=~/.npm-global/bin:$PATH
```
4. Back on the command line, update your system variables:
```sh
source ~/.profile
```
Test: Download Angular-CLI globally without using sudo.
```sh
npm i @angular/cli
```

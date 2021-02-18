# hubert

# README

## Clone Repo

Clone it.

```bash
git clone https://github.com/CodeTheDream/rsites-api.git
cd rsites-api
```

## Download Ruby

This project is using ruby 2.6.0. You must have that locally before you can begin working on this project. [Install rbenv](https://github.com/rbenv/rbenv) if you haven't already.

### MacOs
```bash
brew install rbenv
echo 'eval "$(rbenv init -)"' >> ~/.zshrc # or ~/.bash_profile if you're still on bash
source ~/.zshrc # or close the window and relaunch
rbenv install 2.6.0 # and wait for it to finish
```
### Debian, Ubuntu and their derivatives

```bash
sudo apt install rbenv
```

## Install PostgreSQL
### Mac OS
[MacOS PostgreSQL Install](https://www.digitalocean.com/community/tutorials/how-to-use-postgresql-with-your-ruby-on-rails-application-on-macos)
```bash
brew install postgresql
```
### Ubuntu
[Ubuntu PostgreSQL Install](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04)
```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
```

## Get Google Maps API credentials
Get the Google Maps API key from one of the main devs on the project (and the master key if you need it). Insert GOOGLE_MAP_JS_API_KEY if it’s not already, otherwise, the seeder will complain about not having the correct Google Maps API key when you go to try setting up the DB.

Install vim if it is not already installed:

### Ubuntu
```bash
sudo apt-get install vim
```
Insert key
```bash
EDITOR="vim" rails credentials:edit
```

Also make sure that `config/master.key` has the correct master key.

## Build the app and run it

```bash
bundle
rails db:setup
rails s
```


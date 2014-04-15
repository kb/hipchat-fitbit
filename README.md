# Hipchat Fitbit

A hastily hacked together script to update your Hipchat status with your total step count from Fitbit.

# Setup

* [Create](https://dev.fitbit.com/apps/new) a Fitbit OAuth app
* Add the Client Key and Client Secret to file at the root of the script directory called `.fitgem.yml`
```yml
oauth:
  consumer_key: "your consumer key here"
  consumer_secret: "your consumer secret here"
```
* Goto your Hipchat [Account Settings](https://crashlytics.hipchat.com/account) and create an APIv2 OAuth bearer token
* Add the generated token and your Hipchat login email to a file at the root of the script directory called `.hipchat.yml`
```yml
:email: "your hipchat login email"
:oauth:
  :token: "your APIv2 OAuth bearer token"
```
* (Optional) Setup a rvm or rbenv gemset
* Install bunder via `gem install bundler`
* Install gems via `bundle install`
* Run the script via terminal `./update_status`
    * The first time through will require you to authorize your Fitbit OAuth app

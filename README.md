# cfna2018-blue
A Test App for Blue-Green Deployment Hands-on Labs

## Setup this example
* You'll be assigned a jumphost user on cfdev{n}@bg-lab1.cfna2018.starkandwayne.com
   Where {n} is a number assigned by instructor
* Fork this repository manually on github https://github.com/starkandwayne/cfna2018-blue

## Run this lab
* `ssh cfdev<n>@bg-lab1.cfna2018.starkandwayne.com`
* Clone your fork of this repository `git clone https://github.com/<your github username>/cfna2018-blue`
* Add your github username to ci/settings.yml
* `fly -t cfna2018 login -k -u ci -p ${CONCOURSE_PASSWORD} -c https://ci.cfna2018.starkandwayne.com`
* Run Repipe from the forked repository`./ci/repipe.sh`

## View your Concourse Pipeline
https://ci.cfna2018.starkandwayne.com

## Get a summary of all the pipelines in the lab
https://ci.cfna2018.starkandwayne.com/beta/dashboard

## Test Development workflow
* Edit the application https://github.com/<github username>/cfna2018-blue/blob/master/index.js
* The simplest noticeable effect is to uncomment line 35
* This will trigger the pipeline


# Userify Elastic Beanstalk configuration

## Introduction

In order to deploy this, you should copy the .ebextensions/userify.config into your application's .ebextensions/ directory. (If you don't have one, just create one in the root of your application before deploying or `eb deploy`.)

Also add the following environment properties to your application's Elastic Beanstalk configuration under `Configuration` > `Software Configuration` (click the gear) and then Environment variables at the bottom. You can find the correct values under in Userify under "Review Credentials".


| **Name**             | **Suggested Value**                                                                           |
| -------------------- | --------------------------------------------------------------------------------------------- |
| USERIFY_API_ID       | Your server group's API Id                                                                    |
| USERIFY_API_KEY      | Your server group's API Key                                                                   |
| USERIFY_COMPANY      | Whatever you like (Not used by the shim directly -- just for information on each node)        |
| USERIFY_PROJECT      | Whatever you like (Not used by the shim directly -- just for information on each node)        |
| USERIFY_SELF_SIGNED  | Either 1 or 0, depending on if Userify should check certificates. Usually should be 0.        |
| USERIFY_SHIM_HOST    | Usually shim.userify.com if you're using Userify Cloud, or your server hostname otherwise.    |
| USERIFY_STATIC_HOST  | Usually static.userify.com if you're using Userify Cloud, or your server hostname otherwise.  |

# Vaultwarden on Render

This repository is designed for people who don't want to overpay for a bitwarden subscription) Taking money for a password manager in 2025 is a big deal...

With this repository, you can easily deploy your [Vaultwarden](https://github.com/dani-garcia/vaultwarden) instance to resources render.com. You need to add any database (for example, supabase, a postgres database is also created with vaultwarden, you can use it) using the environment variables provided by the Vaultwarden Wiki. 
Please check out their wiki/documentation to learn more about environment variables and how to use them. 

Below you can find some of the necessary (at least to run this hosting configuration) and recommended parametersc:

|Environment Variable|Required?|Explanation|
|---|-|---|
|ADMIN_TOKEN|No|For admin access to admin dashboard, use [this wiki page](https://github.com/dani-garcia/vaultwarden/wiki/Enabling-admin-page) for instructions on how to generate a secure token. This repo will auto generate a value which you can change later by going to your Render dashboard then go to your service then go to `Environment` tab end edit its value. If you want to completely disable it then remove the environment variable entirely|
|DATABASE_URL|Yes|For database access to store info (If you use the render database, if they delete 30 day!!!)|
|SIGNUPS_ALLOWED|No|Allows users to sign up, set it to `false` after you make your own account on your hosted instance if you don't want anyone else to be able to sign up, allowed values are `true` or `false`|
|WEB_VAULT_ENABLED|No|Allows access to the web interface without needing the desktop and mobile clients or browser extensions. Values are `true` or `false`|

### Other free database providers:
- [Supabase](https://supabase.com/)  
- [Fly.io](https://fly.io/)
- [Render](https://render.com/) Yes render -> render -> render...

## Deployment

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/imsweetdogs/Vaultwarden-Render)

## Upgrading
This uses Vaultwarden's latest Docker image, so just manually deploy latest commit on Render. If you get DB connection errors, shut it down completely from the settings and then restart after a few minutes or set the DB connections environment variable to a number less than or equal to half the max limit provided by the DB hosting service to avoid this problem.

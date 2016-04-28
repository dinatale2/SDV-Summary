# SDV-Summary
A Flask webapp using Python Image Library to reconstruct and display a summary of the player and farm from a Stardew Valley save file.

## Configuration
The `SDV_APP_SETTINGS` environment variable is used in order to specify which Python object to load for configuration from config.py as per Flask's config.from_object. In that file the following settings can be used:

### Mandatory Settings
`UPLOAD_FOLDER` where uploaded files are stored
`SECRET_KEY` for Flask's sessions etc.
`MAX_CONTENT_LENGTH` in bytes for uploads

`PASSWORD_ATTEMPTS_LIMIT` (currently unused)
`PASSWORD_MIN_LENGTH` used to determine minimum password length for registering users

`IMGUR_CLIENTID` for imgur integration
`IMGUR_SECRET` for imgur integration
`IMGUR_DIRECT_UPLOAD` to upload directly to imgur by sending file rather than by directing imgur to url (can't redirect imgur to localhost, for example, when testing)

`RECAPTCHA_ENABLED` for the ReCaptcha on the signup form
`RECAPTCHA_SITE_KEY` as above
`RECAPTCHA_SECRET_KEY` as above

`ANALYTICS_ID` to report interactions server-side to Google Analytics using google-measurement-protocol

`DEBUG` set to True for helpful debugging; never set to True in production environment

#### Database

`USE_SQLITE`

##### SQLite

`DB_SQLITE`

##### PostgreSQL

`DB_NAME`
`DB_USER`
`DB_PASSWORD`

## Creating the database

Once the config file has been setup, run createadmin.py and createdb.py and follow the prompts.

# Apiary language pack

You can now change the display language for [Apiary](https://hexway.io/apiary/), using the localization files provided.

## Installation and configuration

1. Open the console of the machine, where Apiary is installed
2. Switch to the directory, where you'd like to store the localization files, e.g. `cd /opt`.
3. Get the copy of the language pack: 

    ```
    git clone git@github.com:hexway/apiary-langpack.git
    ```
4. Open the `/opt/hw-fh/config/user.ini` file using the command (root privileges required), e.g.:

    ```
    nano /opt/hw-fh/config/user.ini
    ```
5. Add the following parameter to the file and specify the path to the folder, e.g.:

    ```
    f.deck.languages.dir = /opt/apiary-langpack
    ```
6. Save the file.
7. Apply the changes by running:

    ```
    /opt/hw-fh/bin/reconfig
    ``` 
  
After that, you can switch the display language for Apiary:
* On the main login page,
* When you go to User > Profile.

## Language pack update

Language pack should be updated every time, when new Apiary version is released:

1. Login to Apiary server.
2. Switch to the directory, where the localization files are stored, e.g.:

    ```
    cd /opt/apiary-langpack
    ```
3. Run: 

    ```
    git pull
    ```

##  Translations improvement

Localization files are customizable.

If you'd like to fix and/or improve the translations provided, you can edit the corresponding .json file.

If you'd like to provide a translation for any other language, you can create a separate .json file, e.g. `it.json`, copy the field names from `en.json`, and then update the field values accordingly.

Then use GitHub to send us a pull request (PR) with your changes.

**NOTE**: 
* You can only change the values of the fields. The names of the fields cannot be adjusted and new fields cannot be added.
* You can send PRs for all .json files, except for ***en.json***. For changes in ***en.json*** only issues can be created.

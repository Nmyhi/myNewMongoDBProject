![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

Welcome,

This is the Code Institute student template for the mongo lessons. We have preinstalled all of the tools you need to get started. It's perfectly ok to use this template as the basis for your project submissions.

You can safely delete this README.md file, or change it for your own project. Please do read it at least once, though! It contains some important information about Codeanywhere and the extensions we use. Some of this information has been updated since the video content was created. The last update to this file was: **April 3rd, 2023**

## Codeanywhere Reminders

# IDE

- **Connect to Mongo CLI on a IDE**
- navigate to your MongoDB Clusters Sandbox
- click **"Connect"** button
- select **"Connect with the MongoDB shell"**
- select **"I have the mongo shell installed"**
- choose option 4.4 for : **"Select your mongo shell version"**
- choose option: **"Run your connection string in your command line"**
- `mongo "mongodb+srv://<CLUSTER-NAME>.mongodb.net/<DBname>" --username <USERNAME>`
  - replace all `<angle-bracket>` keys with your own data
- enter password *(will not echo **\*\*\*\*** *on screen)\*

#### Clear screen in Mongo Shell:

- `cls`

#### Show all database collections:

- `show collections`

To run a frontend (HTML, CSS, Javascript only) application in Codeanywhere, in the terminal, type:

`python3 -m http.server`

A button should appear to click: _Open Preview_ or _Open Browser_.

To run a backend Python file, type `python3 app.py`, if your Python file is named `app.py` of course.

A button should appear to click: _Open Preview_ or _Open Browser_.

In Codeanywhere you have superuser security privileges by default. Therefore you do not need to use the `sudo` (superuser do) command in the bash terminal in any of the lessons.

To log into the Heroku toolbelt CLI:

1. Log in to your Heroku account and go to _Account Settings_ in the menu under your avatar.
2. Scroll down to the _API Key_ and click _Reveal_
3. Copy the key
4. In Codeanywhere, from the terminal, run `heroku_config`
5. Paste in your API key when asked

You can now use the `heroku` CLI program - try running `heroku apps` to confirm it works. This API key is unique and private to you so do not share it. If you accidentally make it public then you can create a new one with _Regenerate API Key_.

---

# IDE2
- **Connect to Mongo CLI on a IDE**
- navigate to your MongoDB Clusters Sandbox
- click **"Connect"** button
- select **"Connect with the mongo shell"**
- select **"I do not have the mongo shell installed"**
- choose option: **"Run your connection string in your command line"**
- `mongo "mongodb+srv://<CLUSTER-NAME>.mongodb.net/<DBname>" --username <USERNAME>`
    - replace all `<angle-bracket>` keys with your own data
- enter password *(will not echo ******** *on screen)*


#### Clear screen in Mongo Shell:
- `cls`


#### Show all database collections:
- `show collections`


#### Assign collection to variable 'coll':
- `coll = db.collection_name`


#### Insert data to collection:
```shell
coll.insert({
    first: "john",
    last: "lennon",
    dob: "09/10/1940",
    gender: "m",
    hair_color: "brown",
    occupation: "beatle",
    nationality: "british"
});
coll.insert({
    first: "eve",
    last: "ryan",
    dob: "19/09/1992",
    gender: "f",
    hair_color: "pink",
    occupation: "developer",
    nationality: "irish"
});
coll.insert({
    first: "martha",
    last: "fenton",
    dob: "15/05/1974",
    gender: "f",
    hair_color: "brown",
    occupation: "manager",
    nationality: "irish"
});
coll.insert({
    first: "neil",
    last: "hanslem",
    dob: "14/07/1983",
    gender: "m",
    hair_color: "blonde",
    occupation: "actor",
    nationality: "british"
});
coll.insert({
    first: "rocky",
    last: "persolm",
    dob: "19/12/1994",
    gender: "f",
    hair_color: "black",
    occupation: "activist",
    nationality: "american"
});
```

#### Find all documents in collection:
- `coll.find();`


#### Find all documents with gender == "f":
- `coll.find({gender: "f"});`


#### Find all documents with gender == "f" AND nationality == "british":
- `coll.find({gender: "f", nationality: "british"});`


#### Find all documents with gender == "f" AND nationality == "american" OR "irish":
- `coll.find({gender: "f", $or: [{nationality: "american"}, {nationality: "irish"}]});`


#### Find all documents with gender == "f" AND nationality == "american" OR "irish", then sort by nationality (ascending):
- `coll.find({gender: "f", $or: [{nationality: "american"}, {nationality: "irish"}]}).sort({nationality: 1});`


#### Find all documents with gender == "f" AND nationality == "american" OR "irish", then sort by nationality (descending):
- `coll.find({gender: "f", $or: [{nationality: "american"}, {nationality: "irish"}]}).sort({nationality: -1});`


Install the shell: 

# Import the MongoDB public GPG Key
wget -qO - https://www.mongodb.org/static/pgp/server-6.0.asc | sudo apt-key add -

# Create a list file for MongoDB
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu $(lsb_release -cs)/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list

# Reload the local package database
sudo apt-get update

# Install the MongoDB shell
sudo apt-get install -y mongodb-mongosh

# Verify the installation
mongosh --version

# Connect to your MongoDB cluster
mongosh "mongodb+srv://cluster0.tyh5hdx.mongodb.net/myFirstDB" --username root
# the-weather-app-part-2

Before using this code, users will need to set up a MongoDB account and create a new cluster with a username and password. These login credentials will be needed to access the database from the code. 

To create a new cluster:

Go to the MongoDB website.
Sign up for a free account or log in to your existing account.
Click "Create a New Cluster".
Choose the provider, region, and cluster settings that suit your needs.
Click "Create Cluster" and wait for it to be provisioned.
Once the cluster has been created, you will need to create a new database and collection under the "Collections" tab in the cluster dashboard. These are the steps to create a new database:

Click the "Collections" tab in the cluster dashboard.
Click the "Add Database" button.
Give your database a name (e.g. "weatherapp").
Click "Create Database".
Click the "Add Collection" button.
Give your collection a name (e.g. "emails").
Click "Create Collection".

Once the database and collection have been created, you will need to update the following lines of code in the server.mjs file with your MongoDB login credentials and database information:
const url = 'mongodb+srv://sinjinisarkar:<password>@cluster0.p7gyjz5.mongodb.net/?retryWrites=true&w=majority';
const dbName = 'weatherapp';
const data = await db.collection('emails').find().toArray();

Replace sinjinisarkar with your MongoDB username and <password> with your MongoDB password. Replace weatherapp with the name of your database, and replace 'emails' with the name of your collection.


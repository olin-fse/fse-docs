## Week 8

### Deployment

And we're off. Today we'll be deploying the web apps that you've been working so hard on! Follow the guide \(with intentionally vague instructions\) below to successfully set up a live environment.

### Basic Deployment

1. Your database config should be in a separate config file \(eg `db.config.js`\), which will give you the info you need based on the profile you're running \(`TEST` or `DEV`\). We will now configure the `PROD` profile:  
  - Sign up for a **free tier** database service instance:
    - Postgres users: check out ElephantSQL.
    - MySQL users: check out Google Cloud MySQL.
    - Mongo users: check out MongoLab.
  - Once you have signed up for the service, update your database config for `PROD` with the relevant database URI, username, password, etc.
  - If you are using Postgres or MySQL: execute your `schema.sql` on your instance via the CLI e.g. `mysql -h [IP_ADDRESS] -u root -p < schema.sql` - this will set up your production instance with the database, user, and tables you'll need.
  - Run your app locally with the `PROD` profile and see that you successfully connect to your new database instance.

2. Sign up for a Google Cloud Platform account at [console.cloud.google.com](https://console.cloud.google.com).
1. Set up the GCP CLI `gcloud` on your machine.
3. Create a new project on GCP.
4. On the sidebar, go to Compute Engine &gt; VM instances. Spin up a brand new Ubuntu server.
6. SSH into your instance using `gcloud`.
7. Check that Git is installed. If not, [install Git](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04).
8. Install languages required to run your app:
  - [node and npm](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-16-04) (Do the PPA one)
  - [go](https://medium.com/@patdhlk/how-to-install-go-1-8-on-ubuntu-16-04-710967aa53c9)
  - elm - you're on your own
9. Set up and run your app with the `PROD` profile.
10. Discover the external IP address of your server, and access your app at \[IP\_ADDRESS\]:\[PORT\].

### Domain Name

It's no good asking people to go to 51.42.73.33:3000 to access your app - most won't remember that address. So get a domain name to go with your app:

1. Buy a domain name on Amazon/Google \(if you really like your app\), or get one for free at [freenom.com](https://freenom.com).
2. Configure the Domain Name Server \(DNS\) for your domain name. You will need to set up the Name Server \(NS\), as well as add an A-record to your domain.
3. Wait a few seconds for servers to update with the new information. Access your app using your brand new domain name!




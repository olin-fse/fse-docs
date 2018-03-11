## Week 8

### Deployment

And we're off. Today we'll be deploying the web apps that you've been working so hard on! Follow the guide \(with intentionally vague instructions\) below to successfully set up a live environment.

### Prerequisites

* [ ] [Milestone 2](https://olin-fse.gitbooks.io/fse-docs/content/assignments/milestone-2.html)
* [ ] Signed up for GCP account at [console.cloud.google.com](https://console.cloud.google.com).
* [ ] Set up the GCP CLI `gcloud` on your machine: [Mac](https://encrypted.google.com/search?hl=en&ei=tEalWrrYAs2k_QaF2L3QCg&q=gcloud+set+up+mac&oq=gcloud+set+up+mac&gs_l=psy-ab.3...4382.4716.0.6290.4.4.0.0.0.0.155.367.1j2.3.0....0...1c.1.64.psy-ab..1.2.212...0j33i22i29i30k1.0.IKICUNuvZzY), [Ubuntu](https://encrypted.google.com/search?hl=en&ei=u0alWoSqD46t_Qa5yZD4CA&q=gcloud+set+up+ubuntu&oq=gcloud+set+up+ubuntu&gs_l=psy-ab.3..0i8i13i30k1.21280.21819.0.21964.6.5.0.0.0.0.139.253.0j2.2.0....0...1c.1.64.psy-ab..4.2.252....0.kAE9WZTQqRI).
* [ ] Configure the `PROD` profile for your application, which will be active when you run your app live. Steps below:

#### `PROD` Profile 
- Sign up for a **free tier** database service instance:
  - Postgres users: check out ElephantSQL.
  - MySQL users: check out Google Cloud MySQL.
  - Mongo users: check out MongoLab.
- Once you have signed up for the service, update your database config for `PROD` with the relevant database URI, username, password, etc.
- If you are using Postgres or MySQL: execute your `schema.sql` on your instance via the CLI e.g. `mysql -h [IP_ADDRESS] -u root -p < schema.sql` - this will set up your production instance with the database, user, and tables you'll need.
- Run your app locally with the `PROD` profile and see that you successfully connect to your new database instance.



### Deployment

1. Your database config should be in a separate config file \(eg `db.config.js`\), which will give you the info you need based on the profile you're running \(`TEST` or `DEV`\). We will now 
3. Create a new project on GCP.
4. On the sidebar, go to Compute Engine &gt; VM instances. Spin up a brand new server (by default it will run Debian 9 Stretch, if you want it to run Ubuntu 16.04 or something else you will need to figure out how to do that).
6. SSH into your instance using `gcloud`.
7. On your server, check that Git is installed. If not, [install Git](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04).
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

### Nginx

But wait, it doesn't work. The domain name only points to your IP address, but your app runs on a specific port. When you go to `shawty.cf` for example, it will redirect you to http://35.196.132.69/, (implicitly, the port is 80, which the port that listens for http connections (https connections are on port 443)). Shawty-the-app runs on port 9001.

So we need something that will stand in the middle, listens for connections to port 80, and decides: "Oh, you are coming in from shawty.cf, that means I need to point you to port 9001 instead, not 80.". Enter [Nginx](https://www.nginx.com/) (pronounced engine-x by the way).

1. Install `nginx` on your server.
2. Start `nginx` with `sudo /etc/init.d/nginx start`. This command might not work for everyone, depending on your server's configuration.
3. Visit your app at the IP address alone (no port). You should see `nginx`'s welcome page. This is port 80 you're accessing.
4. Go to `nginx`'s configuration directory at `/etc/nginx/`, and briefly read through `nginx.conf`. This is the default `nginx` configuration - you don't need to understand everything, but you should probably read up on how nginx is configured. At the bottom, notice the `include` statement, which points to the directory `/etc/nginx/conf.d`. This means all config files in `/etc/nginx/conf.d` are also read to the main config file.
5. Add a new file `/etc/nginx/conf.d/[your-domain-name].conf`, and write your first nginx configuration file - we will leave this up to you to figure out.
6. Once you're done, run `sudo /etc/init.d/nginx restart` for your file to take effect. Now visit your app at the domain name you "bought", and voila.

### https

This section is under construction, as we don't think anyone will get to this point on Monday :)




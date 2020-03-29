![logo](screenshots/logo.jpgs=200)


This application perform 2 steps:

* Intercept tweets that match some pre-defined characteristics (such as location, language, topic...) and store them in a MongoDB

* From the MongoDB retrieve the corpus information of the tweet, stract the sentiment scores and send them to a PostgreSQL database where they are ready to use

In order to perform this steps, 4 Docker images are needed:

* Tweet-collector - self made

* MongoDB - oficial image

* ETL-job - self made and available in my personal Docker Hub

* PostgreSQL - oficial image




My Kubernetes dashboard with the pipeline up and running:

![Dashboard](screenshots/dashboard.png){:height="50%" width="50%"}


Summary of my namespace where you can see all the basic components and their status:

![Namespace](screenshots/namespaces.png){:height="700px" width="400px"}


Through the Kubectl I can open a command line inside the containers and intereact with the databases to check the information already stored.

MongoDB's container:

![MongoDB](screenshots/mongo_tweets.png)=250x250


Same process but here inside PostgreSQL container:

![PostgreSQL](screenshots/psql_tweets.png)



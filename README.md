# lemmy-elastic-beanstalk

# Instructions for MAC
1. Zip entire repositry content ( do not include root folder)
2. Go to AWS Console (Elastic beanstalk)
3. Create new environment
4. Select web server environment
5. Platform: Select Docker platform
6. Platform branch: Select Docker running on 64 bit Amazon Linux 2
7. Platform version: 3.4.16
8. Select Upload your code and select the zip file that was created in step 1
9. Select configure more options (Select Single instance or High availabity)
10. Edit Network , Select VPC , Check Public Ip address

# Troubleshoot beanstalk
1. Install eb cli
2. Check containers are running (Include restart : always in docker compose)
3. Check port on VPC is allowed


# Troubleshoot Lemmy
1. Try deploying locally


# Changes made
1. Added reverse proxy to docker compose


# ToDo
1. Test elastic beanstalk with ECS platform
2. Try configuring reverse proxy from beanstalk instead of deplyoing as a container from docker compose

# Notes
- Postgres volume will be created automatically (do not add postgres folder into the zipped file)
- Ensure /volumes/pictrs folder permissions are set properly
```
sudo chown -R 991:991 volumes/pictrs
```
# Coming soon template on docker for quick deployment 

![Coming Soon Template Screenshot](https://raw.githubusercontent.com/Houjeiri/docker-coming-soon/2c115eef26fadcd5d94e6604edaf7c2c0d40d60a/Coming-Soon.png)

### 3 steps to run it.
#### Add your existing domain name to nginx config
Edit /nginx/default.conf 
Change www.localhost and localhost str to your www.your-domain-name and your-domain-name
#### Build docker image
docker build -t comingsoon .
#### Run docker container
docker run -p 80:80 -v $(pwd)/app:/var/www/html -d --rm --name nginx-comingsoon comingsoon

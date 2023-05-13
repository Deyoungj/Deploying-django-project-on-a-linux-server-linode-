# Deploying django project on a linux server using (Nginx, Gunicorn and supervisor)

## this is a detailed description on how to deploy your django projects

The following image demonstrates how Django works in the production environment:

![Demonstration](https://pylessons.com/media/Tutorials/django-website/django-deployment/django_nginx_gunicorn.png)

When we enter our website in the browser, the NGINX receives the HTTP request. If the static or media file is requested, NGINX serves the file directly. Suppose a dynamic page is requested, and the NGINX delegates the request to Guniron through the UNIX socket. The resulting HTTP response is returned to NGINX, which passes it back to the client's browser. Finally, Gunicorn makes a request for Django to process. 

To complete this tutorial, you'll need a domain and hosting. For hosting like [aws](https://aws.amazon.com/), I use [lenode](https://www.linode.com/), and specifically for this tutorial, I bought a domain on the Namecheap website. Also, you can deploy it on a pure IP address without a domain while skipping the SSL security step.





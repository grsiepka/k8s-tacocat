FROM nginx
RUN mkdir /usr/share/nginx/www
COPY index.html /usr/share/nginx/www
COPY TacoCat.jpg /usr/share/nginx/www
RUN chmod -R 777 /usr/share/nginx/www
COPY nginx.conf /etc/nginx/nginx.conf

#RUN mkdir -p /var/log/app_engine

RUN mkdir -p /usr/share/nginx/www/_ah && \
    echo "healthy" > /usr/share/nginx/www/liveness_check && \
    echo "ready" > /usr/share/nginx/www/readiness_check

RUN chmod -R a+r /usr/share/nginx/www
FROM nginx:latest
ARG UNAME=user
ARG UID=1001
RUN ln -s /usr/share/nginx/html /app && \
	sed -i '/listen/s/80/8000/g' /etc/nginx/conf.d/default.conf && \
	useradd -m -u $UID -g nginx -s /bin/bash $UNAME && \
	chown -R  1001:nginx /var/cache/nginx && \
	chown -R  1001:nginx /var/log/nginx && \
	touch /var/run/nginx.pid && \
	chown -R 1001:nginx /var/run/nginx.pid
USER 1001 
EXPOSE 8000


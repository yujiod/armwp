FROM yujiod/armv7h-archlinux
RUN pacman -Syu --noconfirm
RUN pacman -S nginx --noconfirm
RUN pacman -Scc --noconfirm

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
	&& ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]

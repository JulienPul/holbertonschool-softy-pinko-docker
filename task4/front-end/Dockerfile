FROM nginx:latest

# Dossier cible demandé par l'énoncé
RUN mkdir -p /var/www/html/softy-pinko-front-end

# Copier TOUT le projet front dans ce dossier
COPY . /var/www/html/softy-pinko-front-end

# Remplacer la conf par défaut par la tienne
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Documenter le port (Nginx écoute sur 9000 via la conf)
EXPOSE 9000

# Image de base : Python 3.13 version légère
FROM python:3.13-slim

# Qui maintient cette image (remplace par ton nom)
LABEL maintainer="Djelodev iriebiange01@gmail.com"

# Installer les dépendances système nécessaires à Flask/LDAP
RUN apt update -y && apt install -y \
    python3-dev \
    libsasl2-dev \
    libldap2-dev \
    libssl-dev \
    gcc \
    build-essential

# Copier le code de l'API à la racine du container
COPY student_age.py /

# Copier le fichier des dépendances Python
COPY requirements.txt /

# Installer les packages Python (Flask, etc.)
RUN pip3 install -r /requirements.txt

# Créer le dossier /data pour stocker le fichier JSON
RUN mkdir /data
VOLUME /data

# Exposer le port 5000 (port de Flask)
EXPOSE 5000

# Commande lancée au démarrage du container
CMD ["python3", "./student_age.py"]
# FROM python:3.11-slim

# # Dossier de travail dans le conteneur
# WORKDIR /app

# # # Installer les dépendances Python (requirements.txt est à la racine du projet)
# COPY requirements.txt /app/requirements.txt
# COPY util.py util.py
# # COPY . .
# RUN pip install --no-cache-dir -r /app/requirements.txt
# CMD ["python", "-u", "app.py"]

# # Copier le code du service generator (fichiers présents dans ./generator côté host)

# # Lancer le service

FROM python:3.11-slim

# Dossier de travail dans le conteneur
WORKDIR /app/cleaner

# Installer les dépendances Python (requirements.txt est à la racine du projet)
COPY requirements.txt /app/cleaner/requirements.txt
RUN pip install --no-cache-dir -r /app/cleaner/requirements.txt

# Copier le code du service generator (fichiers présents dans ./generator côté host)
COPY app.py /app/cleaner/app.py
COPY util.py /app/cleaner/util.py

# Lancer le service
CMD ["python", "-u", "app.py"]

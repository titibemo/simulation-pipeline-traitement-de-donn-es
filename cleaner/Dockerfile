
FROM python:3.11-slim

# Dossier de travail dans le conteneur
WORKDIR /app/aggregator

# Installer les dépendances Python (requirements.txt est à la racine du projet)
COPY requirements.txt /app/aggregator/requirements.txt
RUN pip install --no-cache-dir -r /app/aggregator/requirements.txt

# Copier le code du service generator (fichiers présents dans ./generator côté host)
COPY app.py /app/aggregator/app.py
COPY util.py /app/aggregator/util.py

# Lancer le service
CMD ["python", "-u", "app.py"]

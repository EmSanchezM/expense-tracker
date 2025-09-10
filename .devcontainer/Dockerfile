FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

# Variables de entorno
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
ENV DEBIAN_FRONTEND=noninteractive

# Instalar dependencias del sistema
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    postgresql-client \
    git \
    curl \
    wget \
    vim \
    nano \
    && rm -rf /var/lib/apt/lists/*

# Copiar archivos de requirements
#COPY requirements/ requirements/

RUN pip install --upgrade pip
#RUN pip install -r requirements/dev.txt

# Crear usuario no-root
#RUN useradd --create-home --shell /bin/bash emsanchez
#RUN chown -R emsanchez:emsanchez /workspace
#USER emsanchez

# Exponer puerto
EXPOSE 8000
# 🐝 bWAPP con Docker Compose

Este repositorio contiene una orquestación de **bWAPP** (una aplicación vulnerable para pruebas de seguridad web) utilizando `Docker Compose`.

---

## 🚀 Instalación

1. Clona este repositorio:

```bash
git clone https://github.com/tu-usuario/bwapp-compose.git
cd bwapp-compose
```

2. Levanta el entorno:

```bash
docker compose up -d
```

3. Accede desde tu navegador:

```
http://localhost/install.php
```

Haz clic en **"click here to install bWAPP"** para inicializar la base de datos.

---

## 📁 Estructura del proyecto

```
bwapp-compose/
├── docker-compose.yml
├── .dockerignore
├── .gitignore
├── README.md
```

---

## 🐳 Servicios

### bWAPP

- URL: [http://localhost](http://localhost)
- Volumen: persistencia en `/var/www/html`
- Expone puerto `80`
---


## 🧼 Comandos útiles

Detener servicios:

```bash
docker compose down
```

---

## 📚 Créditos

- Imagen original de bWAPP: [https://hub.docker.com/r/davidaavilar/bwapp](https://hub.docker.com/r/davidaavilar/bwapp)

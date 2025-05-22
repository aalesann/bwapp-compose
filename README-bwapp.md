# 🐝 bWAPP con Docker Compose

Este repositorio contiene una orquestación de **bWAPP** (una aplicación vulnerable para pruebas de seguridad web) utilizando `Docker Compose`, con soporte para:

- 📦 Persistencia de archivos y configuraciones.
- 🐬 Base de datos MySQL externa y persistente.

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
http://localhost:8080/install.php
```

Haz clic en **"click here to install bWAPP"** para inicializar la base de datos.

---

## 📁 Estructura del proyecto

```
bwapp-compose/
├── docker-compose.yml
├── README.md
└── data/              # Persistencia de MySQL
    └── ...
```

---

## 🐳 Servicios

### bWAPP

- URL: [http://localhost:8080](http://localhost:8080)
- Volumen: persistencia en `/var/www/html`
- Expone puerto `8080`

### MySQL

- Host: `mysql`
- Usuario: `root`
- Contraseña: `root`
- Base de datos: `bwapp`

---

## 🧪 Tips para pentesting

- Subidas realizadas con RFI o LFI se almacenan en `/var/www/html/uploads`
- Puedes inspeccionar con:

```bash
docker exec -it bwapp bash
ls /var/www/html/uploads
```

---

## 🧼 Comandos útiles

Detener servicios:

```bash
docker compose down
```

Resetear entorno completo (incluye borrado de datos):

```bash
docker compose down -v
```

---

## 📚 Créditos

- Imagen original de bWAPP: [https://hub.docker.com/r/davidaavilar/bwapp](https://hub.docker.com/r/davidaavilar/bwapp)

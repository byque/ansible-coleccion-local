# Colección de Ansible - byque.local

[![Integración Contínua](https://github.com/byque/ansible-coleccion-local/actions/workflows/ci.yml/badge.svg)](https://github.com/byque/ansible-coleccion-local/actions/workflows/ci.yml)

## Comenzando

### Requerimientos
Python 3 y su módulo para entornos virtuales.
```sh
sudo apt install python3 python3-venv
```

### Instalación
Crear el entorno virtual.
```sh
python3 -m venv .env
```

Activar el entorno virtual.
```sh
source .venv/bin/activate
```

Instalar las dependencias.
```sh
pip install -r ./github/workflows/requerimientos.txt
```

## Distribución

### Requerimientos para cargar la colección a Galaxy

- Obtener un [token](https://galaxy.ansible.com/ui/token/) de Galaxy.
- Crear el archivo del token de Galaxy fuera del repositorio (Por defecto,
  `ansible-galaxy` revisa el directorio de inicio del usuario).
```sh
touch ~/.ansible/galaxy_token
```

- Permitir la lectura y escritura solo al usuario dueño del archivo.
```sh
chmod 600 ~/.ansible/galaxy_token
```

- Agregar el token al archivo `~/.ansible/galaxy_token`
```yaml
---
token: v@l0r
```

### Construir la colección

```sh
ansible-galaxy collection build
```

### Publicar la colección en Galaxy

```sh
ansible-galaxy collection publish byque-local-X.X.X.tar.gz
```

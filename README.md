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

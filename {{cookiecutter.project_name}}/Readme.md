# {{cookiecutter.project_name}}

## Requirements

- `python`: >= 3.6
- `docker`: 19.+

## Setup

> Run this commands inside project folder only

### Starting docker

- Whe need docker in swarm mode so run: `docker swarm init`.*This is for newbies only*.
- Now run `make run`
- **_Voilá_**. Now visit your [**Odoo site**]('https://127.0.0.1:{{cookiecutter.odoo_port}}').

### Development mode

- Create a virtual enviroment: `python -m venv .venv`
- Set the proper source: `source .venv/bin/activate` *Use the proper activate script for ou OS.*
- Install vendor package: `pip install ./vendor/odoo-14.0-py3-none-any.whl`

**Now we are ready to rush into development mode.**

The folder `addons` is ready to hold any future **Odoo module or addon** implementation.

### Useful commands

`make run` : Run the **docker stack**.

`make stop` : Stop the **docker stack**.

`make rm` : Remove docker volumes associated with this **docker stack**.

`make show` : Show **docker services** status.

`make logs` : Show **docker services** logs. 
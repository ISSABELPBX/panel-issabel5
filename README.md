```
  ___               _          _ 
 |_ _|___ ___  __ _| |__   ___| |
  | |/ __/ __|/ _` | '_ \ / _ \ |
  | |\__ \__ \ (_| | |_) |  __/ |
 |___|___/___/\__,_|_.__/ \___|_|
```

Issabel is an open source distribution and GUI for Unified Communications systems forked from Elastix&copy;

It uses the [Asterisk©](http://www.asterisk.org/ "Asterisk Home Page") open source PBX software as its core.

Panel operador
----

Control panel module for Issabel.


License
----

GPLv2 or Later

>This program is free software; you can redistribute it and/or
>modify it under the terms of the GNU General Public License
>as published by the Free Software Foundation; either version 2
>of the License, or (at your option) any later version.

>This program is distributed in the hope that it will be useful,
>but WITHOUT ANY WARRANTY; without even the implied warranty of
>MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
>GNU General Public License for more details.

>You should have received a copy of the GNU General Public License
>along with this program; if not, write to the Free Software
>Foundation, Inc., 51 Franklin Street, Fifth Floor, Bosto



 Panel-Issabel5
==========

Panel Operador opensource para Issabel 5 

Esta version de Panel operador fue actualizada para trabajar en Issabel 5, queda bajo su responsabilidad el uso de este producto.

#### Version actualizada por la comunidad de Issabel, cualquier duda o problema escribir a https://t.me/IssabelPBXip:
Gracias a la colaboracion de Julio pacheco, y comunidad de Issabel en telegram

#### Instalacion
Paso 1-  Subir carpeta "control_panel"  en la ruta /var/www/html/modules y asignar permisos usuario asterisk

Paso 2- asignar en sqlite menu y permisos 

sqlite3 /var/www/db/acl.db
INSERT INTO acl_resource (name, description) VALUES ('control_panel', 'Issabel Panel');

salir con contrl +  D

sqlite3 /var/www/db/menu.db
INSERT INTO menu (id, IdParent, Link, Name, Type, order_no) VALUES ('control_panel', 'pbxconfig', '', 'Issabel Panel', 'module', 8);

salir con contrl +  D

Paso 3- en Sistema , ir a permisos de grupo "administrador" ingresar a "pbxconfig" y asignar permisos para "control_panel"

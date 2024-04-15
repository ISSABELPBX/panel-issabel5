# panel-issabel5
Panel Operador opensource para Issabel 5 

Esta version de Panel operador fue actualizada para trabajar en Issabel 5 

*****Instalacion******
Pso 1-  Subir carpeta "control_panel"  en la ruta /var/www/html/modules y asignar permisos usuario asterisk

Paso 2- asignar en sqlite menu y permisos 

sqlite3 /var/www/db/acl.db
INSERT INTO acl_resource (name, description) VALUES ('control_panel', 'Issabel Panel');
salir con contrl +  D

sqlite3 /var/www/db/menu.db
INSERT INTO menu (id, IdParent, Link, Name, Type, order_no) VALUES ('control_panel', 'pbxconfig', '', 'Issabel Panel', 'module', 8);
salir con contrl +  D

Paso 3- en Sitema , ir a permisos de grupo "administrador" ingresar a "pbxconfig" y asignar permisos para "control_panel"

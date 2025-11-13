# SEGURIDAD_BD
Reporte de Seguridad en Base de Datos – Empresa Segura

Nombre del estudiante: Valentina Rozzo - Daniela Triana
Fecha: 13/11/2025
Materia: Base de Datos

1. Explicación de Roles de Usuario

La gestión de usuarios y sus privilegios es un componente crítico para garantizar la seguridad en la base de datos empresa_segura. A continuación se describen los roles implementados y sus funciones:

Usuario	Privilegios	Objetivo / Justificación
admin_rrhh	ALL PRIVILEGES en tabla empleados	Administrar la información de empleados, incluyendo creación, actualización y eliminación. Este usuario debe tener control completo sobre la tabla de empleados, ya que maneja datos sensibles de RRHH.
analista_bi	SELECT en todas las tablas	Permite únicamente consultas para generar reportes y análisis de información, garantizando que no pueda modificar datos críticos.
desarrollador	SELECT, INSERT, UPDATE en todas las tablas	Permite al equipo de desarrollo agregar y modificar registros necesarios para pruebas y funcionalidades sin comprometer la eliminación de información crítica.

Beneficios de esta segregación de funciones:

Minimiza riesgos de modificaciones accidentales o maliciosas.

Facilita la auditoría de acciones por usuario.

Cumple con el principio de mínimos privilegios, asignando solo lo necesario para cada rol.

2. Justificación de Políticas de Contraseñas

Se aplicaron las siguientes políticas de contraseñas en la base de datos:

Expiración periódica

Todas las contraseñas caducan cada 90 días.

Garantiza que los usuarios actualicen sus credenciales regularmente, reduciendo el riesgo de acceso prolongado en caso de que una contraseña se vea comprometida.

Contraseñas fuertes

Requieren combinación de letras mayúsculas, minúsculas, números y símbolos.

Previene ataques de fuerza bruta y mejora la seguridad de los usuarios críticos.

Bloqueo o auditoría de intentos fallidos

Aunque MySQL no bloquea automáticamente, se puede auditar intentos fallidos mediante triggers o logs de conexión.

Ayuda a detectar intentos de acceso no autorizados y responder rápidamente.

Beneficios de estas políticas:

Protegen información sensible de empleados y operaciones críticas de la empresa.

Cumplen con estándares de seguridad recomendados para bases de datos corporativas.

Complementan la segregación de funciones y el control de acceso.

Conclusión:
La combinación de roles bien definidos y políticas de contraseñas estrictas asegura que cada usuario tenga acceso limitado según sus funciones, reduciendo riesgos de pérdida de datos, accesos indebidos o errores humanos.

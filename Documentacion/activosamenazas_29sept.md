**Identificar 15 activos de SecureShop**  
    1. Catálogo  
    2. Credenciales  
    3. Información personal  
    4. Información financiera  
    5. Servidores  
    6. Información de los métodos de pago  
    7. Datos de proveedores  
    8. Código fuente  
    9. Información de procesos y logística  
    10. Información legal  
    11. Respaldos  
    12. Historial de compras  
    13. Tokens de autenticación  
    14. APIS  
    15. Registros de auditoría  
    
**Clasificar cada activo según**  
    1. *Información:* Información personal, Información financiera, Información legal, Información de procesos y logística, Información de los métodos de pago, Respaldos, Historial de Compras, Registros de auditoría.  
    2. *Software:* Código fuente  
    3. *Servicio:* APIs  
    4. *Infrestructura:* Servidores  
    5. *Datos:* Credenciales, Catálogo, Datos de proveedores, Tokens de autenticación.  
    
    
**¿Qué consecuencias tendría q este activo fuera accedido, modificado o quedara indisponible?** 


| *Activo* | *Tipo* | *Consecuencia de…* |
| --- | --- | --- |
| *Catálogo* | Datos | *Acceder:* exposición de información comercial a la competencia. *Modificar:* precios, descripciones o disponibilidad incorrectos que pueden causar pérdidas económicas. *Indisponibilidad:* los clientes no pueden consultar los productos. |
| *Credenciales* | Datos | *Acceder:* robo de cuentas y posibles accesos no autorizados. *Modificar:* pérdida de acceso a las cuentas. *Indisponibilidad:* no se puede autenticar. |
| *Información personal* | Información | *Acceder:* exposición de datos privados. *Modificar:* vulneración de la integridad de los datos. *Indisponibilidad:* dificultad para gestionar cuentas y operaciones de usuarios. |
| *Información financiera* | Información | *Acceder:* exposición de información financiera que podría generar fraudes o pérdidas económicas. *Modificar:* alteración de información financiera y posibles errores en transacciones. *Indisponibilidad:* dificultad para realizar o consultar operaciones financieras. |
| *Servidores* | Infraestructura | *Acceder:* acceso no autorizado a recursos y servicios del sistema. *Modificar:* alteración de configuraciones o recursos que puede afectar el funcionamiento. *Indisponibilidad:* interrupción de los servicios de SecureShop. |
| *Información de los métodos de pago* | Información | *Acceder:* exposición de información utilizada para realizar pagos. *Modificar:* alteración de los métodos de pago que puede provocar transacciones incorrectas. *Indisponibilidad:* dificultad para realizar compras. |
| *Datos de proveedores* | Datos | *Acceder:* exposición de información comercial de los proveedores. *Modificar:* información incorrecta que puede afectar pedidos o relaciones comerciales. *Indisponibilidad:* dificultad para gestionar proveedores y abastecimiento. |
| *Código fuente* | Software | *Acceder:* exposición de la implementación y posibles vulnerabilidades del sistema. *Modificar:* introducción de errores o código malicioso. *Indisponibilidad:* dificultad para mantener o actualizar la aplicación. |
| *Información de procesos y logística* | Información | *Acceder:* exposición de información operativa y logística. *Modificar:* alteración de procesos que puede generar retrasos o errores en entregas. *Indisponibilidad:* dificultad para gestionar pedidos y entregas. |
| *Información legal* | Información | *Acceder:* exposición de información legal y contractual. *Modificar:* alteración de documentos o información que puede generar problemas legales. *Indisponibilidad:* dificultad para consultar documentos y cumplir obligaciones legales. |
| *Respaldos*               | Información | *Acceder:* exposición de copias de información sensible. *Modificar:* respaldos corruptos o no confiables que dificulten la recuperación. *Indisponibilidad:* imposibilidad o dificultad para recuperar información ante una pérdida o incidente.                                                               |
| *Historial de compras*    | Información | *Acceder:* exposición de información sobre las compras y actividades de los clientes. *Modificar:* registros incorrectos que pueden afectar consultas, devoluciones o procesos comerciales. *Indisponibilidad:* dificultad para consultar compras anteriores, gestionar devoluciones o verificar transacciones. |
| *Tokens de autenticación* | Datos       | *Acceder:* uso no autorizado de las sesiones o cuentas asociadas. *Modificar:* acceso incorrecto o interrupción de las sesiones de los usuarios. *Indisponibilidad:* los usuarios pueden perder sus sesiones y necesitar autenticarse nuevamente.                                                               |
| *APIs*                    | Servicio    | *Acceder:* acceso no autorizado a funcionalidades o información expuesta por las APIs. *Modificar:* alteración de las operaciones o respuestas de los servicios. *Indisponibilidad:* interrupción de funcionalidades que dependen de las APIs, afectando el funcionamiento de la plataforma.                    |
| *Registros de auditoría*  | Información | *Acceder:* exposición de información sobre actividades y operaciones realizadas en el sistema. *Modificar:* pérdida de confiabilidad de los registros y dificultad para investigar incidentes. *Indisponibilidad:* dificultad para rastrear actividades, detectar incidentes o realizar auditorías.             |


**Identificar al menos 3 amenazas de cada activo.**

**Implementar al menos un mecanismo de control para cada amenaza.**


<table>
<thead><tr><th>Activo</th><th>Amenaza</th><th>Mecanismo de control</th></tr></thead>
<tbody>
<tr><td rowspan="3"><b>Catálogo</b></td><td>Extracción masiva de datos (scraping) por la competencia</td><td>Límite de peticiones (rate limiting), WAF y detección de bots</td></tr>
<tr><td>Modificación no autorizada de precios o descripciones</td><td>Control de acceso por roles y registro de cambios</td></tr>
<tr><td>Ataque DDoS que deja el catálogo inaccesible</td><td>CDN, balanceo de carga y mitigación DDoS</td></tr>
<tr><td rowspan="3"><b>Credenciales</b></td><td>Phishing para robar credenciales</td><td>Autenticación multifactor (MFA) y capacitación en seguridad</td></tr>
<tr><td>Fuerza bruta y credential stuffing</td><td>Bloqueo tras intentos fallidos, CAPTCHA y políticas de contraseñas</td></tr>
<tr><td>Filtración de la base de datos con contraseñas</td><td>Hash con sal (bcrypt/Argon2) y cifrado de la base de datos</td></tr>
<tr><td rowspan="3"><b>Información personal</b></td><td>Fuga por inyección SQL</td><td>Consultas parametrizadas y validación de entradas</td></tr>
<tr><td>Acceso indebido de personal interno</td><td>Principio de mínimo privilegio y auditoría de accesos</td></tr>
<tr><td>Interceptación o robo de datos sin cifrar</td><td>Cifrado en tránsito (TLS) y en reposo (AES-256)</td></tr>
<tr><td rowspan="3"><b>Información financiera</b></td><td>Alteración fraudulenta de registros</td><td>Segregación de funciones y control de integridad con registro de cambios</td></tr>
<tr><td>Acceso no autorizado a reportes financieros</td><td>Control de acceso basado en roles y MFA</td></tr>
<tr><td>Ransomware que cifra la información</td><td>Respaldos offline, antimalware y segmentación de red</td></tr>
<tr><td rowspan="3"><b>Servidores</b></td><td>Explotación de vulnerabilidades sin parchear</td><td>Gestión de parches y escaneo de vulnerabilidades</td></tr>
<tr><td>Acceso remoto no autorizado (SSH/RDP)</td><td>MFA, acceso por VPN y restricción por IP</td></tr>
<tr><td>Falla de hardware o ataque DDoS</td><td>Redundancia, alta disponibilidad y monitoreo</td></tr>
<tr><td rowspan="3"><b>Información de los métodos de pago</b></td><td>Robo de información de pago (por ejemplo mediante phishing)</td><td>Cifrado de datos, MFA y capacitación en seguridad al personal</td></tr>
<tr><td>Acceso no autorizado a información de métodos de pago</td><td>Control de acceso por roles (RBAC), mínimo privilegio y auditorías</td></tr>
<tr><td>Intercepciones durante transacciones o pagos</td><td>Cifrado de las comunicaciones mediante HTTPS/TLS y uso de canales seguros</td></tr>
<tr><td rowspan="3"><b>Datos de proveedores</b></td><td>Acceso no autorizado a información de proveedores</td><td>Control de acceso basado en roles y mínimo privilegio</td></tr>
<tr><td>Modificación/alteración de datos de proveedores</td><td>Control de cambios, validación de datos y auditorías</td></tr>
<tr><td>Eliminación de información</td><td>Respaldos periódicos y control de permisos</td></tr>
<tr><td rowspan="3"><b>Código fuente</b></td><td>Robo o filtración del código fuente</td><td>Control de acceso al repositorio y tener repositorios privados</td></tr>
<tr><td>Introducción de código malicioso</td><td>Revisión de código, análisis estático como con SonarQube y control de cambios</td></tr>
<tr><td>Eliminación del código fuente</td><td>Control de versiones, respaldos y protección de ramas</td></tr>
<tr><td rowspan="3"><b>Información de procesos y logística</b></td><td>Acceso no autorizado a información operativa</td><td>RBAC, mínimo privilegio y MFA</td></tr>
<tr><td>Modificación de información de pedidos o entregas</td><td>Validación de datos, control de cambios y auditoría</td></tr>
<tr><td>Interrupción del sistema de logística</td><td>Alta disponibilidad, monitoreo y sistemas de respaldo</td></tr>
<tr><td rowspan="3"><b>Información legal</b></td><td>Acceso no autorizado a contratos y documentos legales</td><td>Control de acceso por roles, cifrado, anonimización de la información y mínimo privilegio</td></tr>
<tr><td>Modificación o falsificación de documentos legales</td><td>Control de versiones, firma digital y registro de cambios</td></tr>
<tr><td>Eliminación o pérdida de documentos legales</td><td>Respaldos periódicos, almacenamiento redundante y control de versiones</td></tr>

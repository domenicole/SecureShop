1. Crear repo de GitHub
2. Identificar 10 activos de SecureShop
    1. Catalogo
    2. Credenciales
    3. Información personal
    4. Información financiera
    5. Servidores
    6. Información de los métodos de pago
    7. Datos de proveedores
    8. Código fuente
    9. Información de procesos y logística 
    10. Información legal
3. Clasificar cada activo según:
    1. Información: Información personal, Información financiera, Información legal, Información de procesos y logística, Información de los métodos de pago
    2. Sw: Código fuente
    3. Servicio
    4. Infrestructura: Servidores
    5. Datos: Credenciales, Catálogo, Datos de proveedores
4. ¿Qué consecuencias tendría q este activo fuera accedido, modificado o quedara indisponible?

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

Todo en un md en una carpeta Documentación → Activos/Amenaza/fecha
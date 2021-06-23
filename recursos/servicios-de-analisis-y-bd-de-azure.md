# Servicios de análisis y bases de datos de Azure

*Nota: todas las BD son PaaS*e

## Azure Cosmos DB

Aure Cosmos DB es un servicio de base de datos de varios modelos destribuido globalmente. **Puede escalar de forma elástica** e independiente el rendimiento y el almacenamiento en cualquier número de regiones de Azure de todo el mundo. Puede aprovechar un acceso rápido y en milisegundos de un solo digito a los datos mediante cualquiera de las diversas API populares. **Azure Cosmos DB proporciona de forma exclusiva SLA completos para garantizar el rendimiento, la latencia, la disponibilidad y la coherencia.**

**Azure Cosmos DB es compatible con los datos son esquema**, lo que permite compilar aplicaciones "Always On" con una gran capacidad de respuesta para admitir datos en continuo cambio.

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-database-fundamentals/media/azure-cosmos-db-1c115364.png)

Azure Cosmos DB es flexible. En el nivel más bajo, Azure Cosmos DB almacena los datos en formato de secuencia de registros de átomos (ARS). Después, los datos se abstraen y se proyectan como una API, que se especifica al crear la DB. Entre las opciones se incluyen SQL, MongoDB, Cassandra, Tables y Gremlin.

## Azure SQL Database

**Azure SQL Database es una base de datos relacional** basada en la última versión estable del motor de base de datos de Microsoft SQL Server. SQL Databae es una base de datos de alto rendimiento, confiable, totalmente administrada y segura. Puede usarla para compilar aplicaciones y sitios web controlados por datos en el lenguaje de programación que prefiera sin necesidad de administrar infraestrructura.

- Azure SQL Database --> PaaS
- Controla la mayoría delas funciones de administración de bases de datos, como las actualizaciones, las aplicaiones de revisiones, las copias de seguridad y la supervisión, sin intervención del usuario
- SQL Database proporciona una disponibilidad del 99,99%
- Las capacidades PaaS que están integradas en SQL Database permiten centrarse en las actividades de adminstración y optimización de bd especificas del dominio que son criticas para el negocio
- SQL Database es un servicio totlamente administrado que ofrece alta disponibilidad, copias de seguridad y otras operacioes de mantenimiento comunes.

## Azure Database for MySQL

Azure Database for MySQL es un servioc de bases de datos rlacionales en la nube, y se basa en el motor de base de datos de MySQL Community Edition.
- Azure Database for MySQL proporciona un SLA de 99,99%
- Alta disponibilad integrada son coste adicional
- REndimiento predecible y precios de pago por uso inclusivos
- Escalado según sea necesario, en cuestión de segundos
- Capacidad de protección de información confidencial en reposo y en movimiento
- Copias de seguridad automáticas
- Seguridad y cumplimiento de nivel empresarial

Permite centrarce en el desarrollo rápido de aplicaiones y en reducir el plazo de comercialización, en lugar de tener que administrar las VM y la infraestructura.

Permite migrar las bases de datos existentes de MySQL con un tiempo de inactividad mínimo mediante **Azure Database Migration Service**

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-database-fundamentals/media/azure-db-for-mysql-conceptual-diagram-02e2a10a.png)

Azure Database for MySQL ofrece varios niveles de servicio, y cada uno de ellos aporta un rendimiento y una funcionalidad diferentes para admitir cargas de trabajo de bd ligeras y pesadas.

## Azure Database for PostgreSQL

- Es un servicio de base de datos relacional en la nube.
- El software de servidor se basa en la varsión de la comunidad del motor de base de datos de PosgrateSQL de código abierto.

Azure Database PostgreSQL ofrece las siguientes ventajas:

- Alta disponibilidad integrada en comparación con los recursos locales. No hay ninguna configuración, replicación o costo adicionales que sean necesarios ára asegurarse de que las aplicacioes están siempre disponibles.
- Precios sencillos y flexibles. Tiene un rendimiento predecible en función de un plan de tarifa seleccionado que incluye copias de segurad automaticas, aplicación de revisiones de software, supervisión y seguridad.
- Escalado o reducción vertical según sea necesario, en cuestion de segundos. Puede escalar procesos o almacenamiento por separado segun sea necesario para asegurarse de que adapta su servico para que coincida con el uso.
- Copias de seguridad automáticas ajustables y restauración a un momento dado durante un máximo de 35 días.
- Seguridad y cumplimiento de nivel empresarial para proteger la información confidencial en reposo y en movimiento. Esta seguridad abarca el cifrado de datos en el disco y en el certificado SSL entre la comunicación entre cliente y servidor.

Azure Database for PostgreSQL esta disponible en dos opciones de implementación: ***Sevidor único** e **Hiperescala (Citus)**
**Servidor único**
    - Alta disponibilidad integrada son coste adicional (SLA 99,99%)
    - Rendimiento predecible y precios de pago por uso inclusivos
    - Escalado vertical según sea necesario, en cuestión de segundos.
    - Supervisión y alertas para evaluar el servidor
    - Capacidad de protección de información confidencial en reposo y en movimiento.
    - Copias de seguridad automáticas y restauración a un momento dado durante un maximo de 35 días.

**Hiperescala**

La opción de Hiperescla (Citus) escala horizontalmente  las consultas entre varias maquinas mediante el particionamiento. Su motos de consultas paraleliza las consultas SQL entrantes en estos servidores para agilizar las respuestas en cinjustos de datos grnades. Proporciona servicios a las aplicaciones que requieren mayor escalay mejor rendimiento, por lo genreal las cargas de trabajo que se aproximan a los 100 GB de datos (o que incluso los superan)

- Admite apliaciones multiinquilino,
- analisis operativos en tiempo real y
- cargas de trabajo transaccionales de alto rendimiento

Las aplicaciones compiladas para PostgreSQL pueden ejecutar consultas distrinuidas en Citus cpn las bibliotecas de conexiones estándar y unos cambios minimos.

## Azure SQL Managed Instance

Es un servico de datos en la nube que proporciona la mayor compatibilidad con el motor de bd de SQL Servercon todas las ventajas de una Paas totalmente administrado. En función de su escenario, Azure SQL Managed Instance podria ofreces mas opciones para sus necedidades de BD.

- SLA 99,99%
- Azure SQL Managed Instance facilita la migración de los datos locales en SQL Server a la nube con Azure Database Migration Service (DMS) o en copias de seguridad y restauración nativas.

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-database-fundamentals/media/migration-process-flow-small-a899c59c.png)

## Analisis y macrodatos
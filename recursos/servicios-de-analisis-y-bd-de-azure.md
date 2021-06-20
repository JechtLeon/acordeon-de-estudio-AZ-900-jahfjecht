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
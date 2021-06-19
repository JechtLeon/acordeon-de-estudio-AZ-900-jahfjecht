# Descripción de los componentes principales de la arquitectura de Azure

La **estructura organizativa de los recursos de Azure**, consta de 4 niveles: grupos de administración, suscripciones, grupos de recursos y recursos.

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/hierarchy-372fef74.png)

- **Grupos de administración**: Estos grupos le ayudan a adminstrar el acceso, las directivas (regla) y el cumplimiento de varias suscripciones. *Todas las suscripciones de un grupo de administración heredan autmáticamente las condicions que se aplican al grupo de administración*.
- **Suscripción**: Una suscripción agrupa las cuentas de usuario y los recursos que han creado esas cuentas de usuario. Para cada suscripción, hay limites o cuotas en la cantidad de recursos que se pueden crear y usar. **las organizaciones pueden usar las suscripciones para administrar los costos y los recursos creados por los usuarios, quipos o proyectos**
- **Grupo de recursos**: Los recursos se combinanen grupos de recursos, que actúan como un contenedor lógico en el que se implementan y adminstran recursos.
- **Recursos**: los recursos son instancias de servicios que puede crear, como máquinas virtuales, bases de datos SQL o almacenamiento.

## Zonas de disponibilidad, pares de regiones y regiones de Azure

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/regions-small-be724495.png)
### Regiones de Azure

Una *región* es un área geográfica del planeta que contiene al menos uncentro de datos, aunque podrían ser varios centros de datos cercanos y conectados mediante una red de baja latencia.

**Nota**: Algunos servicios o características de las máquinas virtuales solo están disponibles en determinadas regiones, como, por ejemplo, tipos de almacenamiento o tamaños de VM especificos.

Las regiones son importantes porque le dan flexibilidad necesaria para acercar las aplicaiones a los usuarios estén donde estén. Las regiones globales proporcionan una mejor escalabilidad y redundancia, y conservan la residencia de datos para los servicios.

### Regiones especiales de Azure

Azure tiene regiones especializadas ques se pueden usar al crear las aplicaiones, en lo referente al cumplimiento normativo o a aspectos legales.
- **US DoD (centro), US Gov Iowa y más**: Estas regiones son instancias físicas y logicas con el aislamiento de red de Azure para asociados y agencias de la adminstración pública de EE.UU. Estos centros de datos están operados por personal estadounidense sometidoa evaluación e incluyen certificaciones de cumplimiento adicionales.
- **Este de China, Norte de China y más**: Estas regiones están disponibles gracias a una asociación exclusiva entre Microsoft y 21Vianet, por lo cual Microsift no mantien directamente los centros de datos.

Las regiones se utilizan para identifar la ubiucación de los recursos, pero hay otros dos terminos que también debemos de conocer: *zonas geográficas y zonas de disponibilidad.*

### Zona de disponibilidad

Las zonas de disponibilidad son centros de datos separados físicamente dentro de una *región* de Azure. Cada zona de disponibilidad consta de uno o varios centros de datos aquipados con alimentación, refrigeración y redes independientes. Una zona de disponibilidd se configura para construir un *limite de aislamiento*. Si una zona deja de funcionar, la otra continua trabajando.
![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/availability-zones-5c3c490c.png)

**Nota**: no todas las regiones son compatibles con la zona de disponibilidad.

Las zonas de disponibilidad son principalmente para las máquinas virtuales, los discos adminstrados, los equilibradores de carga y las bases de datos SQL. Los servicios de Azure que adminten zonas de disponibilidad se dividen en dos categorías:

- **Servicios de zona**: ancle el recurso a una zona especifica (máquinas virtules, discos administrados, direcciones IP).
- **Servicios de redundancia de zona**: la plataforma se replica automáticamente entre zonas (almacenamiento con redundancia de zona, SQL Database).

## Pares de regiones

Cada región de Azure se empareja siempre con otra región de la misma zona geográfica que se encuentre como mínimo a 500 km de distancia. Este enfoque permite la replicación de recursos, como el almacenamientoen de la máquina virtual, en una zona geográfica, lo que ayuda a reducir la probabilidad de que se produzcan interrupciones provocadas por eventos como desastres naturales, disturbios civiles, cortes del suministro eléctrico o interrupciones de la red física que afecten de forma simultanea a ambas regiones.

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/region-pairs-d9eb9728.png)

# Autorizacon
Los grupos de recursos también son un **ámbito** para aplicar **permisos de control de acceso basado en roles (RBAC)**. Al aplicar RBAC a un grupo de recursos, puede facilitar la administración y limitar el acceso para permitir solo lo que sea necesario.
#
## Azure Resource Manager

Azure Resource Manager es el servicio de implementación y administración para Azure. Proporciona una capa de administración que le permite crear, actualizar y eliminar recursos de la cuenta de Azure. Puede usar características de administración como el control de acceso, los bloqueos y las etiquetas para proteger y organizar los recursos depués de la implementación. 

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/consistent-management-layer-feef9259.png)

Cuando un usuarios envía una solicitud de cualquiera de la herramientas, las API o los SDK de Azure, Resource Manager recibe la solitud, Autentica y autoriza la solicitud.

## Ventajas de usar Resource Manager
- Administrar la infraestructura mediante plantillas declarativas en lugar de scripts. Una plantilla de Resource Manager es un archivo JSON que define lo que quiere implementar en Azure.
- Implementar, administrar y supervisar todos los recursos de la solución en grupo, en lugar de controlarlos individualmente.
- Vuelva a implementar la solución a lo largo del ciclo de vida de dasarrollo y tenga la seguridad de que los recursos se implementan en un estado coherente.
- Definir las dependencias entre los recursos de modo que se implementen en el orden correcto.
- Aplicar control de acceso a todos los servicios, puesto que RBAC se intrega de forma nativa en la paltaforma de administración.
- Aplicar **etiqutas** a los recursos para organizar de manera lógica todos los recursos de la suscripción.
- Comprenda la *facturación* de la organización viendo los costos de un grupo que comparten la misma etiqueta.

## Suscripciones de Azure

Una suscripción de Azure es una unidad lógica de servicos de Azure que está vinculada a una cuenta de Azure, que es una *identidad* de **Azure Active Directory (Azure AD)** o en un directorio en el que confía Azure AD.

Una cuneta puede tener una suscripción o varias suscripciones que con distintos modelos de facturación y a las que se aplican diferentes *directivas* de administración de acceso. Se pueden usar las suscripciones de Azure para definir límites en torno a los productosm servicios y recursos de Azure. Hay dos tipos de limite de suscripción:
- **Límite de facturación**: Este tipo de suscripcion determina como se factura una cuenta de Azure por el uso de Azure. Puede crear varias suscripciones para diferentes tipos de requisitos de fecturación. Azure genera facturas e informes de facturación independientes para cada suscripción.
- **Límite de control de acceso**: Azure aplica las *directivas* de administración de acceso en el nivel de suscripción por lo que puede crear suscripciones independientes para reflejar distintas estructuras organizativas.

### Creación de una suscripcion de AZure adicional

Es posible que quiera crear suscripciones adicionales para fines de administración de facturación o recursos. Por ejemplo, puede optar por crear suscripciones adicionales para separar los siguiente:

- **Entonos**: cuando administra sus recursos, puede optar por crear suscripciones con el fin de configurar entornos independientes para el desarrollo y las pruebas, para seguridad o para aislar los datos por motivos de cumplimiento.
- **Estructuras organizativas**.
- **Facturación**: Dado que los costos se agregan primero en el nivel de suscripcion, es posible que quiera crear suscripciones para administrar y realizar un seguimiento de los costos en función de sus necesidades.
- **Limites de suscripción**: las suscripciones se enlazan a algunas limitaciones de hardware. Por ejemplo, el número máximo de circuitos de Azure ExpressRoute por cada suscripción es de 10. Esos límites se deben de tener en concideración al crear suscripciones en la cuenta.

### Personalización de la facturación de para satisfacer sus necesidades

Si tiene varias suscripciones, puede organizarlas en secciones de la factura. Cada sección de la factura es un elemento de línea en la facturaque muestra los cargos en los que se incurre ese mes.
En función de las necesidades, se pueden configurar varias facturas dentro de la misma cuenta de facturación. Para ello, cree perfiles de facturación adicionales. Cada perfil de facturación contiene su propia factura mensual y métod de pago.

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/billing-structure-overview-2c81a8ad.png)

### Grupos de adminstración de Azure

Si la organización tiene muchas suscripciones , es posible que necesite una forma de administrar cin eficacia el acceso, las directivas y el cumplimiento para esas suscripciones. Los grupos de admnistración de Azure ofrecen un nivel de ámbito que está por encima de las suscripciones. Las suscripciones se organizan en contenedores llamados grupos de administración y las condiciones de gobernanza se aplican a los grupos de administración. Todas las suscripciones dentro de un grupo de administración heredan automáticamente las condiciones que se aplican al grupo de Administración.

### Jerarquía de los grupos de adminstración
![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/management-groups-and-subscriptions-bba71896.png)

Hechos importantes acerca de los grupos de administración:
- Se admiten 10,000 grupos de administracipon en un único directorio.
- Un árbol de grupo de administración puede puede admitir hasta seis niveles de profundidad.*Este límite no incluye el nivel raíz ni el nivel de suscripción*.
- Cada grupo de administación y suscripción solo puede admitir un elemento primario.
- Cada grupo de administración puede tener muchos elementos secundarios.
- Todas las suscripciones y gropus de admon. están dentro de una única jerarquía en cada directorio.

## App Service
 Es un servicio basado en HTTP que permite crear y hospedar muchos tipos de soluciones basadas en la Wed sin necesidad de administrar la infraestructura.
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
- 
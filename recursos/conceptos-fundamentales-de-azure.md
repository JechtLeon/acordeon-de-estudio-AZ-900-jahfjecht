# Concepts Fundamentales de Azure

## Los distintos tipos de modelos en la nube

| Modelo de implementación | Descripción |
| :----------------------: | :---------- |
| Nube pública | Los servicios se ofrecen a través de la red de Internet pública y están disponibles para cualquiera que quiera complarlos. Los recuros de nube, como los servidores y el almacenamiento, son propiedad de un proveedor de servicios en la nube de terceros. |
| Nube privada | Una nube privada consta de recursos informáticos que determinados usuarios de una empresa u organización usan en exclusiva. |
| Nube híbrida | Una nube híbrida es un entorno informático que combina una nube pública y una nube privada, lo que permite comprtir datos y aplicaciones entre ellas. |

## Comparación entre modelos de nube

| Nube pública | Nube privada | Nube hibrida |
| :--- | :--- | :--- |
| No hay gastos de capital (CapEx) para escalar verticalmente. | Debe adquirirse hardware para el inicio y el mantenimienti. | Proporciona la máxima flexibilidad |
|Las aplicaciones pueden aprovisionarse y desaprovisionarse rápidamente|Las organizaciones tiene un control total de los recursos y la seguridad|las organizaciones determinan dódne se van a ejecutar sus aplicaciones|
|Las organizaciones solo pagan por lo que usan|Las organizaciones son responsables del mantenimiento y las actualizaciones del hardware|Las organizaciones controlan la seguridad, el cumplimiento o los requisitos legales|

## Ventajas de la informática en la nube

Los entornos en la nube ofrencen varias ventajas en comparación con los entornos físicos.

- **Alta disponibilidad**: en función del contrato de nivel de servicio (SLA) que elija, las aplicaciones basadas en la nube pueden proporcionar una experiencia de usuario continua sin un tiempo de inactividad perceptible, aunque se produzcan errores.
- **Escalabilidad**: las aplicaciones en la nube se pueden escalar *verticalmente* y *horizontalmente*:
    - Escalar *verticalmente* puede aumentar la capacidad de proceso mediante la incorporación de RAM o CPU adicionales a una máquina virtual.
    ![imange](https://www.oscarblancarteblog.com/wp-content/uploads/2017/03/escalamiento-vertical.png)
    - El escalado *horizontal* aumenta la capacidad de proceso mediante la adición de instancias de recursos, como la incorporación de máquinas virtuales a la configuración
    ![image](https://www.oscarblancarteblog.com/wp-content/uploads/2017/03/escalamiento-horizontal.png)
- **Elasticidad**: puede configurar aplicaciones basadas en la nube para aprovechar el escalado automático, de forma que las aplicaciones siempre dispondran de los recursos que necesitan.
- **Agilidad**: implemente y configure rápidamente los recursos basados en la nube a medida que cambian los requisitos de la aplicación.
- **Distribución goegráfica**: puede implementar aplicaciones y datos en centros de datos regionales de todo el mundo, lo que garantiza que sus clientes siempre tendrán el mejor rendimiento de su región.
- **Recuperación ante desastres**: al usar los servicios de copia de seguridad basados en la nube, la replicación de datos y la distribución goegráfica, podrá implementar las aplicaciones con la seguridad de saber que los datos están protegidos en caso de que se produzca un desastre.

## Comparación entre Gastos de Capital y Gastos Operativos

|Gastos de Capital (CapEx)|Gastos Operativos (OpEx)|
|-------------------------|------------------------|
|Hacen referencia a la inversión previa de dinero en la infraestructura física, que se podrá deducir a lo largo del tiempo.|Son dinero que se invierte en servicios o productos y se facturan al instante.|

## La informática en la nube es un modelo basado en el consumo

- Sin costes por adelantado.
- No es necesario comprar ni administrar infraestructuras costosas que es posible que ls usuarios no aprovechen del todo.
- Se puede pagar para obtener recursos adicionales cuando se necesiten.
- Se puede dejar de pagar por los recursos que ya no se necesiten.

## Modelos de servicios en la nube

|Modelo|Descripción|
|---|---|
|Infraestructura como servicio (Iaas) |Este modelo de servicio en la nube es el más similar a la adminstración de servidores físicos; un proveedor de servicios en la nube mantendrá actualizado el hardware, pero el mantenimiento del sistema operativo y la configuración de red serán su responsabilidad como inquilino de nube.|
|Plataforma como servicio (PaaS) |Este modelo de servicio en la nube es un entorno de hospedaje administrado. El proveedor de servicios en la nube administra las maquinas virtuales y los recursos de red, y el inquilono de nube implementa sus aplicaiones en el entorno de hospedaje administrado.|
|Software como servicio (SaaS) |En este modelo de servicio en la nube, el proveedor de servicios en la nube administra todos los aspectos del entorno de la aplicación, como las máquinas virtuales, los recursos de red, el almacenamiento de datos y las aplicaciones.|

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/fundamental-azure-concepts/media/iaas-paas-saas-575a09e9.png#lightbox)

## Comparación de los modelos de servicio en la nube

|Iaas|PaaS|SaaS|
|----|----|----|
|El servicio en la nube más flexible|Céntrense en el desarrollo de aplicaciones|Modelo de pago por uso|
|Configure y administe el hardware de la aplicaión|El proveedor de nube controla la administración de la plataforma|Los usuarios pagan por el software que utilizan en un modelo de su suscripción|

### Niveles de responsabilidad en un proveedor de servicios en la nube y un inquilino de nube

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/fundamental-azure-concepts/media/shared-responsibility-76efbc1e.png)

## Informática sin servidor

Igual que PaaS, la *informática sin servidor* permite que llos desarrolladores creen aplicaciones más rápidamente, ya que elimina la necesidad de administrar la infraestructura. En las aplicaciones sin servidor, el proveedor de servicios en la nube aprovisiona, escala y administra automaticamente la infraestructura necesaria para ejecutar el código.
En otras palabras el término *son servidor* procede del hecho de que las tareas asociadas a la administración y el aprovisionamiento de la infraestructura son invisibles para el desarrollador.
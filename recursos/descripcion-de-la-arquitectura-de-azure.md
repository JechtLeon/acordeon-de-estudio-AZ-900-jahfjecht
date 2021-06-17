# Descripción de los componentes principales de la arquitectura de Azure

La estructura organizativa de los recursos de Azure, conta de 4 niveles: grupos de administración, suscripciones, grupos de recursos y recursos.

![image](https://docs.microsoft.com/es-mx/learn/azure-fundamentals/azure-architecture-fundamentals/media/hierarchy-372fef74.png)

- **Grupos de administración**: Estos grupos le ayudan a adminstrar el acceso, las directivas (regla) y el cumplimiento de varias suscripciones. *Todas las suscripciones de un grupo de administración heredan autmáticamente las condicions que se aplican al grupo de administración*.
- **Suscripción**: Una suscripción agrupa las cuentas de usuario y los recursos que han creado esas cuentas de usuario. Para cada suscripción, hay limites o cuotas en la cantidad de recursos que se pueden crear y usar. **las organizaciones pueden usar las suscripciones para administrar los costos y los recursos creados por los usuarios, quipos o proyectos**
- **Grupo de recursos**: Los recursos se combinanen grupos de recursos, que actúan como un contenedor lógico en el que se implementan y adminstran recursos.
- **Recursos**: los recursos son instancias de servicios que puede crear, como máquinas virtuales, bases de datos SQL o almacenamiento.


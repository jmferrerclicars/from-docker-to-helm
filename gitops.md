# Principios de gitops

## Sistema descrito de forma declarativa

Permite expresar el estado al que se quiere llegar en vez de como llegar a él.

## Estado deseado versionado en git

Se usa git como fuente de verdad. Los mecanismos que proporciona git permiten cosas hacer rollbacks fácilmente con un `git revert` del entorno de producción.

## Cambios aprobados en git se pueden aplicar automáticamente

El repositorio de git debe coincidir con el estado del entorno siempre.

## Agentes para asegurar que se aplica lo anterior

En caso de que el sistema cambie respecto a git, debe haber un agente que lo devuelva al estado deseado y avise.


# Porqué usar gitops

- Permite hacer Despliegue Continuo real de tus aplicaciones
- Permite hacer rollback más fácilmente
- Acercar al mundo del desarrollo el mundo de la infraestructura
- Despliegues auto documentados en git
- El conocimiento del estado se queda en git y a través de los merge requests se distribuye por el equipo



# La idea de gitops

Tenemos una rama de un repositorio git que tiene la descripción del estado de la infraestructura.
Si quieres hacer un nuevo despliegue o modificación en la infraestructura solo necesitas actualizar el repositorio.
Existe un proceso que se asegura de que el estado del repositorio coincide con el estado de la infraestructura.
title: Vagrant, Puppet y Go
theme: jdan/cleaver-retro
author:
  name: Sebas, Jonathan

--

# Vagrant, Puppet y Go

--

### Vagrant

- Vagrant maneja ambientes de desarrollo en máquinas virtuales (y otras opciones).
- Permite unificar ambientes en un equipo: no más excusas de "en mi máquina sí sirve".

--

### ¿Cómo usamos Vagrant?

- Vagrantfile
- base boxes
- Port forwading


--

### ¿Cómo usamos Vagrant?

- `vagrant up`
- `vagrant provision`
- `vagrant reload`
- `vagrant destroy`
- `vagrant halt`
- `vagrant ssh`

Todos aceptan parámetros con el nombre de la máquina
- `vagrant ssh goserver`
- `vagrant reload goserver goagent`

--

### ¿Qué más puede hacer Vagrant?

- Carpetas sincronizadas
- Usar otros proveedores como AWS y VMWare, no solo VBox.

--

### Puppet

Puppet es aprovisionamiento de servidores y manejo de configuraciones.

--

### ¿Cómo usamos Puppet?

- Importamos `modules` con `librarian-puppet` y `Puppetfile`
- Definimos `custom-modules`
  - Paquetes y servicios necesarios
  - Archivos de configuración
  - Usuarios y grupos
  - `require`, `before`, `subscribe`, `notify`

--

### ¿Qué más puede hacer Puppet?

- Modo cliente-servidor
- Puppet Dashboard UI
- Archivos de configuración llave-valor con Hiera (*nice to have*)


--

### Go

Go es entrega continua

--

### ¿Cómo usamos Go?

- Agentes-Servidor
- Pipelines
- Stages (automáticos y manuales)
- Jobs
- Corre Ant, Maven, etc., o comandos personalizados
  + `./gradlew [tarea]`
  + `grunt [tarea]`
  + `sh [archivo]`

--

### ¿Qué más puede hacer Go?

- Environments
- Más agentes!!!
- Artifacts
- Nuevos stages
  + Separar tests de unidad de tests de integración
  + Despliegue a preproducción
  + Despliegue a producción

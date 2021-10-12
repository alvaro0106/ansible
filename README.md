# ansible
Automatizando resplados servidores
Viendo pada seccion de ansible

# Handlers
Es igual que una Tarea. Solo se va a ejecutar cuando otra tarea le llame. El usu mas comun es reiniciar un servicio cuando se cambie la configuracion

# Include y roles 
Dividir un playbook en distintas partes para fasilitar la edicion y tratado. Con **inlcude** especicicamos otro fichero que contiene playbook o una tarea.

Igual que las tareas Podemos separar los play incluir la definicin de un play en otro fichero

**Roles** Es mas Remocmendada por ser flexibles, estructura de directorio y de fichero para separar todos los elementos.
- Puede ser reutilizable
- Posible descargar roles predefinidos
- Ansible Galaxy (Repositorio de roles)

**tasks** Foler obligatprio
La practica de Include y roles se ejecuto si problemas 

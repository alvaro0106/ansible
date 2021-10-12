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

# Templates (platillas)
Forma dinamica de utilizar las variables para que le fichero sea dinamico, dentro de una plantilla see pueden espwcificar las instrucciones:

- Espreciones: {{ Variables }}
- control:  {% ... %}, un ejemplo seria una condicion:
   {% if ansible_distribution == "Debian" %}
   Montar sistema debian (solo si se cumple la condicion)
   {% endif %}
- Cometarios: comtario {# comentario #}

# Prioridad variables
- Variables de grupo definidas dentro del inventsrio
- Variables de grupo ( inventario -> grupo_vars_all -> <grupo>)
- Variables servidor (inventario -> host_vars / <servidor>)
- "Facts" del serfidor 
- Variables del play (-> vars_propt -> vars_file) 
- Variables del role (Definidas en /roles/rol/vars/main.yaml)
- Variables de bloque de tareas 
- Parametrod role -> included_pars -> include_vars
- Set_facts / register_vars
- extra_vars (!siempre ganan)

# Condiciones
-When
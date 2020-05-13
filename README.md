# postgres-k8s
fichero de definición para postgres como stateful set

# Crear el statefull set
```bash
> $ kubectl apply -f postgresql-statefull.yml
```
# Configuración usuarios
Hay que tener en cuenta que la base de datos shipments se crea porque 
así lo hemos configurado, ahora es necesario crear el usuario específico 
para la aplicación.

```bash
> $ kubectl exec -it postgres-0 -- /bin/bash
> $ su - postgres
> $ createuser --interactive --pwprompt
```
A través del comando create user se crea el usuario 
y se asigna la password, en mi caso he creado el usuario shipments.  

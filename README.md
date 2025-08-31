# encuestapp-code-mern-ECMAScript6
Proyecto CI/CD
Otros repositorios relacionados:
1. encuestapp-k8s-ECMAScript6
2. encuestapp-env-argocd-ECMAScript6



#Ultimos Cambios
encuestapp-mern-code
Modificaciones
Backend

    agregue un .env con el puerto cambiado y la base de datos tambien
    en el .env hay unos comentarios sobre las consideraciones que hay que tener con la base de datos
    en el archivo app.js hay unos ajustes comentados (el codigo anterior esta comentado tambien)
    en el bin/wwww.js esta el puerto cambiado por el del .env
    agregue un Dockerfile nuevo. Lo + importante es que el puerto EXPOSE coincida con el port del .env. Lo otro es que copia el .env en el build de la imagen

Frontend

    agregue un archivo default.conf que configura el servidor NGINX
    agregue un Dockerfile nuevo. Lo + importante es que cambia la configuracion de NGINX para que funcione nuestra app
    en el .env.production actualice la url: http://encuestapp.local.cloud/api/

K8S

    Hay un deployment para cada codigo front y back. Igual service
    La idea es que los port del dockerfile sean iguales a los targetport de los yaml
    El ingress tiene corregido los path y tiene un hostname encuestapp.local.cloud
    Para usar el hostname es la ip de tu cluster en minikube y el hostaname ej: 198.162.49.2 encuestapp.local.cloud

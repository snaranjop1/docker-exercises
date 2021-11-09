# CMD vs ENTRYPOINT

- **CMD**: Define comandos y/o parámetros predeterminados para una imagen de Docker. CMD es una instrucción que es mejor usar si se necesita un comando o parametro predeterminado que los usuarios pueden sobrescribir fácilmente, ya que se pueden sobrescribir desde el CLI de Docker cuando el contenedor se está ejecutando.

- **ENTRYPOINT**: Define comandos y/o parámetros predeterminados para una imagen de docker. Se prefiere ENTRYPOINT cuando se desea definir un ejecutable específico para un contenedor pues no se puede sobrescribir cuando los contenedores Docker se ejecutan con parámetros CLI. No es posible sobrescribir un ENTRYPOINT al iniciar un contenedor a menos que agregue --entrypoint.

Fuentes:

- [Docker Docs (ENTRYPOINT)](https://docs.docker.com/engine/reference/builder/#entrypoint)
- [Docker Docs (CMD)](https://docs.docker.com/engine/reference/builder/#cmd)

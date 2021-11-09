# COPY vs ADD

**COPY** y **ADD** son instrucciones de Dockerfile que tienen propósitos similares. Permiten copiar archivos desde una ubicación específica en el host en una imagen de Docker. A primera vista, las directivas **COPY** y **ADD** tienen el mismo aspecto y tienen la misma sintaxis. La diferencia es que **ADD** admite otras 2 fuentes. Primero, permite usar una URL en lugar de un archivo/directorio local. En segundo lugar, permite extraer un archivo tar automaticamente en el destino.

De acuerdo con la guía de mejores prácticas de Dockerfile, siempre deberíamos usar **COPY** sobre **ADD** a menos que necesitemos específicamente una de las dos características adicionales de **ADD**. Por otro lado **ADD** puede aumentar considerablemente el tamaño del contenedor por lo que se recomienda usar _wget_ o _curl_ en su lugar, pues se pueden eliminar los archivos después y no seguirán siendo una parte permanente de la imagen de Docker.

Fuentes:

- [Docker Docs (ADD)](https://docs.docker.com/engine/reference/builder/#add)
- [Docker Docs (COPY)](https://docs.docker.com/engine/reference/builder/#copy)
- [Docker Docs (Dockerfile Best Practices)](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/#add-or-copyy)

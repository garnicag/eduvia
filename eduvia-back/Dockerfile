#Creación de la imagen basada en la oficial de Node 12
FROM node:12.2.0-alpine

# Creación de un directorio donde el backend va a ser copiado
RUN mkdir -p /usr/src/app

# Cambiar directorio de trabajo para que los comandos se ejecuten desde ahí
WORKDIR /usr/src/app

# Copiar el archivo de dependencias de proyecto
COPY package.json /usr/src/app

# Instalar dependencias
RUN npm install

# Copiar el código al contenedor Docker
COPY . /usr/src/app

# Exponer el puerto de trabajo
EXPOSE 3000

# Ejecutar la aplicación
CMD ["npm", "start"]

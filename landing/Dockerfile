# Usa la imagen oficial de Node como base
FROM node:lts-alpine

RUN mkdir /app
# Establece el directorio de trabajo en /app
WORKDIR /app

# Copia el archivo package.json y yarn.lock al directorio de trabajo
COPY ./package*.json .

# Instala las dependencias del proyecto
RUN npm install

EXPOSE 7500

# Compila la aplicación Vue.js para producción
CMD ["npm", "run", "serve", "--", "--port", "7500"]

# Copia el resto de los archivos al directorio de trabajo
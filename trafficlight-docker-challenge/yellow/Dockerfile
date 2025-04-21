# 1.1.1 Imagen base
FROM node:17.0-alpine3.14

# 1.1.2 Directorio de trabajo
WORKDIR /app

# 1.1.3 Copiar los archivos de dependencias
COPY package*.json ./

# 1.1.4 Instalar npm y dependencias
RUN apk add --no-cache npm=7.17.0-r0 && npm install

# 1.1.5 Copiar el archivo principal de la app
COPY app.js .

# 1.1.6 Copiar las vistas
RUN mkdir -p /app/views
COPY index.pug favicon.ico /app/views/

# 1.1.7 Exponer el puerto 80
EXPOSE 80

# 1.1.8 Comando de ejecución
CMD ["node", "app.js"]

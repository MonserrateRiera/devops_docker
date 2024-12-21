FROM node:16

WORKDIR /app


#copy dependencies
COPY package*.json ./

# Instala las dependencias
RUN npm install

# Copia el resto del código al contenedor
COPY . .

# Construye los archivos estáticos de producción
RUN npm run build
#=http://localhost:8080 npm run build

# Instala el paquete 'serve' para servir los archivos estáticos
RUN npm install -g serve

# Expone el puerto 5000
EXPOSE 5000

# Comando para ejecutar la aplicación
CMD ["serve", "-s", "-l", "5000", "build"]






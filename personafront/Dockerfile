# Usar la imagen oficial de Node para construir la aplicación
FROM node:18 AS build
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build --prod

# Usar Nginx para servir la aplicación Angular
FROM nginx:alpine
COPY --from=build /app/dist/personafront /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

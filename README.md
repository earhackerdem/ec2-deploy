# React App con Despliegue Automatizado a AWS EC2

Este proyecto es una aplicación React con un pipeline de CI/CD configurado para desplegar automáticamente a AWS EC2 usando GitHub Actions.

## 🚀 Características

- Aplicación React básica
- Pipeline de CI/CD con GitHub Actions
- Despliegue automatizado a AWS EC2
- Pruebas automatizadas
- Configuración segura con variables de entorno

## 📋 Prerrequisitos

- Node.js 20.x
- Una cuenta de AWS
- Una instancia EC2 configurada
- GitHub Actions habilitado en tu repositorio

## 🔧 Configuración

1. **Clonar el repositorio**
   ```bash
   git clone [URL-del-repositorio]
   cd AI4Devs-DevSecOps-Extra
   ```

2. **Instalar dependencias**
   ```bash
   npm install
   ```

3. **Configurar variables de entorno**
   
   Copia el archivo `.env.example` a `.env` y configura las siguientes variables:
   - `EC2_SSH_PRIVATE_KEY`: Tu clave SSH privada para EC2
   - `AWS_ACCESS_KEY`: Tu clave de acceso AWS
   - `AWS_ACCESS_ID`: Tu ID de acceso AWS
   - `EC2_INSTANCE`: ID de tu instancia EC2
   - `EC2_USER`: Usuario de tu instancia EC2

4. **Configurar Secrets en GitHub**
   
   Añade los siguientes secrets en tu repositorio de GitHub:
   - `EC2_SSH_PRIVATE_KEY`
   - `AWS_ACCESS_KEY`
   - `AWS_ACCESS_ID`
   - `EC2_INSTANCE`
   - `EC2_USER`

## 🏃‍♂️ Desarrollo Local

1. **Iniciar el servidor de desarrollo**
   ```bash
   npm start
   ```

2. **Ejecutar pruebas**
   ```bash
   npm test
   ```

3. **Crear build de producción**
   ```bash
   npm run build
   ```

## 📦 Despliegue

El despliegue se realiza automáticamente cuando:
- Se abre un Pull Request a la rama `main`
- Se actualiza un Pull Request existente en la rama `main`

El pipeline de GitHub Actions:
1. Verifica el código
2. Instala dependencias
3. Ejecuta pruebas
4. Construye la aplicación
5. Despliega a EC2

## 🛠️ Estructura del Proyecto 
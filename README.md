# Instalación de Node.js usando NVM (Usuario `api`)

Guía paso a paso para instalar **Node.js** usando **NVM** en Debian 12 (o derivados), siguiendo exactamente los pasos indicados.

---

## 1. Crear el usuario `api`
```bash
adduser api
```

---

## 2. Cambiar al usuario `api`
```bash
su - api
```

> ⚠️ Importante usar `-` para cargar correctamente el entorno del usuario.

---

## 3. Ir al directorio HOME
```bash
cd ~
```

---

## 4. Descargar el instalador de NVM
```bash
curl -o install.sh https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh
```

---

## 5. Ejecutar el instalador
```bash
sh install.sh
```

---

## 6. Eliminar el instalador
```bash
rm install.sh
```

---

## 7. Cargar NVM en la sesión actual
```bash
source ~/.bashrc
```

> ❌ **No usar** `/home/usuario/.bashrc`  
> ✅ **Correcto:** `~/.bashrc` (usuario `api`)

---

## 8. Verificar instalación de NVM
```bash
nvm --version
```

---

## 9. Instalar Node.js (versión LTS recomendada)
```bash
nvm install --lts
```

Opcional: instalar una versión específica
```bash
nvm install 20
```

---

## 10. Usar Node por defecto
```bash
nvm use --lts
nvm alias default lts/*
```

---

## 11. Verificar Node y npm
```bash
node -v
npm -v
```

---

## ✅ Resultado
- Node.js instalado solo para el usuario `api`
- Gestión de versiones con NVM
- Ideal para APIs, PM2, Vite, React, etc.

---

## Extra (opcional): instalar PM2
```bash
npm install -g pm2
```

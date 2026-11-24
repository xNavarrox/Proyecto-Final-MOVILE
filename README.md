# Proyecto Mobile

Base de React Native con Expo y TypeScript para Android e iOS.

## Desarrollo local

En PowerShell, ejecuta estos comandos desde la raíz del proyecto.

```powershell
npm.cmd ci
if (-not (Test-Path -LiteralPath '.env')) { Copy-Item -LiteralPath '.env.example' -Destination '.env' }
npm.cmd start
```

En un emulador Android puedes usar `npm.cmd run android`. Para un simulador iOS, ejecuta `npm run ios` en macOS.

Completa `EXPO_PUBLIC_API_URL` en tu archivo `.env` cuando tengas la URL del backend. Las variables con el prefijo `EXPO_PUBLIC_` son visibles en la aplicación distribuida.

## GitFlow

- `main` contiene las versiones estables.
- `develop` integra los cambios antes de una versión.
- Las ramas `feature/*` salen de `develop` y vuelven a `develop`.
- Las ramas `release/*` salen de `develop` y se integran en `main` y `develop`.
- Las ramas `hotfix/*` salen de `main` y se integran en `main` y `develop`.

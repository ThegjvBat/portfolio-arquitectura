# Controles de seguridad

Controles implementados en la plataforma. Documentación de capacidades.

## Identidad y acceso
- **SSO con OIDC** (Microsoft Entra ID): autenticación federada, sin gestión propia
  de contraseñas.
- **Doble factor (2FA / TOTP)**.
- **RBAC**: control de acceso por roles, con privilegio mínimo.
- **Onboarding del área de IT** y modelo de roles definidos como base operativa.

## Protección de la aplicación
- **Cabeceras de seguridad y CSP** para mitigar XSS/clickjacking.
- **Rate limiting** frente a abuso y fuerza bruta.
- **Validación de entrada** y esquemas tipados en la API.
- **Gestión de secretos** fuera del código.

## Datos
- **Cifrado de credenciales** sensibles.
- **Copias de seguridad** automáticas.
- **Minimización** y segregación por entorno (PRE/PRO).

## Trazabilidad
- **Registro de auditoría** de acciones relevantes (quién, qué, cuándo).

## Integraciones
- **Acceso delegado por usuario** a SharePoint vía Microsoft Graph (no un acceso de
  aplicación amplio).
- **Residencia de datos en la UE** en el servicio de IA, con control de coste.

## Ciclo de vida / entrega
- **CI/CD** con pruebas automatizadas (**+180**) antes de desplegar.
- **Separación PRE/PRO** y **aprobación manual** del despliegue a producción
  (control de cambios).

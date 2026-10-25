# Decisiones de arquitectura

Resumen del *por qué* de cada pieza. Documentación de criterio; sin implementación.

## Principios de diseño
- **Seguridad y cumplimiento desde el diseño** (*secure by design*), no añadidos al final.
- **Automatizable y auditable**: todo lo repetitivo se automatiza y queda registrado.
- **Escalable y mantenible**: entornos separados, despliegue continuo y pruebas.
- **Residencia y soberanía del dato** en la UE por el sector regulado.

## Capa de acceso
- **SSO con OIDC (Microsoft Entra ID)** en lugar de usuarios/contraseñas propios: se
  delega la identidad en el IdP corporativo, se reduce superficie de ataque y se
  centraliza el ciclo de vida de las cuentas.
- **2FA (TOTP)** y **RBAC** para un control de acceso por rol granular.

## Aplicación
- **API en FastAPI (Python)**: rápido de desarrollar, tipado, con validación de
  esquemas y buen rendimiento asíncrono.
- **SPA en React/TypeScript**: desacoplada de la API vía tokens, con tipado estático.
- **Módulos de negocio** desacoplados (validación regulatoria, QA, informes) para
  poder evolucionar cada jurisdicción por separado.

## Datos
- Base de datos para la persistencia del dominio, con **cifrado de credenciales** y
  **copias de seguridad** automáticas.
- Minimización: solo se almacena lo necesario para la función regulatoria.

## Integraciones
- **Microsoft Graph / SharePoint** con **acceso delegado por usuario** (cada usuario
  ve solo lo suyo) en vez de un acceso de aplicación amplio.
- **Servicio de IA (LLM)** con **residencia de datos en la UE** y control de coste.
- **Correo/SMTP** para avisos automáticos de cumplimiento.

## Infraestructura y entrega
- **Docker** + **Azure Container Apps**: despliegue gestionado, escalado y menos
  operación que administrar servidores.
- **CI/CD con GitHub Actions**: integración y despliegue continuos.
- **PRE y PRO** separados, con dominios y certificados gestionados; PRO con
  aprobación manual del despliegue (control de cambios).

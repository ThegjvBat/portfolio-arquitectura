# Normativas y marcos de cumplimiento

Marcos y estándares con los que he trabajado, entre **consultoría** (Deloitte, Auren)
y **producto**. En consultoría los **implanté, adapté y audité**, y preparé
organizaciones para certificación; en producto **aplico sus principios** al diseño de
la plataforma.

> Nota: la certificación (p. ej. ISO 27001) es de la **organización**, no personal.
> Aquí describo mi **experiencia** implantando, auditando y preparando estos marcos.

## Seguridad de la información
- **ISO/IEC 27001 (SGSI)** — implantación y adaptación de controles, auditoría y
  preparación para certificación.
- **ISO 22301 (Continuidad de negocio)** — implantación y adaptación.
- **ENS (Esquema Nacional de Seguridad)** — implantación y adaptación.
- **NIST** — verificación de conformidad de aplicaciones y controles.

## Auditoría y aseguramiento
- **SOC 2** — participación en proyectos de auditoría y certificación (revisión
  documental, análisis de controles, evaluación de cumplimiento).
- **ITGC / CGTI (Controles Generales de TI)** — ejecución de auditorías,
  identificación de deficiencias y planes de remediación.

## Sector financiero
- **DORA** — adaptación de políticas de cumplimiento y evaluación de completitud
  documental bajo el marco y estándares del sector financiero.

## Protección de datos
- **RGPD / GDPR** — minimización, control de acceso y **residencia de datos en la
  UE** aplicados en la plataforma.

## Cómo se refleja en la plataforma

Los controles técnicos de la plataforma dan soporte directo a estos marcos:

| Control implementado | Da soporte a |
|---|---|
| RBAC, 2FA, SSO/OIDC | ISO 27001 (A.9 control de acceso), ENS |
| Registro de auditoría | ISO 27001 (trazabilidad), SOC 2 |
| Cifrado y copias de seguridad | ISO 27001, RGPD, ISO 22301 |
| Residencia de datos en la UE, minimización | RGPD |
| CI/CD con pruebas + control de cambios PRE/PRO | ISO 27001 (gestión de cambios) |

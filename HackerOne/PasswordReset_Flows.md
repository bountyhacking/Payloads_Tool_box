## Read the full artlicle at [InfoSecWriteups](https://infosecwriteups.com/all-about-password-reset-vulnerabilities-3bba86ffedc7)

### Password reset link not expiring
Cuando un usuario solicita cambiar la contraseña, obtiene un enlace de restablecimiento de contraseña para restablecer la contraseña, ese es el comportamiento normal, pero también debería caducar después de un período de tiempo. Si no está por vencer y puede usar el enlace de restablecimiento de contraseña varias veces para restablecer la contraseña. Entonces puedes considerarlo como vulnerabilidad.
- [HACKERONE REPORTE 685007](https://hackerone.com/reports/685007?source=post_page-----3bba86ffedc7--------------------------------)

### No rate limiting on password reset
La limitación de velocidad se utiliza para controlar la cantidad de tráfico entrante y saliente hacia o desde una red. Básicamente, sin límite de tasa significa que no existe ningún mecanismo de protección contra las solicitudes realizadas en un corto período de tiempo. Intente enviar muchas solicitudes; si no lo bloquea, puede considerarlo una vulnerabilidad.
- [HACKERONE REPORTE 838572](https://hackerone.com/reports/838572?source=post_page-----3bba86ffedc7--------------------------------)

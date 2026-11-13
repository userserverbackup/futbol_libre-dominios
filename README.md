# futbol_libre-dominios

Configuración remota de dominios para la app [futbol_libre](https://github.com/userserverbackup/futbol_libre).

La app descarga `domains.json` al iniciar (`https://raw.githubusercontent.com/userserverbackup/futbol_libre-dominios/main/domains.json`),
lo valida y lo aplica sin recompilar el APK.

## Cuando cambia el dominio

1. Edita `site.baseUrl` y `site.agendaUrl` (y `playerHosts` si cambian los reproductores).
2. **Sube `version`** en 1. La app ignora versiones menores a la que ya tiene.
3. Commit a `main`. GitHub puede tardar unos minutos en refrescar `raw.githubusercontent.com`.

Reglas: solo `https`, hosts válidos, `agendaUrl` en el mismo host que `baseUrl`.
Un JSON inválido se ignora y la app sigue con la última versión válida.

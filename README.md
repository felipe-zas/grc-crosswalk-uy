# grc-crosswalk-uy

Tabla de equivalencias entre los marcos de seguridad que suele tener que cumplir una institución financiera en Uruguay: **ISO 27001:2022**, **NIST CSF 2.0**, **AGESIC Marco de Ciberseguridad 5.0** y **BCU Estándares Mínimos de Gestión (2026)**.

## Por qué

Una fintech regulada normalmente responde a varios marcos a la vez. Evaluarlos por separado implica repetir trabajo y pedir la misma evidencia varias veces. Con un crosswalk se evalúa cada control una sola vez y se ve el impacto en todos los marcos.

## Qué hay

`data/crosswalk.csv`: 83 controles en 12 dominios (gobierno, accesos, vulnerabilidades, incidentes, proveedores, continuidad, monitoreo, desarrollo, personas, criptografía, redes y activos).

Cada fila tiene la descripción del control, su código en cada marco y la evidencia que pediría en una revisión.

| Valor | Significado |
|---|---|
| `CA.1` | Equivalente directo |
| `~GH.1` | Sin equivalente exacto, es el requisito más cercano |
| `N/A` | El marco no lo cubre |

## Cobertura

| Marco | Exactos | Parciales | Sin equivalente |
|---|---|---|---|
| AGESIC 5.0 | 71 | 11 | 1 |
| BCU EMG 2026 | 60 | 14 | 9 |

Cubre 68 de los 93 controles del Anexo A de ISO. Seguridad física (A.7) queda fuera por ahora.

## Algunas observaciones

- El EMG fija plazos concretos que ISO no: escaneo de vulnerabilidades al menos mensual (83.11) y recertificación de accesos al menos anual (63.4).
- El EMG no exige explícitamente antimalware, separación de ambientes ni acuerdos de confidencialidad. Cumplir el EMG no implica cumplir ISO.
- AGESIC no tiene un requisito de filtrado web, y para proveedores solo cubre SLA y monitoreo.

## Limitaciones

- El mapeo entre marcos es criterio profesional, no una equivalencia oficial.
- Las descripciones son propias. No se reproduce texto de ISO.
- Los códigos corresponden a las versiones indicadas arriba. Si un marco se actualiza, hay que revisar su columna.
- No constituye auditoría ni certificación.


- [ISO/IEC 27001:2022](https://www.iso.org/standard/27001)
- [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)
- [AGESIC: Marco de Ciberseguridad](https://www.gub.uy/agencia-gobierno-electronico-sociedad-informacion-conocimiento/comunicacion/publicaciones/marco-ciberseguridad)
- [BCU: Estándares Mínimos de Gestión](https://www.bcu.gub.uy/Servicios-Financieros-SSF/Paginas/Est%C3%A1ndares-M%C3%ADnimos.aspx)

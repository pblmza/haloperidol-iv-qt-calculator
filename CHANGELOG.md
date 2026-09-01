# Changelog — Calculadora Haloperidol EV

Formato basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/).
El campo **"Evidencia revisada"** marca hasta dónde llega la literatura que respalda las reglas codificadas — cualquier cambio de umbrales DEBE venir acompañado de nueva evidencia citada.

## [1.0.0] — 2026-08-31

### Evidencia revisada
- **Hasta**: 31-08-2026. Búsqueda Consensus (4 estrategias: eficacia, seguridad-QT, dosis, paliativo; 62 papers únicos con abstract completo).
- RCTs pivotales de tratamiento: Hope-ICU 2013, MIND-USA 2018, AID-ICU 2022, EuRIDICE 2023.
- Seguridad QT: Beach 2020 (SR seguridad IVH), Meyer-Massetti 2010 (70 casos post-FDA), Wang 2023 (cohorte QT severo), García 2025 (meta MACE), Stollings 2024 (monitoreo QTc), Hatta 2001, Levinsohn 2026, Lawrence 1997.
- Profilaxis: REDUCE 2018, Wang 2012. Paliativo: Agar 2016, Hui 2017/2025, Kawashima 2024.
- **Próxima revisión**: ante RCT nuevo relevante o ≤ 12 meses (ago-2027).

### Reglas codificadas (invariantes de esta versión)
- QTc basal ≥500 ms → no iniciar [Wang 2023, Beach 2020]
- ΔQTc ≥25% vs basal durante tratamiento → suspender/reducir [Lawrence 1997]
- QTc control >500 ms → suspender y repetir ECG [Wang 2023]
- K⁺ <3,0 → corregir antes de administrar; 3,0–3,4 → corregir en paralelo [Wang 2023, Meyer-Massetti 2010]
- ECG si dosis >5 mg por administración; telemetría si riesgo alto + acumulados ≥100 mg o QTc >500 ms [Beach 2020]
- Máximo diario con respaldo RCT: 20 mg/día [AID-ICU, MIND-USA]
- TdP previa → antipsicótico alternativo; EV solo sin opción y con telemetría [Meyer-Massetti 2010]

### Añadido
- Semáforo de veredicto en vivo (gris/rojo/ámbar/verde) con reglas citadas [n]→DOI.
- Flags dinámicos de QTc (Δ≥25%, >500 ms) junto al campo.
- Medidor de dosis acumulada con landmark 100 mg y máximo RCT 20 mg/d.
- Checklist adaptativo antes/durante (telemetría aparece cuando hay riesgo activo).
- Pautas exactas de los 4 RCTs pivotales como franja de referencia.
- UX móvil: barra de veredicto sticky con tap→detalle, targets ≥44px, inputs 16px (sin zoom iOS), safe-areas, botón Limpiar.
- Parser decimal coma/punto indistinto.
- Open Graph para tarjeta de preview al compartir.

### Verificación
- 5 escenarios scripted vía CDP (verde/ámbar/rojo/dinámico/sobredosis+datos faltantes) + QA visual desktop y móvil 390×844.
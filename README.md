# Calculadora Haloperidol EV — Riesgo QT/TdP

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22231704.svg)](https://doi.org/10.5281/zenodo.22231704)
[![Código: MIT](https://img.shields.io/badge/C%C3%B3digo-MIT-blue.svg)](LICENSE)
[![Contenido: CC BY 4.0](https://img.shields.io/badge/Contenido-CC%20BY%204.0-lightgrey.svg)](LICENSE-CONTENT.md)

Calculadora clínica de decisión para evaluar el riesgo de prolongación de QT / torsades de pointes antes y durante el uso de **haloperidol endovenoso** en delirium. Un solo archivo HTML, sin backend, funciona offline.

**[Abrir la calculadora](https://pblmza.github.io/haloperidol-iv-qt-calculator/)** (GitHub Pages)

## Qué hace

- **Semáforo de veredicto en vivo**: gris (sin datos) → rojo (no iniciar / suspender) → ámbar (precauciones) → verde (bajo riesgo).
- **Reglas activadas con cita**: cada regla mostrada lleva su referencia `[n]` que resuelve a un DOI en el pie — la herramienta responde "¿por qué este umbral?" sin abrir un paper.
- **Flags dinámicos de QTc**: Δ ≥25% vs basal y QTc absoluto >500 ms se marcan junto al campo, antes del veredicto.
- **Medidor de dosis acumulada** con el landmark de 100 mg (telemetría si riesgo alto, Beach 2020) y máximo diario de los RCTs (20 mg/d).
- **Checklist adaptativo** "antes / durante": genera pendientes según lo que falta (ECG basal, electrólitos, telemetría) y el riesgo activo.
- Acepta **coma o punto decimal** (3,2 = 3.2), verificado en móvil.

## Evidencia

Las reglas están trazadas a fuentes explícitas — ninguna ponderación oculta:

| Fuente | Aporte | DOI |
|---|---|---|
| Wang 2023, *Heart Rhythm* | Factores de QT severo (edad, IC, hipokalemia, amiodarona, QTc basal); 14,2% QT>500/Δ>60 | 10.1016/j.hrthm.2023.10.027 |
| Beach 2020, *Gen Hosp Psychiatry* | ECG solo >5 mg/dosis; telemetría si riesgo alto + ≥100 mg acumulados o QTc >500 | 10.1016/j.genhosppsych.2020.08.008 |
| Meyer-Massetti 2010, *J Hosp Med* | 70 casos QT/TdP post-aviso FDA 2007: 97% con factores agregados | 10.1002/jhm.691 |
| Stollings 2024, *JAMA Netw Open* | Monitoreo QTc diario aporta poco con QTc basal normal; 0 TdP en MIND-USA | 10.1001/jamanetworkopen.2023.52034 |
| García 2025, *PLOS One* | Meta 84 RCT n=12.180: sin exceso de MACE vs placebo | 10.1371/journal.pone.0326804 |
| Lawrence & Nasraway 1997 | Suspender si QTc se alarga ≥25% del basal | 10.1002/j.1875-9114.1997.tb03061.x |
| Hatta 2001 | ΔQTc correlaciona con dosis IV (r=0,48) | 10.1097/00004714-200106000-00002 |
| Levinsohn 2026, *Harv Rev Psychiatry* | Los cut-offs de QTc como criterio binario son heurístico inapropiado | 10.1097/HRP.0000000000000456 |

Contexto de eficacia: ningún RCT placebo-controlado (Hope-ICU 2013, MIND-USA 2018, AID-ICU 2022, EuRIDICE 2023) mostró que el haloperidol EV modifique el curso del delirium; su rol documentado es el control sintomático de la agitación. La calculadora asume ese marco.

## Uso

Abrir `index.html` en cualquier navegador. Sin dependencias, sin datos que salgan del dispositivo.

## Alcance y límites

Herramienta de apoyo a la decisión clínica. No constituye prescripción ni protocolo institucional; las decisiones finales corresponden al clínico tratante según el paciente y el contexto local. El veredicto integra valores **medidos** (nunca predice QTc) y factores de riesgo documentados.

## Cómo citar

> Moreira-Zabala P. *Calculadora: haloperidol endovenoso y riesgo QT/TdP.* Versión 1.0.0. Zenodo; 2026. doi:[10.5281/zenodo.22231704](https://doi.org/10.5281/zenodo.22231704)

DOI de concepto (siempre resuelve a la última versión): `10.5281/zenodo.22231704` · DOI de esta versión exacta (v1.0.0): `10.5281/zenodo.22231705`. Depósito: [zenodo.org/records/22231705](https://zenodo.org/records/22231705)

## Versiones y vigencia

**v1.0.1** · Evidencia revisada por última vez: **31-08-2026** (ver [CHANGELOG.md](CHANGELOG.md) para el detalle completo de reglas por versión). Próxima revisión sugerida: ante nuevos RCTs o ≤12 meses (ago-2027). Una herramienta que codifica umbrales envejece — revisa la versión antes de confiar en un umbral.

## Cómo citar

Moreira-Zabala P. *Calculadora: haloperidol endovenoso y riesgo QT/TdP*. Versión 1.0.0. Zenodo; 2026. [doi:10.5281/zenodo.22231704](https://doi.org/10.5281/zenodo.22231704)

Use el **DOI de concepto** (10.5281/zenodo.22231704) para referirse a la herramienta en general, y el **DOI de versión** (10.5281/zenodo.22231705 para v1.0.0) cuando importe qué reglas exactas estaban vigentes — por ejemplo, al reportar un estudio de usabilidad o de impacto decisional.

## Licencias

- **Código**: licencia MIT (ver [LICENSE](LICENSE)).
- **Contenido clínico** —reglas, umbrales, textos y síntesis de la evidencia—: [CC BY 4.0](LICENSE-CONTENT.md).

Al reutilizar o adaptar el contenido, cite la fuente y la versión, señale las modificaciones realizadas y conserve el aviso de que se trata de una herramienta de apoyo a la decisión clínica y no de una prescripción ni de un protocolo institucional.

---

**Autor:** Dr. Pablo Moreira-Zabala · Unidad de Psiquiatría de Enlace y Medicina Psicosomática, Hospital Barros Luco Trudeau

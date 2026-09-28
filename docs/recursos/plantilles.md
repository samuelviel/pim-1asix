# Plantilles

Estructures base per als lliurables. Copia-les al teu document i omplin-les: així t'assegures
de no deixar-te cap apartat que la rúbrica avalua.

!!! info "Format lliure"
    Les plantilles són **estructures**, no fitxers tancats. Pots fer-les servir en Word,
    LibreOffice, Google Docs o Markdown. El que s'avalua és el contingut.

---

## Fitxa de l'organització (UP1)

```text
DADES GENERALS
  Nom:
  Activitat:
  Sector:
  Ubicació:
  Any de constitució:
  Web:

DIMENSIÓ
  Nombre de persones:
  Llocs de treball informatitzats:
  Nombre de seus:

ESTRUCTURA
  Organigrama o descripció dels departaments:
  Qui pren les decisions tecnològiques:
  Qui porta la informàtica (intern / extern / ningú):

SITUACIÓ INFORMÀTICA ACTUAL
  Equips (quantitat, antiguitat, sistema operatiu):
  Servidors:
  Connexió a internet (tipus i velocitat):
  Xarxa (cablejada / wifi, electrònica):
  Com comparteixen fitxers:
  Còpies de seguretat:
  Programari de gestió:
  Correu electrònic:

PROBLEMES DETECTATS
  1.
  2.
  3.

FONT DE LA INFORMACIÓ
  Com he obtingut estes dades:
  Data:
```

---

## Guió d'entrevista (UP2)

```text
DADES
  Persona entrevistada:
  Càrrec:
  Data i durada:
  Lloc:

BLOC 1 · CONTEXT (preguntes obertes)
  1. Explica'm com treballeu al dia a dia amb els ordinadors.
  2. Quantes persones utilitzen equips informàtics?
  3. Què és el que més us costa o el que més us frena?

BLOC 2 · SITUACIÓ ACTUAL
  4. Com compartiu els fitxers entre vosaltres?
  5. Qui us porta la informàtica quan hi ha un problema?
  6. Feu còpies de seguretat? Com? Les heu hagut de fer servir alguna vegada?
  7. Algú treballa des de casa? Com hi accedix?

BLOC 3 · PROBLEMES
  8. Recordes l'última vegada que alguna cosa va fallar? Què va passar?
  9. Quant de temps vau estar sense poder treballar?

BLOC 4 · EXPECTATIVES
  10. Si pogueres arreglar una sola cosa, quina seria?
  11. Teniu pressupost previst per a este any?
  12. Hi ha alguna cosa que no t'haja preguntat i hauria de saber?

RESPOSTES
  [Transcripció o resum de cada resposta]

CONCLUSIONS
  Requisits que se'n deriven:
```

---

## Catàleg de requisits (UP2)

| Codi | Requisit | Tipus | Prioritat | Àmbit | Tècnica d'obtenció |
|:----:|----------|:-----:|:---------:|-------|--------------------|
| RF1 | | Funcional | Imprescindible | Xarxa | Entrevista |
| RF2 | | Funcional | Important | Servidors | Observació |
| RNF1 | | No funcional | Imprescindible | Seguretat | Anàlisi documental |

**Prioritats**: Imprescindible · Important · Desitjable
**Àmbits**: Xarxa · Servidors i serveis · Còpies · Seguretat · Disponibilitat · Accés remot · Capacitat

---

## Registre de riscos (UP3)

| Codi | Risc | Categoria | Prob. (1-5) | Imp. (1-5) | Exp. | Resposta | Pla de contingència | Responsable |
|:----:|------|-----------|:-----------:|:----------:|:----:|----------|---------------------|-------------|
| R1 | | Tècnic | | | | Mitigar | | |
| R2 | | Planificació | | | | Evitar | | |

**Categories**: Tècnic · Planificació · Econòmic · Personal · Extern · Legal
**Respostes**: Evitar · Mitigar · Transferir · Acceptar

---

## Pla d'adreçament IP (UP4)

| VLAN | Nom | Xarxa | Màscara | Porta d'enllaç | Àmbit DHCP | IP fixes | Ús |
|:----:|-----|-------|---------|----------------|------------|----------|-----|
| 10 | Gestió | 10.0.10.0 | /24 | 10.0.10.1 | — | .2–.50 | Electrònica de xarxa |
| 20 | Usuaris | 10.0.20.0 | /24 | 10.0.20.1 | .20–.199 | .2–.19 | Equips del personal |
| 30 | Servidors | 10.0.30.0 | /24 | 10.0.30.1 | — | .2–.30 | Servidor, NAS |
| 40 | Convidats | 10.0.40.0 | /24 | 10.0.40.1 | .20–.199 | — | Wifi de visitants |

---

## Traçabilitat requisit → component (UP4)

| Requisit | Component del disseny | Justificació |
|:--------:|-----------------------|--------------|
| RF1 | | |
| RF2 | | |
| RNF1 | | |

---

## Pressupost (UP4)

```text
A · INVERSIÓ INICIAL (CAPEX)

  A.1 Maquinari
      Concepte              Quantitat   Preu unitari   Total   Font del preu
      ─────────────────────────────────────────────────────────────────────

  A.2 Programari i llicències

  A.3 Serveis professionals
      Perfil                Hores       €/h            Total

  A.4 Formació

  Subtotal CAPEX:
  Contingència (10-15 %):
  TOTAL INVERSIÓ INICIAL:

B · COSTOS RECURRENTS ANUALS (OPEX)

  Concepte                  Periodicitat   Cost anual
  ─────────────────────────────────────────────────────

  TOTAL ANUAL:

C · COST TOTAL DE PROPIETAT A 5 ANYS
  CAPEX + (OPEX × 5) =

D · FINANÇAMENT
  Recursos propis:
  Ajudes i subvencions:
  Altres:
```

---

## Fitxa de procediment (UP5)

```text
CODI I NOM DEL PROCEDIMENT:

  Objectiu:
  Tasca de l'EDT associada:
  Responsable (perfil):
  Durada estimada:

  Requisits previs:
    -
  Materials i eines:
    -

  PASSOS
    1.
    2.
    3.

  VERIFICACIÓ
    Com es comprova que ha eixit bé:

  REVERSIÓ
    Com es torna arrere si falla:

  RISCOS I PRECAUCIONS
    -
```

---

## Pla de proves (UP6)

| Codi | Requisit | Descripció de la prova | Resultat esperat | Criteri d'acceptació | Tipus |
|:----:|:--------:|------------------------|------------------|----------------------|:-----:|
| PR-01 | RF1 | | | | Funcional |
| PR-02 | RNF1 | | | | Seguretat |
| PR-03 | RF7 | | | | Recuperació |

**Tipus**: Funcional · Seguretat · Rendiment · Recuperació · Acceptació

---

## Fitxa d'incidència (UP6)

```text
  Codi:                    Data i hora:
  Reportada per:
  Descripció:

  Servei afectat:          Persones afectades:
  Prioritat:               (Crítica / Alta / Mitjana / Baixa)

  Diagnòstic (què s'ha comprovat i què s'ha descartat):

  Solució aplicada:

  Causa arrel:

  Mesura preventiva:

  Hora de resolució:       Temps total:
  Verificada amb l'usuari: (Sí / No)
```

---

## Quadern de seguiment (tot el curs)

### 1 · Bitàcola setmanal

| Setmana | Què he fet | Temps | On m'he encallat |
|---------|------------|:-----:|------------------|
| | | | |

### 2 · Registre de decisions

| Data | Decisió | Alternatives valorades | Per què esta |
|------|---------|------------------------|--------------|
| | | | |

### 3 · Registre d'incidències

| Data | Incidència | Impacte | Solució | Estat |
|------|------------|---------|---------|:-----:|
| | | | | |

### 4 · Control de canvis

| Versió | Data | Què canvia | Motiu | Efecte |
|:------:|------|------------|-------|--------|
| 1.0 | | Versió inicial | — | — |

---

## Declaració d'ús d'IA (tots els lliurables)

| Eina | Per a què l'he usada | Com ho he verificat |
|------|----------------------|---------------------|
| | | |

*Si no n'has usada cap:* «No he utilitzat eines d'IA en este lliurable.»

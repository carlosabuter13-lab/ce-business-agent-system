# CE Business Agent System

Sistema multiagente empresarial para **C&E Ingenieria**, pensado para ejecutarse con un orquestador principal (CEO-Orchestrator) y subagentes especializados en ventas, marketing, web, propuestas, informes, operacion y revision tecnica de ingenieria electrica y energia solar.

---

## Objetivo

Construir una "empresa digital" con agentes de IA para C&E Ingenieria que apoye:

- **Captacion de clientes**: busqueda, prospeccion y seguimiento comercial.
- **Marketing y contenidos**: SEO, campanias, contenido web y redes sociales.
- **Pagina web**: auditoria, mejora de estructuras, copy comercial y conversion.
- **Propuestas y presupuestos**: generacion automatica de cotizaciones y propuestas tecnicas.
- **Informes y documentacion**: informes tecnicos, comerciales y administrativos.
- **Revision tecnica**: validacion de ingenieria electrica, normativa SEC/RIC y energia solar.

---

## Arquitectura General

La arquitectura es jerarquica con tres niveles:

1. **Nivel 1 - CEO Orchestadtor**: Recibe la meta, define el plan, delega tareas y consolida resultados.
2. **Nivel 2 - Directores de area**: Comercial, Marketing/Web, Operaciones y Tecnico.
3. **Nivel 3 - Ejecutores y Revisores**: Subagentes especializados en tareas concretas.

```
                      +-------------------+
                      | CEO Orchestadtor  |
                      +-------------------+
                              |
        +-----------+---------+--------+-----------+
        |           |                  |           |
+---------------+ +---------------+ +---------------+ +---------------+
| Commercial    | | Marketing &   | | Operations    | | Technical     |
| Director      | | Web Director  | | Director      | | Director      |
+---------------+ +---------------+ +---------------+ +---------------+
        |                 |                 |                 |
   [Subagents]       [Subagents]       [Subagents]       [Subagents]
```

---

## Organigrama

| Nivel | Agente | Funcion |
|-------|--------|--------|
| 1 | CEO-Orchestadtor | Recibe la meta, define plan, delega, consolida y prioriza |
| 2 | Commercial-Director | Coordina leads, seguimiento, propuestas y cierre |
| 2 | Marketing-Web-Director | Coordina contenidos, SEO, campanias y sitio web |
| 2 | Operations-Director | Coordina informes, presupuestos y administracion |
| 2 | Technical-Director | Supervisa calidad tecnica en ingenieria electrica y solar |
| 2 | QA-Supervisor | Revisa consistencia, errores y calidad antes de entregar |

---

## Subagentes

### Area Comercial (Commercial-Director)

| Agente | Funcion |
|--------|--------|
| Lead-Hunter | Busca empresas, contactos y oportunidades |
| Lead-Qualifier | Clasifica leads por potencial y urgencia |
| Outreach-Agent | Redacta contacto inicial y seguimiento |
| CRM-Logger | Registra estado y proximos pasos |
| Proposal-Agent | Genera propuestas y presupuestos |

### Area Marketing y Web (Marketing-Web-Director)

| Agente | Funcion |
|--------|--------|
| Website-Manager | Audita y mejora estructura del sitio |
| SEO-GEO-Agent | Optimiza buscadores y visibilidad |
| Content-Agent | Crea contenido web, blog y redes |
| Campaign-Agent | Disenia campanias de captacion |

### Area Operaciones (Operations-Director)

| Agente | Funcion |
|--------|--------|
| Report-Agent | Genera informes tecnicos y comerciales |
| Budget-Agent | Arma presupuestos y valida consistencia |
| Admin-Agent | Gestiona tareas internas y documentacion |
| Finance-Assistant | Controla pagos y vencimientos |

### Area Tecnico (Technical-Director)

| Agente | Funcion |
|--------|--------|
| Electrical-Reviewer | Valida servicios electricos y normativa |
| Solar-Reviewer | Revisa proyectos fotovoltaicos |
| Compliance-Agent | Verifica normativa SEC, RIC y NCh |
| Technical-Writer | Traduce tecnico a documentos claros |

---

## Flujos Principales

### 1. Captacion de Clientes

```
CEO-Orchestadtor -
  -> Commercial-Director -
    -> Lead-Hunter (busca empresas)
    -> Lead-Qualifier (clasifica)
    -> Outreach-Agent (contacta)
    -> CRM-Logger (registra)
  -> QA-Supervisor (valida)
```

### 2. Propuesta Comercial con Revision Tecnica

```
Commercial-Director recopila requerimientos -
  -> Proposal-Agent (estructura propuesta) -
    -> Budget-Agent (revisa costos) -
  -> Technical-Director activa -
    -> Electrical-Reviewer o Solar-Reviewer -
    -> Technical-Writer (documenta) -
  -> QA-Supervisor (revison final)
```

### 3. Mejora de Web y Marketing

```
Marketing-Web-Director define objetivo -
  -> Website-Manager (analiza estructura) -
  -> SEO-GEO-Agent (propone keywords) -
  -> Content-Agent (genera textos) -
  -> Campaign-Agent (conecta con captacion)
```

---

## Estructura del Repositorio

```
ce-business-agent-system/
|-- .claude/
|   |-- agents/
|   |   |-- ceo-orchestrator.md
|   |   |-- commercial-director.md
|   |   |-- marketing-web-director.md
|   |   |-- operations-director.md
|   |   |-- technical-director.md
|   |   |-- qa-supervisor.md
|   |   |-- lead-hunter.md
|   |   |-- lead-qualifier.md
|   |   |-- outreach-agent.md
|   |   |-- crm-logger.md
|   |   |-- proposal-agent.md
|   |   |-- website-manager.md
|   |   |-- seo-geo-agent.md
|   |   |-- content-agent.md
|   |   |-- campaign-agent.md
|   |   |-- report-agent.md
|   |   |-- budget-agent.md
|   |   |-- admin-agent.md
|   |   |-- finance-assistant.md
|   |   |-- electrical-reviewer.md
|   |   |-- solar-reviewer.md
|   |   |-- compliance-agent.md
|   |   -- technical-writer.md
|-- docs/
|   |-- business-context.md
|   |-- services.md
|   |-- sales-playbook.md
|   |-- website-guidelines.md
|   -- technical-standards.md
|-- templates/
|   |-- proposal-template.md
|   |-- quote-template.md
|   |-- report-template.md
|   -- followup-email-template.md
|-- CLAUDE.md
-- README.md
```

---

## Como Usar con Claude Code

1. Clona este repositorio en tu entorno local.
2. Abre el repositorio en Claude Code.
3. Cada subagente en `.claude/agents/` define un rol especializado.
4. El orquestador coordina los flujos de trabajo descritos arriba.
5. Los templates en `/templates` sirven como base para documentos comerciales.
6. La documentacion en `/docs` proporciona contexto del negocio.

---

## Estado

- [x] Repositorio creado
- [ ] Subagentes creados
- [ ] CLAUDE.md configurado
- [ ] Templates implementados
- [ ] Primer flujo de trabajo probado

---

**Empresa:** C&E Ingenieria | **Rubro:** Ingenieria Electrica, Automatizacion y Energia Solar | **Ubicacion:** Biobio, Chile

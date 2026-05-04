# C&E Business Agent System - Reglas del Sistema

## Contexto

Este repositorio contiene el sistema multiagente empresarial de **C&E Ingenieria**, empresa de ingenieria electrica, automatizacion y energia solar ubicada en Biobio, Chile. El sistema esta diseniado para ejecutarse con Claude Code u otros asistentes de IA.

## Prioridades del Sistema

### Prioridad 1 - Exactitud Tecnica
Proteger la reputacion y exactitud tecnica de C&E Ingenieria. Ningun subagente debe prometer soluciones fuera del alcance real de la empresa.

### Prioridad 2 - Enfoque Comercial
Toda propuesta, contenido o documento debe estar orientado a captar clientes y mover la empresa hacia adelante.

### Prioridad 3 - Idioma
El idioma principal del negocio y de todas las salidas es **espaniol chileno**.

### Prioridad 4 - Control de Calidad
Toda salida importante debe pasar por QA-Supervisor antes de entregarse al cliente.

### Prioridad 5 - Verificacion Tecnica
Los subagentes tecnicos (Electrical-Reviewer, Solar-Reviewer, Compliance-Agent) deben validar cualquier propuesta o contenido que mencione servicios de ingenieria.

## Reglas de Orquestacion

1. El CEO-Orchestadtor decide que agentes se activan y en que orden.
2. Los Directores de area coordinan sus subagentes y reportan al CEO.
3. El QA-Supervisor tiene la ultima palabra antes de cualquier entrega.
4. Cuando hay duda sobre alcance tecnico, el Technical-Director decide.
5. Los flows descritos en README.md son la referencia para ejecutar tareas.

## Servicios de C&E Ingenieria

- Ingenieria electrica (disenio, instalacion, mantencion)
- Instrumentacion y control industrial
- Automatizacion industrial
- Eficiencia energetica
- Energia solar fotovoltaica (proyectos, monitoreo, mantencion)
- Cumplimiento normativo (SEC, RIC, NCh)

## Normativa Aplicable

- Reglamento Electrico SEC (Chile)
- Normas RIC (Requisitos de Instalaciones de Consumo)
- Normas NCh aplicables
- Reglamentos de eficiencia energetica

## Domain Knowledge

### Ingenieria Electrica
Sistemas de baja y media tension, tableros electricos, protecciones, tierra fisca,@parametros de diseño, calculo de conductores.

### Energia Solar
Sistemas fotovoltaicos de autoconsumo, monitoreo con Fusion Solar, mantencion preventiva y correctiva de plantas solares.

### Automatizacion
PLC, SCADA, instrumentacion industrial, redes de comunicacion industrial.

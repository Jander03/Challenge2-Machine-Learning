graph TD
    classDef inicial fill:#f9d0c4,stroke:#e74c3c,stroke-width:2px;
    classDef objetivo fill:#d5f5e3,stroke:#2ecc71,stroke-width:2px;
    classDef accion fill:#d6eaf8,stroke:#3498db,stroke-width:2px;
    classDef restriccion fill:#fcf3cf,stroke:#f1c40f,stroke-width:2px;

    A["<b>ESTADO INICIAL</b><br>824,978 casos IRA, 51 defunciones<br>Recursos logísticos centralizados"]:::inicial
    
    A -->|Evaluación de heurística| B{"<b>OPERADORES (Acciones)</b>"}
    
    B --> C["Distribuir 2.22M vacunas<br>a regiones críticas"]:::accion
    B --> D["Ejecutar campañas<br>preventivas (Abrigamos Vidas)"]:::accion
    
    R["<b>RESTRICCIONES</b><br>Stock finito de vacunas<br>Capacidad logística limitada"]:::restriccion -.-> B
    
    C --> E["<b>ESTADO OBJETIVO</b><br>Asignación óptima de recursos<br>Reducción de episodios IRA<br>Cero defunciones prevenibles"]:::objetivo
    D --> E

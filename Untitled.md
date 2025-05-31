# Data Flow Diagrams for Lazy Programmers (Gane & Sarson)

Here's the ultra-concise guide to creating Gane & Sarson DFDs in Obsidian Markdown:

## Basic Elements

```mermaid
flowchart TD
    process["Process
    --------
    Description"]:::process
    
    entity[("External Entity")]:::entity
    
    store["Data Store"]:::store
    
    process -->|Data Flow| store
    entity -->|Data Flow| process
    
    classDef process fill:#ececff,stroke:#9370db,stroke-width:2px
    classDef entity fill:#ececec,stroke:#555,stroke-width:2px
    classDef store fill:#ffffec,stroke:#555,stroke-width:2px,stroke-dasharray: 5 5
```

## Steps to Create

1. Use Obsidian with Mermaid plugin enabled
2. Create a mermaid code block with `flowchart TD` (top-down) directive
3. Define elements using standard Gane & Sarson symbols:
    - Process: Rectangle with rounded corners
    - External Entity: Rectangle or circle
    - Data Store: Open-ended rectangle
    - Data Flow: Arrow with label
4. Style with classes to match Gane & Sarson conventions
5. Maintain hierarchy with levels (DFD0, DFD1, etc.)

## Example for Context Diagram (DFD0)

```mermaid
flowchart TD
    customer[("Customer")]:::entity
    system["Order System
    --------
    Process Orders"]:::process
    inventory[("Inventory\nSystem")]:::entity
    billing[("Billing\nSystem")]:::entity
    
    customer -->|Order| system
    system -->|Inventory Check| inventory
    inventory -->|Availability| system
    system -->|Billing Info| billing
    billing -->|Payment Status| system
    system -->|Order Status| customer
    
    classDef entity fill:#ececec,stroke:#555,stroke-width:2px
    classDef process fill:#ececff,stroke:#9370db,stroke-width:2px
```

That's it! Just copy these patterns and customize for your system.
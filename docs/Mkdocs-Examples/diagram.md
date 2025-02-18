# Diagram Examples

## Types of Diagrams

### Flowcharts

Used to represent workflows or processes. The steps
are rendered as nodes of various kinds and are connected by edges, describing
the necessary order of steps:

```` markdown title="Example Code"
```mermaid

graph LR
    A[start] --> B{failure?};
    B -->|Yes| C[Investigate...];
    C --> D[Debug];
    D --> B;
    B ---->|No| E[Success!];
```
````

<div class="result" markdown>
Result
```mermaid

graph LR
    A[start] --> B{failure?};
    B -->|Yes| C[Investigate...];
    C --> D[Debug];
    D --> B;
    B ---->|No| E[Success!];
```

</div>

### Sequence diagrams

Are used to describe a specific scenario as sequential interactions 
between multiple objects or actors, including the messages that are exchanged
between those actors:

```` markdown title="Example Code"
```mermaid
sequenceDiagram
    autonumber
    Server->>Terminal: Send request
    loop Health
        Terminal->>Terminal: Check for health
    end
    Note right of Terminal: System online
    Terminal-->>Server: Everything is OK
    Terminal-->>Database: Request customer data
    Database-->>Terminal: Customer data
```
````

<div class="result" markdown>
Result
```mermaid
sequenceDiagram
    autonumber
    Server->>Terminal: Send request
    loop Health
        Terminal->>Terminal: Check for health
    end
    Note right of Terminal: System online
    Terminal-->>Server: Everything is OK
    Terminal-->>Database: Request customer data
    Database-->>Terminal: Customer data
```

</div>
```mermaid
flowchart TD
    A[Start Day] -->|Wake Up| B[Morning Grazing]
    B -->|Assess Thirst| C[Search for Water Source]

    C -->|Detect Water Scents| D{Move Toward Water}
    D -->|Water Nearby (Distance < 100m)| E[Drink Water]
    D -->|No Water Detected| Q[Wandering for New Water]



```
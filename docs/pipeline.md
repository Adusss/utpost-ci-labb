flowchart LR
B[branch + commit] --> PR[pull request]
PR --> Q[Kvalitet: lint · format · test - 15s]
PR --> BU[Bygg - 16s]
Q --> S{gröna?}
BU --> S
S -->|ja| M[merge]
S -->|nej| F[fixa, pusha igen]

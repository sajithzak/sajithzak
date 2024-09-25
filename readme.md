## Platform Strategy Diagram

```mermaid
graph TD;
    A[Current Platform] -->|Migrate| B[Target Platform]
    subgraph Current Platform
        C1[OpenShift]
        C2[Bitbucket]
        C3[Jenkins]
    end
    subgraph Target Platform
        T1[GCP GKE]
        T2[GitHub]
        T3[GitHub Actions]
    end
    subgraph CI/CD
        C3 -->|CI/CD| T3
    end
    subgraph GCP Platform
        C1 -->|Container Orchestration| T1
        C2 -->|Source Code Management| T2
    end

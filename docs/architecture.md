# System Architecture Design

## 1. Overview
The Adaptive Denoising Framework is designed as a **layered architecture** to separate algorithmic logic from system management. This ensures that the code is maintainable, testable, and scalable.

## 2. Layer Diagram

```mermaid
graph TD
    User[User / Script] --> API[Main Entry (main.py)]
    API --> Pipeline[Pipeline Layer]
    
    subgraph Pipeline Layer
        Adaptive[Adaptive Selector] --> |Selects| Mode{Mode}
        Mode --> |Quality| Q[Quality Pipeline]
        Mode --> |Speed| S[Speed Pipeline]
    end
    
    subgraph Core Layer
        Q --> Feat[Feature Extractor]
        S --> Feat
        Q --> Clust[Clustering]
        Feat --> Restore[Pixel Restorer]
        Clust --> Restore
    end
    
    subgraph Infrastructure Layer
        Restore --> Mem[Memory Manager]
        Feat --> Cache[Smart Cache]
        API --> Exp[Experiment Manager]
    end

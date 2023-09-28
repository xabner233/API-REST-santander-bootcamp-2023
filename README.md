# API REST Santander Bootcamp 2023

## Diagrama de Classes

```mermaid
classDiagram
  class Usuario {
    - name: String
    - account: Conta
    - features: List<Feature>
    - card: Cartao
    - news: List<Noticia>
  }
  class Conta {
    - number: String
    - agency: String
    - balance: Double
    - limit: Double
  }
  class Feature {
    - icon: String
    - description: String
  }
  class Cartao {
    - number: String
    - limit: Double
  }
  class Noticia {
    - icon: String
    - description: String
  }

  Usuario "1" *-- "1" Conta 
  Usuario "1" *-- "N" Feature 
  Usuario "1" *-- "1" Cartao 
  Usuario "1" *-- "N" Noticia 

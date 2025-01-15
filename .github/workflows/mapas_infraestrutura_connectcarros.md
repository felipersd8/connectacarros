
```mermaid
graph TD
    A[ConnectCarros] --> B[Backend]
    B --> B1[Linguagem: Python]
    B1 --> B1a[Framework: Django]
    B --> B2[Banco de Dados: PostgreSQL]
    B2 --> B2a[ORM: Django ORM]
    B --> B3[Autenticação: Keycloak]
    B3 --> B3a[OAuth2, SSO, 2FA]
    B --> B4[Integrações]
    B4 --> B4a[APIs externas (OLX, Mercado Livre, etc.)]
    B4 --> B4b[ManyChat (WhatsApp)]
    B4 --> B4c[SendGrid (E-mail)]
    B --> B5[Testes: Pytest]
    B --> B6[Dockerfile]
    
    A --> C[Frontend]
    C --> C1[Web: Bootstrap]
    C --> C2[App: React.js]
    C --> C3[REST/GraphQL]
    C --> C4[Testes: Cypress]
    C --> C5[Dockerfile]
    
    A --> D[Infraestrutura de DevOps]
    D --> D1[Gerenciamento de Código: Git + GitHub/GitLab]
    D --> D2[CI/CD: GitHub Actions ou GitLab CI]
    D2 --> D2a[Testes automatizados]
    D2 --> D2b[Build de imagens Docker]
    D2 --> D2c[Deploy automático]
    D --> D3[Configuração Local: Docker Compose]
    D3 --> D3a[Serviços: backend, frontend, banco, Keycloak]
    D3 --> D3b[Rede interna: connectcarros-network]

    A --> E[Documentação]
    E --> E1[Descrição do MVP e roadmap]
    E --> E2[Guia de APIs]
    E --> E3[Modelagem de dados (ERD)]
    E --> E4[Tutorial de setup local]

    subgraph Infraestrutura de Sistemas
        F[Hospedagem]
        F --> F1[Desenvolvimento: VPS na Hostinger]
        F1 --> F1a[Ubuntu 22.04 LTS]
        F --> F2[Produção: GCP ou AWS]
        F2 --> F2a[Compute Engine (EC2)]
        F2 --> F2b[Cloud SQL (PostgreSQL)]
        F2 --> F2c[Cloud Storage]

        G[Containerização e Orquestração]
        G --> G1[Docker: backend, frontend, banco, Keycloak]
        G --> G2[Portainer com Docker Swarm]
        G --> G3[Traefik como Load Balancer]

        H[Monitoramento e Logs]
        H --> H1[ELK Stack]
        H --> H2[Prometheus e Grafana]
        H --> H3[Alertas no Grafana]
        H --> H4[Sentry para monitoramento de erros]

        I[Segurança]
        I --> I1[HTTPS: Let’s Encrypt]
        I --> I2[Firewall configurado na nuvem]
        I --> I3[Backup: banco de dados e volumes Docker]

        J[Recursos de Servidor]
        J --> J1[32 GB de RAM]
        J --> J2[8 vCPUs]
        J --> J3[400 GB SSD]
        J --> J4[Ubuntu 22.04 LTS]

        K[Serviços Adicionais]
        K --> K1[Redis para cache]
        K --> K2[CDN para conteúdos estáticos]
        K --> K3[Load balancer integrado ao Kubernetes]
    end
```

# E-COMMERCE FARMÁCIA - ESPECIFICAÇÃO COMPLETA


## 🎯 Visão Geral do Projeto

### Propósito
Desenvolvimento de um e-commerce farmacêutico completo, destinado a demonstrar competências técnicas em desenvolvimento fullstack, com foco em:
- Arquitetura robusta e escalável
- Implementação de padrões de projeto
- Compliance com regulamentações brasileiras
- Interface moderna e responsiva

---

## 🎯 Objetivos e Metas

### Objetivos Técnicos
- Demonstrar domínio completo da stack Java/Spring Boot 
- Implementar padrões de arquitetura Clean Architecture
- Criar pipeline CI/CD completo
- Desenvolver sistema de alta disponibilidade

### Objetivos de Negócio
- Simular operação real de e-commerce farmacêutico
- Atender regulamentações específicas do setor
- Proporcionar experiência de usuário superior

### Metas de Portfólio
- Código limpo e bem documentado
- Cobertura de testes > 80%
- Performance otimizada
- Deploy automatizado

---

## 🛠️ Stack Tecnológica

### Backend
- **Linguagem**: Java 17+
- **Framework**: Spring Boot 3.x
- **Banco de Dados**: PostgreSQL 15+
- **ORM**: Spring Data JPA / Hibernate
- **Segurança**: Spring Security 6
- **Documentação**: Swagger/OpenAPI 3
- **Testes**: JUnit 5, Mockito, TestContainers

### DevOps & Infraestrutura
- **Containerização**: Docker + Docker Compose
- **CI/CD**: GitHub Actions
- **Cloud**: AWS (EC2, RDS, S3, CloudFront)
- **Monitoramento**: Prometheus + Grafana
- **Logs**: ELK Stack

### Ferramentas de Desenvolvimento
- **Build**: Maven (Backend) + Vite (Frontend)
- **Versionamento**: Git + GitHub
- **IDE**: IntelliJ IDEA / VSCode
- **Qualidade**: SonarQube, ESLint, Prettier

---

## 🏗️ Arquitetura do Sistema

### Padrões Arquiteturais
- **Clean Architecture**: Separação clara de responsabilidades
- **Hexagonal Architecture**: Portas e adaptadores
- **CQRS**: Separação de comandos e consultas
- **Event-Driven**: Eventos de domínio

### Estrutura de Camadas

#### Backend (Spring Boot)
```
src/
├── main/
│   ├── java/
│   │   └── com/
│   │       └── pharmacy/
│   │           ├── application/       # Casos de uso
│   │           ├── domain/            # Entidades e regras
│   │           ├── infrastructure/    # Adaptadores
│   │           └── presentation/      # Controllers
│   └── resources/
│       ├── application.yml
│       └── db/migration/
└── test/
```
---

## ⚙️ Requisitos Funcionais

### RF001 - Gestão de Usuários
- **Descrição**: Sistema completo de autenticação e autorização
- **Funcionalidades**:
  - Cadastro de usuários (clientes, farmacêuticos, administradores)
  - Login/logout com JWT
  - Recuperação de senha
  - Perfil de usuário
  - Múltiplos endereços por usuário
  - Verificação de email

### RF002 - Catálogo de Produtos
- **Descrição**: Gestão completa do catálogo farmacêutico
- **Funcionalidades**:
  - CRUD de produtos
  - Categorias hierárquicas
  - Múltiplas imagens por produto
  - Classificação por tipo (medicamento, cosmético, etc.)
  - Controle de medicamentos (A1, A2, B1, etc.)
  - Busca avançada com filtros
  - Busca por princípio ativo

### RF003 - Controle de Estoque
- **Descrição**: Gestão de inventário com controle de lotes
- **Funcionalidades**:
  - Controle de lotes e validades
  - Reserva de produtos
  - Alertas de estoque baixo
  - Relatórios de movimento
  - Rastreabilidade completa

### RF004 - Sistema de Receitas
- **Descrição**: Gestão de receitas médicas digitais
- **Funcionalidades**:
  - Upload de receitas (imagem/PDF)
  - Validação por farmacêutico
  - Controle de validade
  - Histórico de uso
  - Integração com pedidos

### RF005 - Carrinho e Checkout
- **Descrição**: Processo completo de compra
- **Funcionalidades**:
  - Carrinho persistente
  - Cálculo de frete
  - Aplicação de cupons
  - Múltiplas formas de pagamento
  - Confirmação de pedido

### RF006 - Gestão de Pedidos
- **Descrição**: Controle completo do ciclo de vida dos pedidos
- **Funcionalidades**:
  - Status em tempo real
  - Histórico de pedidos
  - Cancelamento de pedidos
  - Reembolsos
  - Notas fiscais

### RF007 - Sistema de Pagamentos
- **Descrição**: Integração com gateways de pagamento
- **Funcionalidades**:
  - Cartão de crédito/débito
  - PIX
  - Boleto bancário
  - Parcelamento
  - Controle de fraudes

### RF008 - Logística e Entregas
- **Descrição**: Gestão de entregas e retiradas
- **Funcionalidades**:
  - Cálculo de frete
  - Rastreamento de entregas
  - Agendamento de retirada
  - Integração com transportadoras
  - Confirmação de entrega

### RF009 - Painel Administrativo
- **Descrição**: Interface para gestão do sistema
- **Funcionalidades**:
  - Dashboard com métricas
  - Gestão de usuários
  - Gestão de produtos
  - Relatórios financeiros
  - Configurações do sistema

### RF010 - Auditoria e Logs
- **Descrição**: Rastreamento completo de operações
- **Funcionalidades**:
  - Log de todas as operações
  - Auditoria de alterações
  - Relatórios de conformidade
  - Backup e restauração

---

## 🔧 Requisitos Não-Funcionais

### RNF001 - Performance
- **Tempo de resposta**: < 2 segundos para 95% das requisições
- **Throughput**: Suportar 1000 usuários simultâneos
- **Disponibilidade**: 99.9% uptime
- **Escalabilidade**: Arquitetura horizontal

### RNF002 - Segurança
- **Autenticação**: JWT com refresh tokens
- **Autorização**: Role-based access control
- **Criptografia**: HTTPS obrigatório
- **Compliance**: LGPD, ANVISA

### RNF003 - Usabilidade
- **Responsividade**: Mobile-first design
- **Acessibilidade**: WCAG 2.1 AA
- **Internacionalização**: Suporte a pt-BR
- **PWA**: Progressive Web App

### RNF004 - Manutenibilidade
- **Código limpo**: Clean Code principles
- **Documentação**: Swagger + README
- **Testes**: Cobertura > 80%
- **Monitoramento**: Logs estruturados

### RNF005 - Portabilidade
- **Containerização**: Docker
- **Cloud-native**: AWS/Azure compatible
- **Database**: PostgreSQL
- **CI/CD**: GitHub Actions

---

## 📊 Casos de Uso

### UC001 - Cadastro de Cliente
**Ator**: Cliente
**Pré-condições**: Nenhuma
**Fluxo Principal**:
1. Cliente acessa página de cadastro
2. Preenche dados pessoais
3. Sistema valida CPF único
4. Envia email de confirmação
5. Cliente confirma email
6. Cadastro ativado

### UC002 - Compra com Receita
**Ator**: Cliente
**Pré-condições**: Cliente logado
**Fluxo Principal**:
1. Cliente adiciona medicamento ao carrinho
2. Sistema identifica necessidade de receita
3. Cliente faz upload da receita
4. Farmacêutico valida receita
5. Cliente finaliza compra
6. Pedido processado

### UC003 - Gestão de Estoque
**Ator**: Administrador
**Pré-condições**: Admin logado
**Fluxo Principal**:
1. Admin acessa painel de estoque
2. Visualiza produtos com estoque baixo
3. Registra nova entrada
4. Sistema atualiza quantidades
5. Gera relatório de movimento

### UC004 - Processamento de Pedido
**Ator**: Sistema
**Pré-condições**: Pedido confirmado
**Fluxo Principal**:
1. Sistema recebe confirmação de pagamento
2. Reserva produtos no estoque
3. Gera ordem de separação
4. Atualiza status do pedido
5. Envia notificação ao cliente

---

## 🗄️ Modelo de Dados

### Entidades Principais

#### Users (Usuários)
- **Atributos**: id, email, password_hash, full_name, cpf, phone, role
- **Relacionamentos**: 1:N com Addresses, Orders, Prescriptions

#### Products (Produtos)
- **Atributos**: id, name, description, price, sku, requires_prescription
- **Relacionamentos**: N:1 com Categories, 1:N com Inventory

#### Orders (Pedidos)
- **Atributos**: id, order_number, total_amount, status, payment_status
- **Relacionamentos**: N:1 com Users, 1:N com OrderItems

#### Prescriptions (Receitas)
- **Atributos**: id, doctor_name, doctor_crm, validity_date, status
- **Relacionamentos**: N:1 com Users, 1:N com PrescriptionItems

### Relacionamentos Chave
- **Users** ↔ **Orders**: Um usuário pode ter múltiplos pedidos
- **Orders** ↔ **OrderItems**: Um pedido pode ter múltiplos itens
- **Products** ↔ **Inventory**: Um produto pode ter múltiplos lotes
- **Prescriptions** ↔ **Orders**: Uma receita pode ser usada em múltiplos pedidos

---

## 🔌 APIs e Integrações

### APIs Internas (RESTful)

#### Authentication API
```
POST /api/v1/auth/login
POST /api/v1/auth/register
POST /api/v1/auth/refresh
POST /api/v1/auth/logout
```

#### Products API
```
GET /api/v1/products
GET /api/v1/products/{id}
POST /api/v1/products
PUT /api/v1/products/{id}
DELETE /api/v1/products/{id}
```

#### Orders API
```
GET /api/v1/orders
GET /api/v1/orders/{id}
POST /api/v1/orders
PUT /api/v1/orders/{id}/status
```

#### Prescriptions API
```
GET /api/v1/prescriptions
POST /api/v1/prescriptions
PUT /api/v1/prescriptions/{id}/validate
```

### APIs Externas

#### Gateway de Pagamento
- **Stripe/Mercado Pago**: Processamento de pagamentos
- **Endpoints**: Tokenização, cobrança, webhook

#### Serviços de Logística
- **Correios**: Cálculo de frete
- **Transportadoras**: Rastreamento de entregas

#### Serviços de Terceiros
- **AWS S3**: Armazenamento de imagens
- **SendGrid**: Envio de emails
- **Twilio**: Notificações SMS

---

## 🔒 Segurança e Compliance

### Autenticação e Autorização
- **JWT**: Tokens com expiração
- **Refresh Tokens**: Renovação automática
- **Role-based Access**: ADMIN, PHARMACIST, CUSTOMER
- **Rate Limiting**: Proteção contra ataques

### Proteção de Dados
- **HTTPS**: Comunicação criptografada
- **Hashing**: bcrypt para senhas
- **Validação**: Sanitização de inputs
- **CORS**: Configuração restritiva

### Compliance Regulatório
- **LGPD**: Consentimento e portabilidade
- **ANVISA**: Controle de medicamentos
- **Receita Digital**: Certificação ICP-Brasil
- **Auditoria**: Logs imutáveis

### Monitoramento de Segurança
- **Logs**: Tentativas de acesso
- **Alertas**: Comportamentos suspeitos
- **Backup**: Estratégia 3-2-1
- **Disaster Recovery**: Plano de contingência

---


## ✅ Critérios de Aceitação

### Critérios Técnicos
- [ ] **Arquitetura**: Clean Architecture implementada
- [ ] **Testes**: Cobertura mínima de 80%
- [ ] **Performance**: Tempo de resposta < 2s
- [ ] **Segurança**: Sem vulnerabilidades críticas
- [ ] **Documentação**: APIs documentadas com Swagger
- [ ] **CI/CD**: Pipeline automatizado funcionando

### Critérios Funcionais
- [ ] **Usuários**: Cadastro, login e perfil funcionais
- [ ] **Produtos**: CRUD completo com busca avançada
- [ ] **Pedidos**: Fluxo completo de compra
- [ ] **Receitas**: Upload e validação funcionais
- [ ] **Pagamentos**: Múltiplas formas implementadas
- [ ] **Estoque**: Controle de lotes e validades

### Critérios de Qualidade
- [ ] **Responsividade**: Funciona em mobile e desktop
- [ ] **Usabilidade**: Interface intuitiva e acessível
- [ ] **Performance**: Carregamento rápido
- [ ] **Confiabilidade**: Sistema estável
- [ ] **Manutenibilidade**: Código limpo e documentado
- [ ] **Escalabilidade**: Preparado para crescimento

### Critérios de Compliance
- [ ] **LGPD**: Tratamento adequado de dados pessoais
- [ ] **ANVISA**: Controle de medicamentos implementado
- [ ] **Segurança**: Dados criptografados e seguros
- [ ] **Auditoria**: Logs completos de operações
- [ ] **Backup**: Estratégia de backup implementada
- [ ] **Monitoramento**: Alertas e métricas configurados

---

## 📚 Recursos Adicionais

### Documentação Técnica
- **README**: Instruções de instalação e uso
- **API Documentation**: Swagger/OpenAPI
- **Architecture Decision Records**: Decisões arquiteturais
- **Database Schema**: Diagrama ER completo
- **Deployment Guide**: Guia de deploy

### Ferramentas de Apoio
- **Postman Collection**: Testes de API
- **Docker Compose**: Ambiente de desenvolvimento
- **GitHub Actions**: Workflows de CI/CD
- **SonarQube**: Análise de qualidade
- **Grafana**: Dashboards de monitoramento

### Referencias e Estudos
- **Clean Architecture**: Robert C. Martin
- **Domain-Driven Design**: Eric Evans
- **Spring Boot Documentation**: docs.spring.io
- **React Documentation**: reactjs.org
- **PostgreSQL Documentation**: postgresql.org

---

## 📞 Contato e Suporte

### Desenvolvimento
- **GitHub**: [E-Commerce Farmácia](https://github.com/scaglia-aylla1/e-commerce-farmacia)
- **Documentation**: [SwaggerUI]()
- **Demo**: [Deploy Render]()

### Tecnologias Utilizadas
- Java 17+ com Spring Boot 3.x
- React 18+ com TypeScript
- PostgreSQL 15+
- Docker e Docker Compose
- AWS Cloud Services
- GitHub Actions

---

*Documento gerado em: 10-07-2025*
*Versão: 1.0*
*Status: Em Desenvolvimento*

---

**© 2025 - E-commerce Farmácia - Projeto de Portfólio**

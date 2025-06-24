### Perfeito! Vou criar prompts separados e focados para você conseguir apresentar algo funcional no hackathon. Vamos por etapas:

| ## 1. Prompt para Arquitetura e Setup Inicial |
|---|



```
Você é um arquiteto de software especializado em plataformas educacionais. Preciso criar uma plataforma web para geração automática de provas do ensino médio usando IA.

### OBJETIVO PARA DEMO
Criar uma aplicação funcional que demonstre a geração de uma prova completa com questões de múltipla escolha estilo ENEM/vestibulares.

### ESPECIFICAÇÕES TÉCNICAS
- **Matérias**: Português, Matemática, Química, Física, Biologia
- **Tipo de questões**: Múltipla escolha (5 alternativas) estilo ENEM
- **Sistemas de referência**: Anglo e SAS (para padrão de qualidade)
- **Stack**: Python (FastAPI), React.js, PostgreSQL, Amazon Bedrock (Claude)

### ESTRUTURA DO PROJETO
Crie a estrutura completa de pastas para:
- Backend API (FastAPI)
- Frontend (React)
- Banco de dados (modelos SQLAlchemy)
- Configurações AWS
- Docker para desenvolvimento

### MODELOS DE DADOS ESSENCIAIS
1. **Questão**: id, materia, topico, enunciado, alternativas, gabarito, dificuldade, fonte_referencia
2. **Prova**: id, nome, data_criacao, questoes[], status
3. **Usuario**: id, nome, email, perfil (professor/coordenador)

### DELIVERABLES
1. Estrutura completa de pastas
2. Configuração Docker
3. Modelos de dados
4. Setup inicial do projeto
5. Documentação de instalação

Gere o código completo para setup inicial, priorizando simplicidade e funcionalidade para demo.
```

## 2. Prompt para Integração com Amazon Bedrock

```
Você é um especialista em integração de IA com Amazon Bedrock. Preciso criar um serviço para geração de questões de múltipla escolha estilo ENEM usando Claude.

### CONTEXTO
- Plataforma educacional para ensino médio
- Matérias: Português, Matemática, Química, Física, Biologia
- Padrão de qualidade: Anglo e SAS
- Tipo: Múltipla escolha (5 alternativas)

### FUNCIONALIDADES NECESSÁRIAS
1. **Serviço de Geração de Questões**
   - Função que recebe: matéria, tópico, dificuldade
   - Retorna: questão formatada com enunciado + 5 alternativas + gabarito

2. **Templates de Prompt por Matéria**
   - Prompts específicos para cada disciplina
   - Instruções para manter padrão ENEM/vestibulares
   - Referência aos sistemas Anglo/SAS

3. **Validação de Qualidade**
   - Verificação de formato da resposta
   - Validação de conteúdo pedagógico
   - Retry automático em caso de erro

### REQUISITOS TÉCNICOS
- Integração com Amazon Bedrock (Claude)
- Tratamento de erros robusto
- Logs detalhados
- Rate limiting
- Cache de questões geradas

### DELIVERABLES
1. Classe/serviço de integração com Bedrock
2. Templates de prompts por matéria
3. Sistema de validação de respostas
4. Configuração AWS
5. Testes unitários básicos

Crie o código completo focando em funcionalidade para demo, com exemplos práticos de uso.
```

## 3. Prompt para Templates de Questões por Matéria

```
Você é um especialista em criação de questões educacionais para ENEM e vestibulares. Preciso de templates de prompts específicos para geração de questões via IA.

### CONTEXTO
- Público: Estudantes de ensino médio
- Padrão: ENEM e principais vestibulares (USP, UNICAMP, UNESP)
- Referência de qualidade: Sistemas Anglo e SAS
- Formato: Múltipla escolha (5 alternativas)

### MATÉRIAS E ESPECIFICAÇÕES

**PORTUGUÊS**
- Tópicos: Interpretação de texto, gramática, literatura, redação
- Características: Textos de apoio, análise literária, norma culta

**MATEMÁTICA**
- Tópicos: Álgebra, geometria, trigonometria, estatística, funções
- Características: Problemas contextualizados, cálculos práticos

**QUÍMICA**
- Tópicos: Química orgânica, inorgânica, físico-química, estequiometria
- Características: Fórmulas, reações, problemas quantitativos

**FÍSICA**
- Tópicos: Mecânica, termodinâmica, eletromagnetismo, óptica, ondas
- Características: Problemas práticos, fórmulas, gráficos

**BIOLOGIA**
- Tópicos: Citologia, genética, ecologia, evolução, fisiologia
- Características: Processos biológicos, meio ambiente, saúde

### DELIVERABLES
Para cada matéria, crie:
1. Template de prompt principal
2. Variações por nível de dificuldade (fácil, médio, difícil)
3. Instruções específicas de formatação
4. Exemplos de questões geradas
5. Critérios de validação pedagógica

Foque em prompts que gerem questões de alta qualidade, similares aos padrões ENEM/vestibulares.
```

## 4. Prompt para Interface de Criação de Provas

```
Você é um desenvolvedor frontend especializado em interfaces educacionais. Preciso criar uma interface React para geração e visualização de provas.

### FUNCIONALIDADES DA INTERFACE
1. **Tela de Configuração de Prova**
   - Nome da prova
   - Seleção de matérias
   - Quantidade de questões por matéria
   - Nível de dificuldade
   - Botão "Gerar Prova"

2. **Tela de Geração em Tempo Real**
   - Progress bar da geração
   - Status por matéria
   - Preview das questões conforme são geradas

3. **Tela de Visualização da Prova**
   - Layout similar ao ENEM
   - Questões numeradas
   - Alternativas A, B, C, D, E
   - Opção de download PDF
   - Gabarito separado

4. **Tela de Gerenciamento**
   - Lista de provas criadas
   - Opções de editar/duplicar/excluir
   - Filtros por matéria/data

### REQUISITOS DE DESIGN
- Interface limpa e intuitiva
- Responsiva (desktop/tablet)
- Componentes reutilizáveis
- Loading states
- Tratamento de erros
- Feedback visual para usuário

### STACK
- React.js com hooks
- Material-UI ou Ant Design
- Axios para API calls
- React Router para navegação

### DELIVERABLES
1. Componentes React completos
2. Páginas principais da aplicação
3. Integração com API backend
4. Estilos CSS/styled-components
5. Tratamento de estados de loading/erro

Crie uma interface funcional e profissional para demonstração no hackathon.
```

## 5. Prompt para API Backend Completa

```
Você é um desenvolvedor backend especializado em APIs educacionais. Preciso criar uma API REST completa em FastAPI para geração de provas.

### ENDPOINTS NECESSÁRIOS
1. **POST /api/provas/gerar**
   - Recebe configuração da prova
   - Gera questões via IA
   - Retorna prova completa

2. **GET /api/provas**
   - Lista provas criadas
   - Filtros por matéria/data

3. **GET /api/provas/{id}**
   - Retorna prova específica
   - Inclui questões e gabarito

4. **POST /api/questoes/gerar**
   - Gera questão individual
   - Para testes e validação

5. **GET /api/materias**
   - Lista matérias disponíveis
   - Tópicos por matéria

### FUNCIONALIDADES CORE
- Integração com Amazon Bedrock
- Validação de dados de entrada
- Tratamento de erros
- Logs estruturados
- Rate limiting
- Cache de questões

### ESTRUTURA DE DADOS
```json
{
  "prova": {
    "id": "uuid",
    "nome": "string",
    "configuracao": {
      "materias": ["matematica", "portugues"],
      "questoes_por_materia": 10,
      "dificuldade": "medio"
    },
    "questoes": [...],
    "gabarito": [...],
    "status": "concluida",
    "created_at": "datetime"
  }
}
```

### DELIVERABLES
1. API FastAPI completa
2. Modelos Pydantic
3. Integração com banco PostgreSQL
4. Serviços de IA
5. Documentação automática (Swagger)
6. Testes básicos

Foque em criar uma API robusta e funcional para a demonstração.
```

### ## Estratégia de Execução para o Hackathon:

| 1. **Dia 1**: Execute prompts 1 e 2 (Setup + Integração IA) |
|---|


2. **Dia 2**: Execute prompts 3 e 5 (Templates + API)
3. **Dia 3**: Execute prompt 4 (Interface) + Integração final

Quer que eu detalhe mais algum prompt específico ou criar prompts adicionais para funcionalidades específicas?

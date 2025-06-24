### Excelente projeto! Vou criar um prompt estruturado para o Amazon Q Developer que vai ajudar a desenvolver o código inicial da plataforma. Aqui está o prompt otimizado:

| ## Prompt para Amazon Q Developer |
|---|



```
Você é um desenvolvedor sênior especializado em plataformas educacionais e IA. Preciso criar uma plataforma web para "Otimização do Processo de Provas com IA" com as seguintes especificações:

### CONTEXTO DO PROJETO
- Plataforma para automatizar criação de provas do ensino médio usando IA
- Substituir criação manual de questões por professores
- Manter qualidade pedagógica com validação docente
- Permitir comparação entre provas tradicionais vs IA durante calibragem

### FUNCIONALIDADES PRINCIPAIS
1. **Geração de Questões com IA**
   - Integração com Claude (Amazon Bedrock)
   - Geração baseada em planejamento curricular
   - Diferentes tipos de questões (múltipla escolha, dissertativas, etc.)
   - Níveis de dificuldade configuráveis

2. **Sistema de Validação**
   - Interface para professores validarem questões geradas
   - Aprovação/rejeição com comentários
   - Histórico de validações

3. **Gestão de Provas**
   - Criação de provas com questões validadas
   - Versionamento de provas (tradicional vs IA)
   - Agendamento e distribuição

4. **Dashboard Analítico**
   - Comparação de performance entre modelos
   - Métricas de qualidade das questões
   - Relatórios para coordenadores

5. **Banco de Questões Inteligente**
   - Armazenamento categorizado por matéria/tópico
   - Sistema de tags e metadados
   - Busca avançada

### STACK TECNOLÓGICA SUGERIDA
- **Backend**: Python (FastAPI) ou Node.js
- **Frontend**: React.js ou Vue.js
- **Banco de Dados**: PostgreSQL + Redis (cache)
- **IA**: Amazon Bedrock (Claude)
- **Infraestrutura**: AWS (Lambda, RDS, S3, CloudFront)
- **Autenticação**: AWS Cognito

### ESTRUTURA INICIAL NECESSÁRIA
1. Configuração do projeto com estrutura de pastas
2. Modelos de dados (usuários, questões, provas, validações)
3. APIs básicas para CRUD de questões e provas
4. Integração inicial com Amazon Bedrock
5. Interface básica de administração
6. Sistema de autenticação e autorização por perfis (professor, coordenador, admin)

### REQUISITOS ESPECÍFICOS
- Arquitetura escalável para múltiplas escolas
- Logs detalhados para auditoria
- Backup automático de questões
- Interface responsiva
- Suporte a diferentes formatos de questão (texto, imagem, fórmulas matemáticas)

Gere o código inicial completo incluindo:
- Estrutura de pastas do projeto
- Configurações de ambiente
- Modelos de dados
- APIs principais
- Interface administrativa básica
- Documentação de setup

Priorize código limpo, bem documentado e seguindo boas práticas de desenvolvimento.
```

### ## Dicas Adicionais para Maximizar o Resultado:

| 1. **Execute o prompt em etapas**: Primeiro peça a arquitetura geral, depois cada módulo específico |
|---|



2. **Personalize conforme necessário**: Adicione detalhes específicos sobre:
   - Matérias que serão cobertas
   - Tipos específicos de questões
   - Integrações com sistemas existentes

3. **Solicite exemplos específicos**: Peça exemplos de prompts para geração de questões por matéria

4. **Pense na demonstração**: Para o hackathon, foque em uma funcionalidade core que funcione end-to-end

Quer que eu ajude a refinar alguma parte específica do prompt ou criar prompts adicionais para funcionalidades específicas?

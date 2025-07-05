Relatório de Gestão de Riscos, Vulnerabilidades e Ameaças

# Cenário 🛡️

Sendo um consultor de cibersegurança, fui contratado para prestar serviço a uma famosa empresa do ramo financeiro que foi recentemente atacada e teve os dados dos clientes expostos. Por ser uma empresa listada na bolsa, fez-se necessário divulgar para o mercado uma nota, esclarecendo o ocorrido. O CEO da ACME Truques Financeiros, Sr. P. Léguas, me deu carta branca e orçamento livre para a implantação de três processos que foram solicitados pela CVM e BACEN:

## 1- Gestão de ameaças 🚨

**Objetivo**: Garantir que as principais ameaças para o setor financeiro estejam sendo monitoradas e bloqueadas.

### 1.1 Livro de casos de uso:

| Caso | Objetivo | Regra | Fontes necessárias |
|---|---|---|---|
| 1° | Detectar acessos remotos não autorizados | Monitorar logs de autenticação e redes para logins fora do padrão. | Logs de autenticação e firewalls |
| 2° | Mitigar vazamento de dados sensíveis | Monitorar tráfego de rede, e-mail suspeitos e alertas de acessos não autorizados. | Dados de Firewalls, e-mails, banco de dados |
| 3° | Mitigar possíveis ataques de força bruta (DDoS) | Monitorar picos incomuns de tráfego de rede, número excessivo de requisições a serviços web, e alertas de sistemas. | Dados de firewall, servidores web e tráfego de rede. |
| 4° | Prevenir ataques de ransomware | Atualizações regulares do sistema, controle de acesso rígido em arquivos que possuam dados sensíveis, monitoramento constante dos dados e backups preventivos. | Logs de eventos do sistema, antivírus, firewall, monitoramento de rede. |
| 5° | Mitigar fraudes de acesso a áreas com acesso privilegiado | Monitorar acessos e atividades de usuários privilegiados, incluindo tentativas de elevação de privilégios e acessos a dados críticos. | Dados do sistema de gerenciamento de acessos (PAM) e banco de dados. |
| 6° | Alertar possíveis ataques de phishing | Monitorar logs de servidor de e-mail para mensagens com características de phishing e alertas de sistemas de segurança. | Servidores de e-mail e dados de anti-spam |
| 7° | Evitar injeção de códigos maliciosos em aplicações web ou em banco de dados (sql injection) | Monitorar alertas de injeção de SQL e XSS, e logs de servidor web para requisições maliciosas. | Dados de servidores web e banco de dados. |
| 8° | Mitigar possíveis fraudes de cartões de crédito | Monitorar transações incomuns, picos de uso de cartões e logs de sistemas de processamento de cartão de crédito para atividades suspeitas. | Banco de dados dos cartões de crédito e sistemas de transações |
| 9° | Detectar malware no sistema e servidores | Monitorar dados de endpoints e antivírus para detecção de malware, logs de sistema para comportamento anômalo de processos e arquivos.  | Relatórios de antivírus e dados do sistema de operação dos servidores e sistemas. |
| 10° | Monitorar o tráfego de rede |Monitorar o fluxo de dados na rede, identificando padrões de tráfego normais e anormais. | Dados dos firewalls e IPS/IDS |
| 11° | Mitigar vulnerabilidades conhecidas |Realizar varreduras de vulnerabilidades regulares. | Relatórios de vulnerabilidades |
| 12° | Monitorar quaisquer modificações feitas nos bancos de dados | Monitorar logs de auditoria de banco de dados para alterações em esquemas, tabelas, usuários e privilégios.| Banco de dados |
| 13° | Identificar possíveis agentes maliciosos | Analisar logs de segurança e eventos para identificar padrões de comportamento que correspondam a perfis de agentes de ameaça conhecidos. | Dados do sistema de autenticação e de controles de acesso. |
| 14° | Recorrer a meios para proteger dados de possíveis perdas, como realização de backups. | Implementar e monitorar rotinas de backup regulares e testar a restauração dos dados periodicamente. | Ferramentas de backups |
| 15° | Mitigar possíveis engenharias sociais | Educar e conscientizar os funcionários sobre táticas de engenharia social e monitorar atividades suspeitas de comunicação interna e externa. | Relatórios de treinamento, servidores de e-mail. |

### 1.2 - Tecnologias adquiridas para monitoração e/ou tratamentos de ameaças cibernéticas: 💻

| Fabricante | Produto | Justificativa |
|---|---|---|
| Cisco Systems | Splunk Enterprise Security | Ferramenta SIEM para centralizar o monitoramento e análise de ameaças e comportamentos anormais. |
| Microsoft | Microsoft Defender | Analisar dados de múltiplas fontes para identificar possíveis ameaças ao sistema. |
| Exabeam | Exabeam | Detectar atividades anormais que possam afetar informações sensíveis, como vazamento de dados. |

## 2- Gestão de vulnerabilidades 🩹

**Objetivo**: Garantir que todas as vulnerabilidades cibernéticas da empresa sejam descobertas e tratadas.

### 2.1 Definir a estratégia que será utilizada para tratamento das vulnerabilidades, desde sua detecção até o tratamento final. 📝

A estratégia será incorporar ferramentas de segurança responsáveis por detectar e identificar vulnerabilidades no sistema, com acompanhamento de CVE, CWE, CVSS e definir regras para lidar com, ordem de prioridades, as possíveis intercorrências. Uso de ferramentas automatizadas para realizar análise estáticas (SAST), responsáveis por definir níveis de criticidade entre as vulnerabilidades identificadas, configurar ambientes de simulação para testes dinâmicos (DAST), incluindo teste de penetração. Será de suma importância, o monitoramento constante dos logs de múltiplas áreas do sistema com o uso de ferramentas SIEM.

As etapas do plano de estratégia serão feitas da seguinte forma:

1.  **Identificar as vulnerabilidades conhecidas** com a ajuda de boletins de seguranças fornecidos por fóruns especializados, como o CVE e CWE. Descobrir novas vulnerabilidades com uso de pentests periódicos.
2.  **Analisar e definir o nível de criticidade** para cada vulnerabilidade identificada com a ajuda do CVSS, determinar seu impacto ao sistema e ordenar seu nível de prioridade de acordo com risco causado.
3.  **Tratar as vulnerabilidades** após definir uma matriz de risco para determinar quais tipos de tratamentos serão usados, como aceitar, evitar, mitigar e transferir.
4.  **Monitoramento contínuo** para confirmar a mitigação ou novos riscos das vulnerabilidades identificadas e deixando tudo documentado para futuras pesquisas.

### 2.2 Tecnologias adquiridas para detecção e orquestração de vulnerabilidades: 🛠️

| Fabricante | Produto | Justificativa |
|---|---|---|
| Qualys | Qualys VMDR | Permite a descoberta de vulnerabilidade realizando uma análise e corrigindo de forma automatizada em diversos ambientes, incluindo nuvem e endpoints. |
| Sonar | SonarQube | Automatiza a segurança dos códigos desenvolvidos e fornece recomendações de codificações mais seguras. |
| Snyk | Snyk | Acelera o desenvolvimento seguro do sistema com o uso de inteligência artificial, reduzindo possíveis vulnerabilidades. |

## 3- Gestão de riscos 📊

**Objetivo**: Implementar processos de gestão de riscos que sejam capazes de promover visibilidade e gerenciamento dos riscos cibernéticos da empresa.

Descrever as atividades necessárias para se implementar com os detalhes em cada etapa do processo (PDCA).

### 3.1 Metodologia e frameworks utilizados: 📖

A metodologia utilizada será a Estrutura de Gerenciamento de Risco (RMF) do framework NIST (National Institute of Standards and Technology) sendo comumente usada em setores financeiros.

### 3.2 - Explicando cada etapa do processo, descrevendo seus principais objetivos e resultados esperados. 🎯

As etapas do processo de gestão de riscos serão baseados no NIST RMF:

### 1° Preparar ⚙️

-   **Objetivo**: Preparar todos os níveis da organização para gerenciar seus riscos de segurança e privacidade usando o RMF.
-   **Atividades**:
    * Definir o contexto organizacional, incluindo missão, objetivos e ambiente de operação da ACME Truques Financeiros, além de identificar informações críticas para o negócio.
    * Revisar ou criar políticas de segurança da informação e privacidade de acordo com os requisitos da CVM e BACEN.
    * Estabelecer claramente as responsabilidades das partes interessadas na gestão de riscos, como o Comitê de Auditoria, equipes técnicas, RH, Jurídico e Comunicação.
    * Determinar o apetite a risco da empresa, de acordo com o perfil de risco do Sr. P. Léguas e as exigências regulatórias.
    * Garantir a alocação adequada de recursos humanos, financeiros e tecnológicos para implementar e manter o processo de gestão de riscos.
-   **Resultados esperados**:
    * Estabelecimento de políticas de segurança;
    * Organização e divisão das funções de acordo com as partes interessadas e suas responsabilidades;
    * Definição do apetite de riscos da organização.

### 2° Categorizar 🗂️

-   **Objetivo**: Gerenciar riscos organizacionais, determinando o impacto adverso na confidencialidade, integridade e disponibilidade dos sistemas e informações.
-   **Atividades**:
    * **Categorização de Dados**: Categorizar os dados processados, armazenados e transmitidos por ativos presentes na empresa com base em sua criticidade, sensibilidade (por exemplo, dados de cartão de crédito, informações pessoais).
    * **Categorização de Sistemas**: Atribuir classificações de segurança (impacto baixo, moderado ou alto para confidencialidade, integridade e disponibilidade) aos sistemas com base na criticidade dos dados que eles processam. Por exemplo, o servidor de banco de dados e os sistemas de cartão de crédito provavelmente terão classificação de impacto alta devido aos dados sensíveis.
-   **Resultados esperados**:
    * Classificação dos níveis de risco de cada sistema ou dado com base em nível de criticidade;
    * Documentação dos requisitos de segurança e privacidade para cada sistema e tipo de dado.

### 3° Selecionar ✅

-   **Objetivo**: Selecionar, adaptar e documentar controles de proteção de sistemas e da organização de forma proporcional ao risco.
-   **Atividades**:
    * Selecionar controles de segurança e privacidade com base na categorização dos sistemas e requisitos regulatórios (BACEN, CVM, PCI-DSS, LGPD).
    * Adaptar os controles selecionados para as necessidades da ACME Truques Financeiros, considerando a arquitetura de rede e tecnologias existentes (rede única, acesso remoto via VPN).
    * Documentar os controles, incluindo configurações, procedimentos e responsabilidades.
-   **Resultados esperados**:
    * Seleção de conjuntos de controles de segurança com base na categorização do sistema.
    * Adaptação dos controles para atender às necessidades da organização e seu sistema.
    * Documentação detalhada dos controles abordados.

### 4° Implementar 🚀

-   **Objetivo**: Os controles de segurança selecionados são implementados e operam eficazmente.
-   **Atividades**:
    * Configurar regras de NGFW para segmentar a rede, controlar o tráfego entre os diferentes tipos de servidores e estações de trabalho, além de bloquear acessos não autorizados.
    * Configurar os roteadores para garantir conectividade segura e segmentação da rede.
    * Implementar criptografia de dados em repouso e em trânsito, controle de acesso granular e auditoria detalhada.
    * Implementar SAST e SCA para identificar vulnerabilidades no código e componentes de terceiros antes da produção.
-   **Resultados esperados**:
    * Controles de segurança configurados e instalados de forma correta e atualizada;
    * Treinamentos de conscientização dos usuários e equipes técnicas sobre os novos controles selecionados.

### 5° Avaliar 📝

-   **Objetivo**: Verificar se os controles estão implementados corretamente, operando conforme o esperado e produzindo os resultados desejados para atender aos requisitos de segurança e privacidade do sistema e da organização.
-   **Atividades**:
    * Realizar auditorias internas e externas dos controles implementados.
    * Utilizar DAST e Pentests para identificar falhas na implementação ou novas vulnerabilidades.
    * Analisar logs de segurança e incidentes passados para avaliar a eficácia dos controles em detectar e responder a ameaças.
    * Avaliar se as políticas e procedimentos estão sendo seguidos e se são eficazes.
-   **Resultados esperados**:
    * Criação de relatórios de testes e avaliação dos controles implementados;
    * Identificação de não conformidades com os controles;
    * Recomendações de melhorias e correções.

### 6° Autorizar 👍

-   **Objetivo**: Atribuir a um funcionário sênior a responsabilidade de determinar a aceitabilidade do risco de segurança e privacidade decorrente da operação de um sistema ou do uso de controles comuns.
-   **Atividades**:
    * O Comitê Executivo ACME de Auditoria e o Sr. P. Léguas revisarão os resultados da avaliação dos controles e o risco residual.
    * O funcionário sênior decide formalmente se o risco residual é aceitável, considerando o apetite a risco da empresa.
    * Para riscos não aceitáveis, desenvolver planos de ação para mitigar, transferir ou evitar o risco.
-   **Resultados esperados**:
    * Tomada de decisão para aceitação ou não do risco em questão;
    * Criação de plano de ação para mitigar riscos não aceitáveis;
    * Documentação de autorização pelo responsável para operar o sistema.

### 7° Monitorar 📈

-   **Objetivo**: Manter consciência situacional contínua sobre a segurança e privacidade do sistema e da organização para apoiar a gestão de riscos.
-   **Atividades**:
    * Usar SIEM para monitorar continuamente o desempenho dos controles de segurança e a detecção de ameaças.
    * Realizar revisões regulares da matriz de risco e do mapa de calor para identificar novas ameaças, vulnerabilidades e mudanças no ambiente que possam afetar o perfil de risco.
    * Ajustar o processo de gestão de riscos e os controles implementados conforme a evolução das ameaças, tecnologias e requisitos regulatórios.
    * Fornecer relatórios periódicos ao Comitê Executivo ACME de Auditoria sobre a postura de risco da empresa.
-   **Resultados esperados**:
    * Monitoramento contínuo da eficácia dos controles e da postura de risco;
    * Revisão periódica dos riscos e reavaliação das conformidades.

### 3.3 Tecnologias adquiridas para detecção e orquestração de vulnerabilidades: 🔗

| Fabricante | Produto | Justificativa |
|---|---|---|
| RSA | RSA Archer | Oferece recursos automatizados para conformidades, alinhado ao objetivo de gerenciamento de riscos. |
| CrowdStrike | CrowdStrike Falcon | Inteligência de ameaças que contribui para a gestão de riscos e melhora a detecção de ameaças provendo dados essenciais. |
| One Trust | OneTrust | Gerencia a privacidade e conformidades de dados sensíveis, sendo de suma importância para lidar com dados sensíveis dos clientes. |

## 4 Planilha para gestão de Risco 

<img width="1350" height="843" alt="Image" src="https://github.com/user-attachments/assets/9ee353a6-5e5e-4152-a76e-a702f68ae9d5" />

**4.1 Matriz de Risco**

<img width="560" height="144" alt="Image" src="https://github.com/user-attachments/assets/c68b409f-8c79-4ebd-82b8-bd9a9be5d0f2" />


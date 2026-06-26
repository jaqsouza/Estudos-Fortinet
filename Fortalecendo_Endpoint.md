### Hardening Endpoints  

Abaixo estão 4 tópicos e formas de deixar o seu endpoint mais protegido.  

# Controles Administrativos

- Senhas - Muitas vezes são a primeira barreira de defesa, as recomendações envolvem o uso de senhas grandes, que mistura letras maiúsculas e minúsculas, números e símbolos. Além de serem trocadas de tempo em tempo

- Restrição de Usuário - Bloqueia ou limita o que o usuário pode ver, acessar ou baixar. Podemos fazer a ligação com os filtros de conteúdo da Fortinet que foi um dos assuntos passados.

- Princípio de Privilegio Mínimo - Principle of Least Privilegio (PoLP) - É você dar ao usuário ou processo apenas as permissões necessárias para realizar a sua função e nada além disso. Uma pessoa do marketing não precisa ter acesso a dados do RH, por exemplo.  

# Proteção de Endpoint Local  

- OS and Startup Hardening - É um conjunto de técnicas de "endurecimento" e segurança aplicadas ao sistema operacional (FortiOS) e ao processo de inicialização (boot) dos dispositivos, como os firewalls. Como exemplo você pode configurar os logs, backup, realizar pentests, monitorar vulnerabilidades, entre outros..

- Boot Management - É um menu de nível de BIOS/UEFI acessível durante a inicialização do dispositivo. Ele é usado para recuperação de desastres, atualizações de firmware de emergência e manutenção do sistema operacional 

- Segurança e Criptografia de Disco - Envolve a aplicação de criptografia para proteger dados sensíveis armazenados em discos físicos, sejam em equipamentos de segurança da própria marca ou em endpoints (computadores dos usuários) gerenciados pelo ecossistema da empresa.

- Data Loss Prevention (DLP) - Previne que dados da empresa sejam vazados para fora, ele 
permite que as empresas detectem a perda de dados, bem como evitem a transferência não autorizadas de dados para fora da organização e a destruição indesejada de dados confidenciais ou pessoalmente identificáveis (PII).  

# Manutenção de Endpoints  

- Auto-updates / Patching - Automação de atualização, pois elas trazem novas correções de vulnerabilidades.

- Policy Checks - É uma ferramenta nativa de diagnóstico e auditoria da Fortinet, ela é usada para verificar a consistência, eficácia e o processamento de regras de firewall.

- Backup - É importante para casos em que ocorra a perda de dados por diversos motivos, mantendo a rápida recuperação e disponibilidade de um serviço. Ajuda em casos de ataques de ransomware.  

# Monitoramento de Endpoints  

- Endpoint Protection Platform (EPP) - Previne que ameaças consigam infectar um dispositivo. Exemplos incluem FortiClient, FortiXDR e FortiEDR. Um EPP pode realizar o bloqueio de algo suspeito.

- Intrusion Detection Systems (IDS) - Faz monitoramento atrás de algo suspeito e alerta sobre, mas não realiza bloqueios.

- Endpoint Detection and Response (EDR) - Percebe um comportamento suspeito e age em cima dele.  

> [!TIP]
> Caso esteja com dificuldades para entender a diferença entre EPP e EDR, o EPP age analisando arquivos atrás de algo que sabe ser malicioso, já uma EDR analisa o comportamentos suspeitos e pode descobrir ataques de zero day. Por exemplo, um arquivo que chegou por e-mail é analisado pelo EPP, mas ele não apresenta nada de suspeito e o EPP deixa ele passar, quando começa sua ação o EDR percebe que tem um processo criptografando tudo e para ele.    

Material complementar: [Hardening](https://docs.fortinet.com/document/fortigate/8.0.0/best-practices/555436/hardening), [DLP](https://www.fortinet.com/br/resources/cyberglossary/dlp), [Vulnerability-scanning-compare](https://www.fortinet.com/br/resources/cyberglossary/vulnerability-scanning-compare), [Policy-and-route-checks](https://docs.fortinet.com/document/fortigate/6.2.0/cookbook/217826/policy-and-route-checks)

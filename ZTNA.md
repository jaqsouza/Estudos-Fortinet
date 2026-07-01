# ZTNA 

ZT = Zero Trust

NA = Acesso à Rede

Ou seja, nunca confiar automaticamente em ninguém na rede.

----  
FortiClient = Programa que o usuário instala na máquina para se conectar. Ele é um agente de proteção.  

FortiClient EMS (Endpoint Management Server) = Servidor que gerencia de forma centralizada todos esses agentes instalados.  

----

O FortiClient envia para o FortiClient EMS:

- Características do dispositivo: Informações de hardware, sistema operacional, endereço IP, nome do computador e número de série.
- Informações do usuário: Nome do usuário conectado e credenciais associadas ao domínio, como ID do usuário.
- Postura de segurança do dispositivo: Status de proteção em tempo real (antivírus ativo, assinaturas atualizadas), histórico de ameaças ou malwares detectados.

----

Com essas informações o FortiClient EMS consegue gerar tags e emitir um certificado digital para o cliente.

- O certificado digital identifica o dispositivo, geralmente muda pouco, ele é emitido durante o registro no EMS e serve como uma prova de identidade.

- Com um certificado válido, é possível estabelecer uma conexão TLS (ou mTLS, quando há autenticação mútua entre cliente e servidor), criando um canal criptografado para a comunicação. O certificado é utilizado durante o handshake TLS para autenticar o dispositivo.

- Depois vem as tags, que descrevem o estado do dispositivo. Elas pode mudar a qualquer momento, são atualizadas continuamente pelo FortiClient EMS, servem como uma prova de conformidade (postura) do dispositivo com as políticas de segurança configuradas.
> [!IMPORTANT]
> O FortiGate pode acabar com a sessão criptografada caso o o dispositivo não esteja em conformidade.

----
> [!NOTE]
> Essa dinâmica funciona pois no ZTNA a decisão de acesso não depende apenas de quem é o usuário, mas também de qual dispositivo está sendo usado (certificado) e em que estado esse dispositivo se encontra (tags de postura). Por exemplo, se um dispositivo em conformidade desativa o antivírus, sua tag muda e ele pode não ser mais confiável, mesmo que o login de usuário seja realizado certinho. 

> Quando o usuário se autentifica, e tudo está validado, ele recebe uma função do servidor de autenticação (pode ser AD, diretório de LDAP, um database ou IDaaS), essa função define qual o tipo de acesso essa pessoa vai ter na rede.

Materiais complementares: [tags](https://docs.fortinet.com/document/forticlient/7.4.7/ems-administration-guide/937027/tags), [O que é ZTNA](https://www.fortinet.com/br/resources/cyberglossary/what-is-ztna)

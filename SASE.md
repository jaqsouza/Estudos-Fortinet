# SASE

SASE (Secure Access Service Edge) é uma arquitetura que combina serviços de rede e segurança entregues pela nuvem para fornecer acesso seguro a usuários, dispositivos e aplicações, independentemente de sua localização. Assim colaboradores híbridos e remotos conseguem ter um acesso mais seguro.  

---
> [!NOTE]
> Uma arquitetura é um modelo de como os componentes devem funcionar juntos e o SASE depende desse integração entre eles.

No caso do SASE da Fortinet os componentes são:

- SD-WAN: Escolhe o melhor caminho da internet.
- Firewall: Bloqueia o que há de ruim.
- ZTNA: Só pode entrar na rede quem provar que é confiavel.
- Secure Web Gateway: Protege enquanto navegamos.
- CASB: Cuida dos aplicativos na nuvem.

---
> [!TIP]
> A implementação da arquitetura de SASE da Fortinet se chama FortiSASE, ele é um produto/serviço, executado na nuvem da Fortinet.

> [!NOTE]
> O termo “Thin Edge” se refere a um problema onde filiais possuem apenas segurança mínima e dependem de uma rede central para a maior parte das funções de segurança (como precisar se conectar a matriz da empresa antes de acessar a internet). O FortiSASE é a solução moderna para esta questão, pois permite que a filial ou o usuário acesse a Internet diretamente, enquanto a segurança é aplicada na nuvem.

---
Materiais complementares: [SASE](https://www.fortinet.com/br/resources/cyberglossary/sase)

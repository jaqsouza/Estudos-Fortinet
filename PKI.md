# Public Key Infrastructure (PKI)  

São ferramentas usadas para implementar criptografia em uma rede de computadores, ele é usado amplamente para proteger a comunicação na internet. Com este conjunto de tecnologias, políticas e processos é possível criar, gerenciar, distribuir, validar e revogar certificados digitais e chaves criptográficas.  

---
O PKI garante:

- Privacidade e confidencialidade
- Integridade
- Autenticidade
- Não Repúdio

---

A PKI funciona baseada em dois elementos principais: chaves criptográficas (criptografia assimétrica) e certificados digitais.

Na criptografia assimétrica é usada duas chaves, uma pública (quem criptografa) e uma privada (quem descriptografa). Como não é necessario compartilhar qual é a chave privada, esse tipo de criptografia trás uma maior segurança para auteticação. Porém, ela é mais lenta se comparada por exemplo com a criptografia simetrica, onde só é preciso uma chave.      

Algoritmos comuns: RSA, ECC (Elliptic Curve Cryptography), Diffie-Hellman.  

Já os certificados digitais são como um documento de identidade com informações como Identidade do proprietário, chave pública, período de validade. Este certificado é emitido por uma autoridade que ambos (cliente e servidor) confiam, autoridade certificadora (CA), que pode ter o apoio de uma autoridade de registro (RA), cuja a função é validar a identidade do solicitante antes da emissão do certificado.  

Material complementar: [public key infrastructure](https://www.fortinet.com/br/resources/cyberglossary/public-key-infrastructure)

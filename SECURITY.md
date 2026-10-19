# Segurança

A PDTI Revive está em desenvolvimento e ainda não passou por uma auditoria de segurança independente.

## Informações que não devem entrar neste repositório

- Senhas, tokens, chaves SSH/GPG privadas e certificados com chave privada.
- Arquivos pessoais, dados de clientes, endereços internos de rede e configurações privadas de servidores.
- Rootfs extraídos, bancos de dados, backups, logs privados e imagens de discos virtuais.
- Chaves privadas usadas para assinar o catálogo da PDTI Store.

## Comunicação de vulnerabilidades

Evite publicar detalhes de vulnerabilidades exploráveis, chaves ou dados sensíveis em Issues públicas. Entre em contato com os mantenedores por um canal privado apropriado antes de divulgar um problema grave.

## Integridade

Os artefatos de uma futura Release deverão incluir manifesto SHA-256, histórico de construção e informação clara sobre componentes e licenças. A presença de SHA-256 não equivale a uma assinatura digital nem comprova a segurança do software.

# Histórico de desenvolvimento

Este registro resume marcos do projeto. As versões anteriores são marcos de desenvolvimento, não necessariamente lançamentos públicos.

## 0.3.2-dev — boot e instalador em teste (28/10/2026)

- Imagem **Lite build6 bootlayout**: após ajuste de uma falha de boot observada nos testes, o mantenedor confirmou que o ambiente iniciou e o instalador abriu diretamente, sem a mensagem anterior.
- SHA-256 da ISO local `pdti-revive-lite-amd64-0.3.2-build6-bootlayout.iso` validado por `sha256sum -c`: `fb8d297f805a4bc17c14c87df5b9b4538433ba608c410f68ff7a093f9c746945`.
- Teste do **AutoTune** em computador Dell com funcionamento confirmado; objetivo de otimização geral para diferentes hardwares, não exclusiva desse equipamento.
- Iniciada a etapa de planejamento/refinamento de **desempenho e navegação** para computadores variados. Não declarar ganho de desempenho comprovado antes de medições.
- **Pendências:** homologação 0.3.2 Lite/Standard, testes em mais combinações BIOS/UEFI, revisão de licenças, disponibilização auditada do código e geração de release pública.
- **Importante:** não há confirmação de uma ISO 0.3.2 Standard finalizada nem de release pública; este registro descreve os testes locais informados pelo mantenedor.

## Catálogo v104 e revisões de inicialização (21–22/10/2026)

- Catálogo remoto assinado da **PDTI Store v104 publicado**, com **69 aplicativos**, incluindo **WPS Office** (`com.wps.Office`) via Flatpak; pacote proprietário de terceiros e não verificado pelo fabricante.
- Instalação do **WPS Office** confirmada em teste, porém **interface em pt-BR ainda pendente**.
- Imagens 0.3.1 reempacotadas para boot com **GRUB2 BIOS/UEFI**; testes de inicialização positivos em QEMU e notebook com BIOS Legacy. Testes UEFI completos permanecem em aberto.

## 0.3.1 R7 — ícones automáticos no Live CD (20/10/2026)

- **Lite e Standard R7 compiladas**, conforme confirmação do mantenedor. Revisão em homologação, sem publicação pública das ISOs até o momento.
- **PDTI Store 0.3.1-7:** atualização automática, não bloqueante e com intervalo entre tentativas, dos metadados AppStream do Flathub para resolver ícones de aplicativos.
- Carregamento automático de ícones confirmado pelo mantenedor em teste com **Live CD R7**, sem executar `flatpak update --appstream flathub` manualmente.
- Catálogo remoto **v103 com 68 aplicativos**, assinado digitalmente com **Ed25519**, incluindo Arduino IDE 2 e Tor Browser Launcher.
- **PDTI Store Manager:** ferramenta administrativa utilizada para adicionar programas e publicar versões assinadas do catálogo no GitHub sem recompilar as ISOs.
- **R6 (etapa anterior):** busca dinâmica de ícones APT/Flatpak, catálogo remoto e integração com Flathub; a R7 acrescenta a atualização automática do AppStream.
- Mantidos os **45 ícones offline existentes**; novos ícones do Flathub podem depender de internet e de metadados baixados para aparecer.
- Pendências: testes de instalação limpa específicos da R7 nas duas edições, verificação dos hashes SHA-256 das ISOs R7, revisão de licenças e homologação geral.

## 0.3.1 — em homologação

- PDTI Store com catálogo ampliado e estados de disponibilidade APT.
- Interface com detalhes dos aplicativos e identificação visual.
- Correção de detecção indevida de processo auxiliar `unattended-upgrades`.
- Integração de Flatpak e configuração preparada para Flathub no primeiro acesso.
- 45 ícones reais coletados para funcionamento offline; **redistribuição pendente de revisão de licenças**.
- Geração das ISOs Lite e Standard; hashes confirmados conforme README.

## 0.3.0 — etapa AutoTune

- Evolução dos perfis Lite e Standard e da seleção conforme o hardware.

## 0.2.0 — etapa de integração e testes

- Testes das edições Lite e Standard e refinamentos do sistema de instalação.

## Próximos passos

- Homologar a **0.3.2** nas duas edições e em hardwares diversos, verificando BIOS/UEFI, instalador e desempenho.
- Revisar o suporte ao **português do Brasil no WPS Office**.
- Reconstituir e publicar apenas os fontes auditados.
- Confirmar instalação limpa, APT, Flatpak e comportamento offline **da R7** nas duas edições.
- Revisar licença de código, dependências e ícones antes de disponibilizar ISOs.

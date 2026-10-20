<div align="center">

# PDTI Revive

### Uma nova vida para computadores antigos.

**Distribuição Linux baseada no Debian 13 (Trixie), com Xfce, aplicativos acessíveis e otimização inteligente para diferentes perfis de hardware.**

<p>
  <img alt="Debian 13" src="https://img.shields.io/badge/Base-Debian%2013-A81D33?style=flat-square&logo=debian&logoColor=white">
  <img alt="Desktop Xfce" src="https://img.shields.io/badge/Desktop-Xfce-2869B1?style=flat-square">
  <img alt="Edições Lite e Standard" src="https://img.shields.io/badge/Edi%C3%A7%C3%B5es-Lite%20%2B%20Standard-556B2F?style=flat-square">
  <img alt="Versão 0.3.1 em homologação" src="https://img.shields.io/badge/0.3.1-Em%20homologa%C3%A7%C3%A3o-E6A23C?style=flat-square">
</p>

[Visão geral](#visão-geral) · [PDTI Store](#pdti-store--central-própria-de-aplicativos) · [AutoTune](#autotune--otimização-inteligente) · [Edições](#edições) · [Capturas](#capturas-de-tela) · [Status](#status-do-projeto)

<a href="docs/imagens/01-area-de-trabalho.webp">
  <img src="docs/imagens/01-area-de-trabalho.webp" alt="Área de trabalho da PDTI Revive com Xfce" width="510">
</a>

<sub>Prévia da área de trabalho • clique na imagem para ampliar</sub>

</div>

---

## Visão geral

O **PDTI Revive** é um projeto de distribuição Linux voltado a tornar o uso do computador mais simples, mesmo em máquinas com recursos limitados. Combina a base do **Debian 13**, o ambiente gráfico **Xfce** e ferramentas desenvolvidas para facilitar a instalação de aplicativos e o ajuste do sistema.

O desenvolvimento prioriza **leveza, manutenção prática e uma experiência familiar**. O projeto permanece em homologação: as ISOs já foram compiladas, mas ainda não são anunciadas aqui como lançamentos públicos.

## Principais recursos

| Recurso | O que oferece |
| :--- | :--- |
| **PDTI Store** | Catálogo organizado por categorias, busca, detalhes de aplicativos e ações de instalação ou remoção. |
| **APT + Flatpak** | Acesso a programas dos repositórios Debian e suporte a aplicativos externos via Flathub. |
| **Ícones de aplicativos** | Identificação visual com cache AppStream e imagens disponíveis offline quando incorporadas. |
| **AutoTune** | Detecta características do hardware e ajusta o perfil de otimização do sistema. |
| **Desktop Xfce** | Interface tradicional e personalizável, adequada ao objetivo de manter o sistema leve. |
| **BIOS e UEFI** | Imagens híbridas preparadas para diferentes modos de inicialização. |

## PDTI Store — central própria de aplicativos

A **PDTI Store** é a loja desenvolvida para o PDTI Revive. Em vez de depender do terminal para encontrar e instalar programas, o usuário encontra uma interface gráfica organizada, integrada ao Debian 13.

A versão **0.3.1-5** reúne um catálogo local de **66 entradas** e apresenta informações para ajudar o usuário a escolher programas compatíveis com o computador.

**O que ela oferece:**

- **Explorar e pesquisar:** navegação por categorias como internet, escritório, multimídia, design e utilitários.
- **Identificação visual:** ícones próprios quando disponíveis; a versão testada incorpora **45 imagens reais para uso offline**, com fallback para os demais aplicativos.
- **Disponibilidade pelo APT:** consulta se um pacote está disponível ou instalado nos repositórios configurados do Debian.
- **Instalar e remover:** operações de gerenciamento de pacotes integradas ao APT; em testes na VM, o **Geany foi instalado e desinstalado com sucesso**.
- **Aplicativos externos:** suporte ao **Flatpak/Flathub** como opção complementar. A origem do aplicativo é indicada, inclusive quando o pacote é distribuído por terceiros.
- **Página de detalhes:** descrição, origem, identificador, versão instalada/disponível, tamanho quando conhecido e informações de compatibilidade.
- **Aplicativos instalados:** uma aba que reúne programas detectados no sistema e exibe versão, origem e tamanho quando disponíveis.
- **Configurações:** controles de integração com Flatpak e de catálogo. O catálogo local utilizado nos testes apresentou **verificação de assinatura Ed25519** na interface.

### Escolha de aplicativos de acordo com o hardware

A loja apresenta indicações de consumo, como **leve** e **moderado**, levando em conta o foco da distribuição em PCs antigos. Programas que pedem mais recursos recebem avisos, mas a decisão de instalar continua com o usuário.

<div align="center">
  <a href="docs/imagens/02-pdti-store-explorar.webp"><img src="docs/imagens/02-pdti-store-explorar.webp" alt="PDTI Store com catálogo, ícones e indicação de consumo de recursos" width="460"></a>
  <p><sub>Catálogo da PDTI Store em teste — aplicativos reconhecidos com ícones e indicação de disponibilidade.</sub></p>
</div>

> **Estado atual:** as funcionalidades APT e a interface foram exercitadas em máquina virtual. **O Flathub automático em instalação limpa foi testado com sucesso**, conforme confirmação do mantenedor: a loja reconheceu o repositório sem configuração manual. A instalação de cada aplicativo Flatpak ainda exige testes individuais; a presença no catálogo não garante disponibilidade em todas as arquiteturas.

## AutoTune — otimização inteligente

O **PDTI Revive AutoTune** é o componente que adapta os ajustes do sistema ao computador. Seu objetivo é **priorizar fluidez e uso consciente de memória**, sobretudo em equipamentos antigos, sem exigir que o usuário conheça cada configuração do Linux.

### Como funciona

**1. Identifica o hardware.** A interface apresenta dados como processador, quantidade de memória RAM, tipo de armazenamento e características gráficas.

**2. Seleciona um perfil.** O AutoTune usa as informações detectadas para recomendar ou aplicar um perfil de otimização. A interface permite visualizar o **modo automático** e o **modo manual**, além de exibir a pontuação calculada para o equipamento.

**3. Mostra o que foi ajustado.** Em vez de esconder as alterações, a central lista as otimizações ativas e os avisos pertinentes.

**4. Oferece controle ao usuário.** A interface inclui a opção de restaurar configurações originais. Algumas alterações, especialmente relacionadas à memória de troca, podem exigir reinicialização.

### Exemplo real de teste

Em uma máquina virtual de teste com aproximadamente **2 GB de RAM** e armazenamento identificado como **HDD**, o AutoTune selecionou o **perfil Econômico** e apresentou as seguintes otimizações:

| Área | Ajuste mostrado no teste | Objetivo |
| :--- | :--- | :--- |
| Interface | Compositor e efeitos visuais desativados | Reduzir trabalho gráfico e consumo de memória |
| Memória | ZRAM configurada com compressão **zstd** | Ajudar a aproveitar melhor a RAM disponível |
| Disco | Ajustes no despejo de páginas de memória modificadas | Melhorar o comportamento de escrita em disco lento |
| Arquivos | Limite para miniaturas locais | Reduzir trabalho adicional no gerenciador de arquivos |
| Proteção | Regra para RAM crítica | Evitar um perfil inadequado quando há pouca memória |

<div align="center">
  <a href="docs/imagens/04-autotune.webp"><img src="docs/imagens/04-autotune.webp" alt="AutoTune exibindo hardware detectado, perfil econômico e ajustes ativos" width="440"></a>
  <p><sub>AutoTune em funcionamento na VM, com hardware identificado, perfil ativo e explicação dos ajustes.</sub></p>
</div>

> **Importante:** o AutoTune não aumenta a capacidade física do computador nem garante ganhos de velocidade em qualquer cenário. O efeito de cada ajuste depende do hardware e dos programas utilizados. O comportamento das regras ainda faz parte dos testes de homologação.

## Edições

| **Lite** | **Standard** |
| :--- | :--- |
| Pensada para computadores modestos e uso com menos recursos. | Pensada para quem busca uma experiência mais completa no uso diário. |
| Prioriza economia de memória e fluidez. | Reúne mais recursos e aplicativos. |
| Compartilha a PDTI Store e o AutoTune. | Compartilha a PDTI Store e o AutoTune. |

> A compatibilidade e o desempenho dependem do hardware. Os requisitos mínimos definitivos serão publicados após os testes de homologação.

## Capturas de tela

As imagens abaixo são de testes da **PDTI Revive 0.3.1** em máquina virtual. Clique em cada uma para visualizar em tamanho maior.

<table>
  <tr>
    <td align="center" width="50%">
      <a href="docs/imagens/02-pdti-store-explorar.webp"><img src="docs/imagens/02-pdti-store-explorar.webp" alt="PDTI Store com categorias, pesquisa e aplicativos disponíveis" width="340"></a><br>
      <strong>PDTI Store · Explorar aplicativos</strong>
    </td>
    <td align="center" width="50%">
      <a href="docs/imagens/03-pdti-store-instalados.webp"><img src="docs/imagens/03-pdti-store-instalados.webp" alt="PDTI Store com relação de programas instalados" width="340"></a><br>
      <strong>PDTI Store · Aplicativos instalados</strong>
    </td>
  </tr>
  <tr>
    <td align="center" colspan="2">
      <a href="docs/imagens/04-autotune.webp"><img src="docs/imagens/04-autotune.webp" alt="AutoTune mostrando informações do hardware e perfil econômico" width="390"></a><br>
      <strong>AutoTune · Otimização conforme o hardware</strong>
    </td>
  </tr>
</table>

<sub>Capturas demonstrativas. O papel de parede e marcas de aplicativos podem estar sujeitos a direitos de terceiros.</sub>

## Status do projeto

**Versão em teste: 0.3.1 · PDTI Store 0.3.1-5**

| Marco | Situação |
| :--- | :--- |
| Compilação das ISOs Lite e Standard | Concluída |
| Testes em instalação limpa das edições Lite e Standard | **Confirmado** |
| Flatpak instalado nas imagens | Confirmado nos logs de build |
| Integridade dos artefatos com SHA-256 | Verificada |
| Testes da loja e do AutoTune em VM | Realizados parcialmente |
| Flathub automático em instalação limpa | **Validado em teste de instalação limpa** |
| Revisão das licenças dos ícones e homologação geral | Pendente |

As imagens e o pacote da loja foram arquivados com verificações de integridade. **Ainda não há um download público homologado neste repositório.**

<details>
<summary><strong>Ver hashes SHA-256 dos artefatos 0.3.1</strong></summary>

| Artefato | SHA-256 |
| :--- | :--- |
| `pdti-store_0.3.1-5_all.deb` | `d23d28a6499f6936736a8c1023a81edfcb8a6d83bfce7933836b63703df6fd0c` |
| `pdti-revive-lite-amd64-0.3.1-final.iso` | `a8a1fe52f8eba3b2f39c77dbfe1cddc554dc04956103888151ef724db6a69fb3` |
| `pdti-revive-standard-amd64-0.3.1-final.iso` | `6c6c30b274a429cb4484d8755bfdb20fd38fc02b5b78cf1685f606361c02e238` |

Os hashes verificam a integridade dos arquivos; não representam homologação funcional nem assinatura criptográfica de release.

</details>

## Próximas etapas

- [x] Finalizar testes limpos das edições **Lite** e **Standard**.
- [x] Validar o **Flathub no primeiro acesso** sem configuração manual (teste confirmado pelo mantenedor).
- [ ] Revisar as licenças dos ícones e outros recursos incorporados.
- [ ] Publicar o código-fonte, os testes e os scripts de build após auditoria.
- [ ] Preparar as primeiras **Releases** públicas acompanhadas de instruções e checksums.

## Desenvolvimento e documentação

O repositório está sendo estruturado de forma gradual. Consulte o [histórico de alterações](CHANGELOG.md) e a [galeria de imagens](docs/imagens/ORIGEM.md).

As ISOs, discos virtuais e diretórios temporários de compilação ficam fora do histórico Git; o objetivo é manter o repositório dedicado ao código-fonte e à documentação.

## Licenciamento

A licença geral do código ainda não foi definida. Ícones, marcas, temas e outros componentes de terceiros obedecem às suas respectivas licenças. Materiais pendentes de revisão não serão oferecidos como redistribuição pública.

---

<div align="center">

**PDTI Revive** · Desenvolvido e mantido por [Yagami-Murakami](https://github.com/Yagami-Murakami)

*Tecnologia acessível. Mais possibilidades para o hardware que você já tem.*

</div>

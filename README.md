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

[Visão geral](#visão-geral) · [Recursos](#principais-recursos) · [Edições](#edições) · [Capturas](#capturas-de-tela) · [Status](#status-do-projeto) · [Próximas etapas](#próximas-etapas)

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
| Flatpak instalado nas imagens | Confirmado nos logs de build |
| Integridade dos artefatos com SHA-256 | Verificada |
| Testes da loja e do AutoTune em VM | Realizados parcialmente |
| Flathub automático em instalação limpa | Validação pendente |
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

- [ ] Finalizar testes limpos das edições **Lite** e **Standard**.
- [ ] Validar o **Flathub no primeiro acesso** sem configuração manual.
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

# PDTI Revive

Distribuição Linux em desenvolvimento, baseada no **Debian 13 (Trixie)** e no ambiente gráfico **Xfce**, com foco em facilitar o uso de computadores antigos e proporcionar uma experiência amigável.

> **Status: pré-lançamento / homologação.** As imagens ISO 0.3.1 foram compiladas e verificadas por SHA-256, mas ainda exigem testes completos em instalações limpas (Lite e Standard), revisão das licenças dos ícones incorporados e validação do Flathub automático antes da distribuição pública.

## Edições

- **Lite:** perfil pensado para máquinas mais modestas.
- **Standard:** perfil com mais recursos para uso diário.

## Funcionalidades em desenvolvimento

- **PDTI Store 0.3.1-5:** catálogo de aplicativos, busca e estados de disponibilidade, detalhes dos programas, integração com APT e Flatpak/Flathub.
- **AutoTune:** ajustes de perfil conforme as características do hardware.
- Ícones de aplicativos com fallback local e suporte a cache AppStream.
- Ferramentas de compilação e remasterização de ISOs híbridas BIOS/UEFI.

## Progresso da versão 0.3.1

As duas imagens (Lite e Standard) foram compiladas com a PDTI Store 0.3.1-5 e o Flatpak no sistema. O usuário confirmou a verificação do manifesto SHA-256:

| Artefato | SHA-256 |
| --- | --- |
| `pdti-store_0.3.1-5_all.deb` | `d23d28a6499f6936736a8c1023a81edfcb8a6d83bfce7933836b63703df6fd0c` |
| `pdti-revive-lite-amd64-0.3.1-final.iso` | `a8a1fe52f8eba3b2f39c77dbfe1cddc554dc04956103888151ef724db6a69fb3` |
| `pdti-revive-standard-amd64-0.3.1-final.iso` | `6c6c30b274a429cb4484d8755bfdb20fd38fc02b5b78cf1685f606361c02e238` |

**Integridade do arquivo não significa homologação funcional ou aprovação para distribuição.**

## Código e builds

Este repositório está sendo estruturado. Serão adicionados os fontes revisados, testes, documentação e scripts de construção após auditoria. As ISOs, discos virtuais, raízes de sistema temporárias e pacotes gerados **não devem ser commitados no Git**.

Antes de executar scripts de remasterização, leia a documentação, revise os destinos de escrita e use um ambiente de teste. Não execute builds desconhecidos com privilégios de administrador.

## Licenças e terceiros

A licença geral do projeto ainda será definida. **Não há concessão explícita de licença para reutilização do código neste momento.** Imagens e marcas de terceiros, incluindo ícones recolhidos do AppStream, têm licenças próprias e não serão redistribuídos no repositório antes de revisão. Debian, Xfce, Flatpak e nomes de aplicativos pertencem aos respectivos projetos.

<!-- PDTI-GALERIA-INICIO -->
## Capturas de tela

Imagens de testes da **PDTI Revive 0.3.1** em máquina virtual. Clique para ampliar.

<table>
<tr>
<td align="center" width="50%">
<strong>Área de trabalho Xfce</strong><br>
<a href="docs/imagens/01-area-de-trabalho.webp"><img src="docs/imagens/01-area-de-trabalho.webp" alt="Área de trabalho da PDTI Revive com Xfce" width="420"></a>
</td>
<td align="center" width="50%">
<strong>PDTI Store — Explorar</strong><br>
<a href="docs/imagens/02-pdti-store-explorar.webp"><img src="docs/imagens/02-pdti-store-explorar.webp" alt="PDTI Store mostrando categorias, aplicativos e ícones" width="340"></a>
</td>
</tr>
<tr>
<td align="center" width="50%">
<strong>PDTI Store — Instalados</strong><br>
<a href="docs/imagens/03-pdti-store-instalados.webp"><img src="docs/imagens/03-pdti-store-instalados.webp" alt="PDTI Store listando aplicativos instalados" width="340"></a>
</td>
<td align="center" width="50%">
<strong>AutoTune — Otimização de hardware</strong><br>
<a href="docs/imagens/04-autotune.webp"><img src="docs/imagens/04-autotune.webp" alt="AutoTune detectando hardware e aplicando perfil econômico" width="340"></a>
</td>
</tr>
</table>

*As capturas mostram o projeto em desenvolvimento. O plano de fundo e as marcas de aplicativos podem pertencer a terceiros.*
<!-- PDTI-GALERIA-FIM -->

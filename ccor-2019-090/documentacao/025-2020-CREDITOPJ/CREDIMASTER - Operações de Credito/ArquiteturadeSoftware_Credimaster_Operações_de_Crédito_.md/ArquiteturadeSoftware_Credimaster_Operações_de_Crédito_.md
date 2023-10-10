<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Documento de Arquitetura de Software</strong></td>
</tr>
<tr class="even">
<td>CREDIMASTER – Operações de Crédito</td>
</tr>
<tr class="odd">
<td></td>
</tr>
<tr class="even">
<td><p>Autor: <strong>Jennifer Alves, Lucas Nunes</strong></p>
<p>E-mail: <a href="mailto:jennifer.alves@pdcase.com.br"><strong>jennifer.alves@pdcase.com.br</strong></a></p>
<p><strong><u>lucas.nunes@pdcase.com.br</u></strong></p></td>
</tr>
<tr class="odd">
<td></td>
</tr>
</tbody>
</table>

# Histórico de REVISÕES

| **Data**   | **Versão** | **Descrição**           | **Autor**                    |
|------------|------------|-------------------------|------------------------------|
| 27/09/2023 | 0.1        | Elaboração do documento | Jennifer Alves / Lucas Nunes |
|            |            |                         |                              |
|            |            |                         |                              |

# 

# Sumário

[Histórico de REVISÕES [2](#histórico-de-revisões)](#histórico-de-revisões)

[Sumário [3](#_Toc88575086)](#_Toc88575086)

[1. INTRODUÇÃO [4](#introdução)](#introdução)

[1.1. Finalidade [4](#_Toc88575088)](#_Toc88575088)

[1.2. Escopo [4](#_Toc88575089)](#_Toc88575089)

[1.3. Definições, Acrônimos e Abreviações [4](#_Toc131243936)](#_Toc131243936)

[1.4. Referências [4](#referências)](#referências)

[2. DESCRIÇÃO DO PRODUTO [4](#descrição-do-produto)](#descrição-do-produto)

[3. REPRESENTAÇÃO ARQUITETURAL [4](#representação-arquitetural)](#representação-arquitetural)

[3.1. Diagramas C4 [4](#diagramas-c4)](#diagramas-c4)

[3.1.1. Diagrama de Contexto [4](#diagrama-de-contexto)](#diagrama-de-contexto)

[3.1.2. Diagrama de Container [4](#diagrama-de-container)](#diagrama-de-container)

[3.1.3. Diagrama de Componente [4](#diagrama-de-componente)](#diagrama-de-componente)

[4. METAS E RESTRIÇÕES ARQUITETURAIS [4](#metas-e-restrições-arquiteturais)](#metas-e-restrições-arquiteturais)

[4.1. Justificativas da Arquitetura Adotada [4](#_Toc88575099)](#_Toc88575099)

[4.2. Metas e Restrições Técnicas [5](#_Toc88575100)](#_Toc88575100)

[4.3. Tecnologias Utilizadas [5](#tecnologias-utilizadas)](#tecnologias-utilizadas)

[4.4. Impactos no Ambiente e Legados [5](#impactos-no-ambiente-e-legados)](#impactos-no-ambiente-e-legados)

[5. APROVAÇÃO DAS PARTES INTERESSADAS [5](#aprovação-das-partes-interessadas)](#aprovação-das-partes-interessadas)

# INTRODUÇÃO

<span id="_Toc88575088" class="anchor"></span>

## Finalidade

<span id="_Toc88575089" class="anchor"></span>

Este documento visa descrever informações relevantes para uma visão geral da arquitetura do sistema CREDIMASTER – Operações de Crédito, do Banco do Estado do Pará, bem como apresentar padrões adotados no seu desenvolvimento. Objetiva também servir como meio de comunicação entre a equipe técnica e membros da equipe do Banco, a fim de facilitar e apoiar decisões em melhorias ou atendimento de demandas legais, que venham a ser necessárias para o mesmo.

Além disso, neste documento serão detalhadas integrações, estruturas internas, metas, restrições e objetivos, buscando esclarecer o seu funcionamento e dependências internas e externas, através de tabelas e diagramas.

## Escopo

<span id="_Toc131243936" class="anchor"></span>

O modelo arquitetural adotado engloba toda a estrutura de acesso a dados e camadas de negócio, neste caso adotado para o desenvolvimento ou manutenção de funcionalidades no sistema .

As práticas e padrões utilizados estão descritos na seção Metas e restrições arquiteturais.

## Definições, Acrônimos e Abreviações

CREDIMASTER– Operações de Crédito

## Referências

Não possui referências externas.

# DESCRIÇÃO DO PRODUTO

CREDIMASTER - módulo Operações de Crédito, onde permite o usuário solicitar e renegociar Operações de Crédito para clientes do tipo Pessoa Jurídica -PJ.

# REPRESENTAÇÃO ARQUITETURAL

<img src="C:\Users\MICRO\Downloads\entregas\banpara\documantacao\ccor-2019-090\documentacao\025-2020-CREDITOPJ\CREDIMASTER - Operações de Credito\ArquiteturadeSoftware_Credimaster_Operações_de_Crédito_.md\media/media/image1.png" style="width:4.54236in;height:6.83542in" />

Figura 1 – Visão arquitetural do CREDIMASTER – Operações de Crédito

## Diagramas C4

## Diagrama de Contexto

<img src="C:\Users\MICRO\Downloads\entregas\banpara\documantacao\ccor-2019-090\documentacao\025-2020-CREDITOPJ\CREDIMASTER - Operações de Credito\ArquiteturadeSoftware_Credimaster_Operações_de_Crédito_.md\media/media/image2.png" style="width:7.26806in;height:4.26806in" />

Figura 1 – Diagrama de contexto

## Diagrama de Container

Não se aplica.

## Diagrama de Componente

Não se aplica.

# METAS E RESTRIÇÕES ARQUITETURAIS

<span id="_Toc88575099" class="anchor"></span>

O software tem como requisitos básicos a segurança e privacidade dos dados, devido a utilização dos mesmos para a realização de pagamentos de diversos tipos de créditos e benefícios.

No CREDIMASTER – Operações de Crédito o código é legado e possui mais de 11 anos desde sua versão inicial que veio sendo mantida por diferentes contratos e empresas desde então. Ele possui um design de arquitetura distribuída e utiliza de ferramentas (*Intellij*, bibliotecas e linguagens) de domínio público como *Java, html, Javascript*, etc e de domínio particular usando o framework Summer, Hydra. Sendo que o foco do sistema está no seu uso de forma para o usuário.

## Justificativas da Arquitetura Adotada

<span id="_Toc88575100" class="anchor"></span>

A arquitetura distribuída adotada pelo CREDIMASTER – Operações de Crédito foi uma decisão em conjunto da equipe de desenvolvimento da empresa com a equipe de segurança do banco na época de sua criação visando garantir que o servidor web tivesse acessos ao banco de dados com segurança e dessa forma o servidor de aplicação foi criado com a tecnologia existente na época, Metas e Restrições Técnicas

## Tecnologias Utilizadas

| **NOME**       | **VERSÃO BASE** | **OBJETIVO**                                    |
|----------------|-----------------|-------------------------------------------------|
| Java           |                 | Maquina Virtual Java                            |
| Summer         |                 | Framework de desenvolvimento proprietário       |
| Jboss          |                 | Servidor de aplicação web                       |
| Jasper Reports |                 | Biblioteca utilizada para geração de relatórios |
| Hydra          |                 | Framework de desenvolvimento proprietário       |

## Impactos no Ambiente e Legados 

O CREDIMASTER – Operações de Crédito roda atualmente em um servidor dedicado, e possui acesso ao banco de dados SQL SERVER no cluster 02. Possui integrações diretas com o Sistemas: Conta Corrente, Grisco e SGG.

# APROVAÇÃO DAS PARTES INTERESSADAS

| Data: \_\_\_\_\_/\_\_\_\_\_/\_\_\_\_\_\_\_\_                           | Data: \_\_\_\_\_/\_\_\_\_\_/\_\_\_\_\_\_\_\_                           |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |

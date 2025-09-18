
---

# 📘 Trabalho de Engenharia de Software

## Estrutura de Armazenamento de Massa com foco em Estrutura RAID

---

### 1. Introdução

A evolução dos sistemas computacionais trouxe consigo um crescimento exponencial na geração e armazenamento de dados. Desde pequenas aplicações até ambientes corporativos de grande escala, a forma como os dados são armazenados e recuperados impacta diretamente o desempenho, a confiabilidade e a disponibilidade dos sistemas.

Nesse contexto, o armazenamento em massa desempenha papel central, sendo geralmente baseado em discos magnéticos ou dispositivos de estado sólido. Para otimizar a utilização desses dispositivos, tanto em termos de **desempenho** quanto de **tolerância a falhas**, surgiu o conceito de **RAID (Redundant Array of Independent/Inexpensive Disks)**.

Este trabalho tem como objetivo analisar os principais conceitos relacionados ao armazenamento de massa, com ênfase na estrutura RAID, apresentando seus níveis, vantagens, desvantagens e aplicações práticas.

---

### 2. Conceitos Fundamentais de Armazenamento de Massa

O **armazenamento em massa** é responsável por guardar permanentemente programas e dados. Historicamente, os discos magnéticos foram a tecnologia predominante, organizados em **trilhas, setores e blocos**, que formam a base lógica para a leitura e escrita de informações.

A estrutura do disco e as estratégias de gerenciamento adotadas pelo sistema operacional influenciam diretamente o tempo de resposta e o throughput das operações de I/O (entrada/saída).

Além disso, novos dispositivos como os **SSDs (Solid-State Drives)** introduziram melhorias significativas em desempenho, embora com custos mais elevados.

---

### 3. Estrutura RAID

O **RAID** consiste em uma técnica que combina múltiplos discos físicos em uma única unidade lógica, com o objetivo de melhorar desempenho, aumentar a confiabilidade ou ambos.

Existem duas formas principais de implementação:

* **RAID por hardware**: realizado por controladores dedicados, que oferecem maior desempenho e transparência para o sistema.
* **RAID por software**: implementado pelo sistema operacional, mais econômico, porém com maior consumo de recursos computacionais.

A avaliação de cada nível de RAID é feita com base em três critérios principais:

* **Desempenho** (velocidade de leitura e escrita);
* **Custo** (quantidade de discos e recursos necessários);
* **Tolerância a falhas** (capacidade de continuar operando mesmo após falhas de hardware).

---

### 4. Níveis de RAID

#### RAID 0 – Striping

* **Funcionamento**: os dados são distribuídos em blocos entre vários discos, sem redundância.
* **Vantagem**: alto desempenho em leitura e escrita.
* **Desvantagem**: ausência total de tolerância a falhas; a perda de um disco implica perda de todos os dados.
* **Aplicação**: sistemas que priorizam velocidade em detrimento da confiabilidade.

#### RAID 1 – Espelhamento (Mirroring)

* **Funcionamento**: cada dado é gravado simultaneamente em dois discos.
* **Vantagem**: alta confiabilidade e leitura mais rápida.
* **Desvantagem**: custo elevado (necessita o dobro de discos).
* **Aplicação**: servidores críticos de banco de dados.

#### RAID 2 – Bit-Level Striping com ECC

* **Funcionamento**: divide os dados em nível de bits e utiliza códigos de correção de erro.
* **Vantagem**: alta correção de falhas.
* **Desvantagem**: custo muito alto; pouco usado na prática.

#### RAID 3 – Byte-Level Striping com Disco de Paridade

* **Funcionamento**: distribuição de dados em nível de bytes, com um disco dedicado à paridade.
* **Vantagem**: boa taxa de transferência.
* **Desvantagem**: gargalo no disco de paridade.

#### RAID 4 – Block-Level Striping com Disco de Paridade

* **Funcionamento**: dados distribuídos em blocos, com disco exclusivo para paridade.
* **Vantagem**: permite leituras independentes.
* **Desvantagem**: gargalo no disco de paridade.

#### RAID 5 – Block-Level Striping com Paridade Distribuída

* **Funcionamento**: dados e paridade distribuídos entre todos os discos.
* **Vantagem**: equilíbrio entre desempenho e tolerância a falhas.
* **Desvantagem**: desempenho em escrita inferior ao RAID 0.
* **Aplicação**: servidores corporativos e aplicações de alta disponibilidade.

#### RAID 6 – Striping com Dupla Paridade

* **Funcionamento**: semelhante ao RAID 5, mas armazena duas informações de paridade.
* **Vantagem**: suporta falha de até dois discos.
* **Desvantagem**: menor desempenho em escrita devido ao cálculo extra.
* **Aplicação**: data centers e sistemas críticos que exigem alta tolerância a falhas.

#### RAID 10 (RAID 1+0)

* **Funcionamento**: combina espelhamento (RAID 1) com striping (RAID 0).
* **Vantagem**: alta performance e alta confiabilidade.
* **Desvantagem**: custo elevado (mínimo 4 discos).
* **Aplicação**: bancos de dados de missão crítica e aplicações de alto desempenho.

---

### 5. Estudo de Caso / Análise Crítica

1. **Servidor de banco de dados crítico**

   * Melhor escolha: **RAID 10**, pois garante tanto velocidade quanto confiabilidade.

2. **Sistema doméstico de baixo custo**

   * Melhor escolha: **RAID 0** (se desempenho for prioridade) ou **RAID 1** (se a confiabilidade for mais importante).

3. **Data center de alta disponibilidade**

   * Melhor escolha: **RAID 6**, pela capacidade de suportar a falha simultânea de dois discos com custo relativamente otimizado.

---

### 6. Conclusão

A análise da **estrutura de armazenamento de massa** evidencia a importância de mecanismos que conciliem **desempenho** e **segurança dos dados**. O **RAID** surge como solução eficiente para diferentes contextos, desde ambientes domésticos até sistemas corporativos de alta criticidade.

A escolha do nível de RAID deve sempre considerar os objetivos do sistema, o orçamento disponível e a criticidade das informações armazenadas. Assim, profissionais de engenharia de software precisam compreender profundamente essas estruturas para projetar sistemas robustos e eficientes.

---

### 7. Referências

* SILBERSCHATZ, A.; GALVIN, P. B.; GAGNE, G. **Fundamentos de Sistemas Operacionais**. 9. ed. Rio de Janeiro: LTC, 2015. Capítulo 10, Seção 10.7.
* PATTERSON, D. A.; GIBSON, G.; KATZ, R. H. A case for redundant arrays of inexpensive disks (RAID). *ACM SIGMOD*, 1988.
* Documentações técnicas de fabricantes (Dell, HP, IBM, Intel).

---


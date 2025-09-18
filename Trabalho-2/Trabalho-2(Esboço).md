# Trabalho de Engenharia de Software

## Tema: Máquinas Virtuais

### 1. Introdução

As máquinas virtuais (MVs) constituem uma das tecnologias mais importantes no contexto da computação moderna. Elas permitem a execução de múltiplos sistemas operacionais e aplicações de forma isolada em um mesmo hardware físico, otimizando o uso de recursos e oferecendo flexibilidade. Historicamente, a ideia de virtualização surgiu nos mainframes da IBM nos anos 1960, quando havia a necessidade de compartilhar poder computacional entre diversos usuários. Hoje, as MVs estão presentes desde o desenvolvimento de software até a computação em nuvem.

### 2. Conceitos Fundamentais

Uma máquina virtual é uma abstração do hardware físico, criada por uma camada de software conhecida como hypervisor. Existem dois tipos principais de virtualização:

* **Máquinas Virtuais de Sistema**: simulam um computador inteiro, permitindo executar múltiplos sistemas operacionais. Exemplos: VMware, VirtualBox, Hyper-V.
* **Máquinas Virtuais de Processo**: fornecem um ambiente de execução para aplicações específicas, independente do sistema operacional subjacente. Exemplos: Java Virtual Machine (JVM), Common Language Runtime (CLR).

A virtualização pode ser de **hardware**, quando simula recursos físicos, ou de **software**, quando oferece um ambiente abstrato para programas.

### 3. Componentes e Funcionamento

O funcionamento de uma MV envolve:

* **Hypervisor**: software responsável por gerenciar as MVs. Pode ser:

  * **Tipo 1 (bare-metal)**: executado diretamente no hardware (ex.: VMware ESXi, Microsoft Hyper-V Server).
  * **Tipo 2 (hospedado)**: executado sobre um sistema operacional (ex.: VirtualBox, VMware Workstation).
* **Gerenciamento de recursos**: o hypervisor distribui CPU, memória, armazenamento e dispositivos de I/O entre as MVs.
* **Interação**: o SO hospedeiro controla o hardware, enquanto o SO convidado (guest) é executado dentro da MV como se estivesse em um computador físico.

### 4. Vantagens e Desvantagens

**Vantagens:**

* Isolamento entre sistemas e aplicações.
* Portabilidade e escalabilidade.
* Redução de custos com hardware.
* Flexibilidade para testes e desenvolvimento.

**Desvantagens:**

* Overhead de desempenho devido à camada extra de virtualização.
* Complexidade de gerenciamento.
* Necessidade de hardware robusto para suportar múltiplas MVs.

### 5. Aplicações Práticas

* **Ambientes de teste e desenvolvimento**: criação de múltiplos cenários em um único hardware.
* **Computação em nuvem**: base da infraestrutura de provedores como AWS, Azure e Google Cloud.
* **Segurança**: isolamento de aplicações potencialmente maliciosas.
* **Containers x Máquinas Virtuais**: enquanto containers compartilham o mesmo kernel, MVs simulam um sistema completo. Containers são mais leves, mas MVs oferecem maior isolamento.

### 6. Estudo de Caso

#### VMware Workstation

* **Arquitetura**: hypervisor tipo 2, executado sobre um sistema hospedeiro.
* **Características**: suporte a múltiplos sistemas operacionais convidados, snapshots de estados da MV, integração com rede e dispositivos USB.
* **Exemplo de uso**: amplamente utilizado em empresas para testes de compatibilidade de software em diferentes ambientes.

#### Docker (comparação)

* **Arquitetura**: utiliza containers, compartilhando o kernel do SO.
* **Características**: leve, rápido para iniciar e ideal para aplicações distribuídas.
* **Exemplo de uso**: plataformas de microserviços na nuvem.

### 7. Conclusão

As máquinas virtuais são uma tecnologia essencial para a Engenharia de Software, proporcionando flexibilidade, isolamento e otimização de recursos. Apesar de apresentarem sobrecarga de desempenho, sua importância em áreas como computação em nuvem, segurança e desenvolvimento é indiscutível. O futuro aponta para soluções híbridas, integrando VMs e containers, permitindo que cada abordagem seja aplicada de acordo com a necessidade do ambiente.

### 8. Referências

* SILBERSCHATZ, Abraham; GALVIN, Peter Baer; GAGNE, Greg. *Fundamentos de Sistemas Operacionais*. 9. ed. Rio de Janeiro: LTC, 2015. Capítulo 16.
* ROSENBLUM, M.; GARFINKEL, T. Virtual Machine Monitors: Current Technology and Future Trends. *IEEE Computer*, 2005.
* RED HAT. *What is virtualization?*. Disponível em: [https://www.redhat.com/en/topics/virtualization](https://www.redhat.com/en/topics/virtualization). Acesso em: ago. 2025.
* VMWARE. *VMware Workstation Pro Documentation*. Disponível em: [https://www.vmware.com/](https://www.vmware.com/). Acesso em: ago. 2025.

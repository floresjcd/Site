
---

# Questões Discursivas sobre Máquinas Virtuais

### Introdução

1. **O que são máquinas virtuais (MVs)?**  
   São abstrações do hardware físico criadas por software, permitindo executar sistemas operacionais e aplicações de forma isolada em um mesmo equipamento.

2. **Qual foi a motivação histórica para o surgimento das MVs?**  
   Surgiram nos anos 1960 em mainframes da IBM para compartilhar recursos computacionais entre múltiplos usuários.

3. **Por que as MVs são importantes para a Engenharia de Software?**  
   Porque permitem criar ambientes de teste, desenvolvimento e produção isolados, flexíveis e de baixo custo.

4. **Qual a principal diferença entre máquinas virtuais e computadores físicos?**  
   As MVs são abstrações virtuais do hardware, enquanto computadores físicos possuem componentes reais.

5. **Qual o impacto da virtualização na computação moderna?**  
   Tornou possível a consolidação de servidores, a computação em nuvem e novos modelos de distribuição de software.

---

### Conceitos Fundamentais

6. **O que diferencia máquinas virtuais de sistema e de processo?**  
   De sistema simulam um computador inteiro; de processo criam um ambiente de execução para uma aplicação.

7. **Dê exemplos de máquinas virtuais de sistema.**
   VMware, VirtualBox, Hyper-V.

8. **Dê exemplos de máquinas virtuais de processo.**
   Java Virtual Machine (JVM), Common Language Runtime (CLR).

9. **O que significa virtualização de hardware?**  
   É a simulação de recursos físicos como CPU, memória e dispositivos.

10. **O que significa virtualização de software?**  
    É a criação de ambientes de execução abstratos para aplicações, sem simulação direta do hardware.

---

### Componentes e Funcionamento

11. **O que é um hypervisor?**  
    É o software que gerencia máquinas virtuais, controlando o uso de recursos de hardware.

12. **Quais os tipos de hypervisores?**  
    Tipo 1 (bare-metal) e Tipo 2 (hospedado).

13. **O que caracteriza o hypervisor tipo 1?**  
    Executa diretamente sobre o hardware, sem depender de um sistema operacional hospedeiro.

14. **O que caracteriza o hypervisor tipo 2?**  
    Roda sobre um sistema operacional hospedeiro, como uma aplicação.

15. **Dê exemplos de hypervisores tipo 1.**
    VMware ESXi, Microsoft Hyper-V Server, Xen.

16. **Dê exemplos de hypervisores tipo 2.**
    VirtualBox, VMware Workstation.

17. **Como o hypervisor gerencia os recursos do sistema?**  
    Ele aloca CPU, memória, disco e dispositivos de entrada/saída entre as MVs de forma controlada.

18. **Qual a relação entre SO hospedeiro e SO convidado?**  
    O hospedeiro gerencia o hardware real, enquanto o convidado roda dentro da MV como se tivesse acesso direto ao hardware.

19. **O que são snapshots em máquinas virtuais?**  
    São capturas do estado de uma MV que permitem voltar a um ponto anterior.

20. **Qual a importância da emulação de hardware em MVs?**  
    Permite que sistemas diferentes rodem sem modificações, independentemente do hardware físico.

---

### Vantagens e Desvantagens

21. **Quais as principais vantagens das MVs?**  
    Isolamento, flexibilidade, portabilidade, redução de custos.

22. **Quais as principais desvantagens das MVs?**  
    Overhead de desempenho, maior complexidade de gerenciamento e necessidade de hardware robusto.

23. **Por que as MVs são consideradas seguras?**  
    Porque isolam aplicações e sistemas, impedindo que falhas se propaguem para outras MVs ou para o hospedeiro.

24. **Como as MVs contribuem para redução de custos?**  
    Ao permitir consolidar vários sistemas em um único servidor físico, economizando hardware e energia.

25. **Por que pode haver perda de desempenho em MVs?**  
    Porque existe uma camada extra de virtualização que adiciona overhead no acesso ao hardware.

---

### Aplicações Práticas

26. **Como as MVs são usadas em desenvolvimento de software?**  
    Criando ambientes de teste isolados que replicam sistemas de produção.

27. **Como as MVs são aplicadas na computação em nuvem?**  
    Servem como base para infraestrutura como serviço (IaaS), permitindo provisionamento dinâmico de recursos.

28. **Por que MVs são úteis em segurança?**  
    Permitem rodar softwares suspeitos em ambientes isolados sem comprometer o sistema principal.

29. **Qual a diferença entre MVs e containers?**  
    Containers compartilham o kernel do SO, enquanto MVs simulam um sistema completo.

30. **Quando containers são mais vantajosos que MVs?**  
    Em aplicações que exigem inicialização rápida e menor consumo de recursos.

---

### Estudo de Caso

31. **Qual o tipo de hypervisor utilizado pelo VMware Workstation?**  
    Hypervisor tipo 2 (hospedado).

32. **Quais as principais funcionalidades do VMware Workstation?**  
    Suporte a múltiplos SOs convidados, snapshots, integração com dispositivos e rede.

33. **Em que cenários o VMware Workstation é mais utilizado?**  
    Testes de compatibilidade e ambientes de desenvolvimento.

34. **O que diferencia o Docker de uma MV tradicional?**  
    O Docker usa containers que compartilham o kernel do hospedeiro, enquanto uma MV simula um sistema completo.

35. **Por que o Docker é preferido em arquiteturas de microserviços?**  
    Porque é leve, rápido de inicializar e facilita a escalabilidade de aplicações distribuídas.

---

### Conclusão e Perspectivas Futuras

36. **Por que MVs continuam relevantes mesmo com o avanço dos containers?**  
    Porque oferecem maior isolamento e permitem rodar sistemas operacionais distintos.

37. **Qual o papel das MVs em provedores de nuvem?**  
    São a base para serviços de infraestrutura, permitindo provisionamento de servidores virtuais sob demanda.

38. **Como MVs e containers podem ser usados de forma complementar?**  
    Containers podem rodar dentro de MVs para combinar isolamento e leveza.

39. **Qual a principal tendência para o futuro da virtualização?**  
    O uso integrado de VMs e containers em ambientes híbridos e distribuídos.

40. **Por que o estudo de MVs é essencial na formação em Engenharia de Software?**  
    Porque fornece base para compreender infraestrutura de TI moderna, nuvem e segurança.

---

### Questões Avançadas

41. **Explique como o hypervisor garante isolamento entre MVs.**
    Ele cria ambientes independentes com recursos alocados separadamente, impedindo interferências diretas.

42. **Qual a relação entre virtualização e cloud computing?**  
    A virtualização é a base técnica que permite a existência da computação em nuvem.

43. **O que é paravirtualização?**  
    É uma técnica em que o SO convidado é modificado para interagir melhor com o hypervisor, aumentando desempenho.

44. **Explique o conceito de virtualização aninhada.**
    É a capacidade de executar uma MV dentro de outra MV.

45. **Quais são os impactos ambientais do uso de MVs?**  
    Reduzem consumo de energia e necessidade de hardware físico, diminuindo impacto ambiental.

46. **O que é live migration em MVs?**  
    É a capacidade de mover uma MV em execução de um servidor físico para outro sem interrupção significativa.

47. **Como a virtualização impacta no gerenciamento de data centers?**  
    Facilita a consolidação de servidores, melhora a escalabilidade e reduz custos operacionais.

48. **Quais mecanismos de segurança podem ser aplicados em MVs?**  
    Firewalls virtuais, criptografia de discos virtuais e isolamento de rede.

49. **Por que snapshots são importantes em ambientes de teste?**  
    Porque permitem restaurar rapidamente um estado conhecido após falhas.

50. **Explique o papel das MVs na estratégia de continuidade de negócios.**
    Garantem recuperação rápida em caso de falhas, replicando ambientes em diferentes servidores ou data centers.

---


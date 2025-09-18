---

# 📘 50 Questões Discursivas

## Tema: Estrutura de Armazenamento de Massa – Estrutura RAID

---

## 🔹 1. Introdução e Conceitos Fundamentais

1. **O que é armazenamento de massa e qual sua função nos sistemas computacionais?**  
   → É o conjunto de dispositivos responsáveis por armazenar permanentemente dados e programas, garantindo persistência e acessibilidade mesmo após desligar o computador.

2. **Qual a diferença entre memória principal e armazenamento de massa?**  
   → A memória principal (RAM) é volátil e rápida, utilizada para execução temporária, enquanto o armazenamento de massa é permanente, mais lento, mas essencial para persistência.

3. **Por que discos de armazenamento são considerados gargalos no desempenho do sistema?**  
   → Porque possuem tempo de acesso mecânico (seek e latência rotacional), sendo muito mais lentos que processadores e memórias principais.

4. **O que caracteriza um SSD em comparação a discos magnéticos tradicionais?**  
   → O SSD não possui partes móveis, oferece menor latência e maior taxa de transferência, embora custe mais caro por GB.

5. **Qual o papel do sistema operacional na gerência de armazenamento?**  
   → Controlar, organizar e otimizar o acesso aos dispositivos, fornecendo abstrações como arquivos e diretórios.

---

## 🔹 2. Estrutura RAID – Definições Gerais

6. **O que significa RAID e qual o seu objetivo?**  
   → RAID significa *Redundant Array of Independent/Inexpensive Disks* e tem como objetivo melhorar desempenho e/ou confiabilidade combinando múltiplos discos em uma unidade lógica.

7. **Qual a principal diferença entre RAID por hardware e RAID por software?**  
   → O RAID por hardware utiliza controladores dedicados, oferecendo melhor desempenho; o RAID por software é gerenciado pelo sistema operacional, consumindo mais recursos da CPU.

8. **Quais são os três critérios principais para avaliar níveis de RAID?**  
   → Desempenho (velocidade), custo (quantidade de discos) e tolerância a falhas (confiabilidade).

9. **RAID substitui a necessidade de backups? Explique.**
   → Não, pois RAID protege apenas contra falhas de hardware; não evita perda de dados por exclusão acidental, corrupção lógica ou ataques.

10. **Por que o RAID é considerado uma solução de tolerância a falhas?**  
    → Porque nos níveis com redundância (espelhamento ou paridade) os dados podem ser recuperados mesmo com falha de disco.

---

## 🔹 3. RAID 0 – Striping

11. **Explique o funcionamento do RAID 0.**  
    → Ele divide os dados em blocos e distribui entre os discos (striping), aumentando o desempenho, mas sem redundância.

12. **Qual a vantagem principal do RAID 0?**  
    → Alto desempenho em leitura e escrita.

13. **Qual a desvantagem principal do RAID 0?**  
    → Não há tolerância a falhas; a perda de um disco causa perda total dos dados.

14. **Qual cenário mais adequado para RAID 0?**  
    → Sistemas que priorizam velocidade, como edição de vídeo ou jogos.

15. **Por que RAID 0 não é indicado para servidores críticos?**  
    → Porque a ausência de redundância implica risco alto de perda total de dados.

---

## 🔹 4. RAID 1 – Espelhamento

16. **Explique o funcionamento do RAID 1.**  
    → Cada dado é gravado em dois discos simultaneamente, garantindo redundância total.

17. **Qual a principal vantagem do RAID 1?**  
    → Alta confiabilidade, pois os dados estão duplicados.

18. **Qual a principal desvantagem do RAID 1?**  
    → Custo elevado, já que utiliza o dobro de espaço físico.

19. **O desempenho de leitura em RAID 1 pode ser melhor?**  
    → Sim, pois a leitura pode ser distribuída entre os discos espelhados.

20. **Cite um exemplo de aplicação prática para RAID 1.**
    → Servidores de banco de dados que exigem disponibilidade constante.

---

## 🔹 5. RAID 2, 3 e 4

21. **O que caracteriza o RAID 2?**  
    → Striping em nível de bits e uso de códigos de correção de erros (ECC).

22. **Por que o RAID 2 é pouco utilizado?**  
    → Exige muitos discos extras para correção de erros, tornando-o caro e ineficiente.

23. **Explique o funcionamento do RAID 3.**
    → Striping em nível de bytes com um disco dedicado à paridade.

24. **Qual o gargalo do RAID 3?**  
    → O disco de paridade único, que pode sobrecarregar-se.

25. **Como o RAID 4 difere do RAID 3?**  
    → RAID 4 faz striping em nível de blocos, mas ainda usa um disco dedicado para paridade.

---

## 🔹 6. RAID 5

26. **Explique o funcionamento do RAID 5.**  
    → Faz striping em blocos e distribui a paridade entre todos os discos, evitando gargalo central.

27. **Qual a principal vantagem do RAID 5?**  
    → Bom equilíbrio entre desempenho, custo e tolerância a falhas.

28. **Qual a desvantagem do RAID 5?**  
    → Escritas são mais lentas devido ao cálculo e atualização da paridade.

29. **Quantos discos no mínimo são necessários no RAID 5?**  
    → Pelo menos três discos.

30. **Cite um exemplo prático de uso do RAID 5.**
    → Servidores de arquivos corporativos que precisam de alta disponibilidade.

---

## 🔹 7. RAID 6

31. **Como funciona o RAID 6?**  
    → Distribui dados e dupla paridade entre os discos, permitindo falha de até dois discos.

32. **Qual a principal vantagem do RAID 6?**  
    → Alta confiabilidade com tolerância à falha de dois discos simultaneamente.

33. **Qual a principal desvantagem do RAID 6?**  
    → Escritas mais lentas devido ao cálculo de dupla paridade.

34. **Quantos discos no mínimo são necessários no RAID 6?**  
    → No mínimo quatro discos.

35. **Qual cenário ideal para RAID 6?**  
    → Data centers que demandam alta disponibilidade e segurança dos dados.

---

## 🔹 8. RAID 10 (1+0)

36. **Explique o funcionamento do RAID 10.**  
    → Combina espelhamento (RAID 1) e striping (RAID 0), unindo redundância e desempenho.

37. **Qual a vantagem principal do RAID 10?**  
    → Alta confiabilidade e alto desempenho.

38. **Qual a desvantagem principal do RAID 10?**  
    → Alto custo, pois exige no mínimo quatro discos.

39. **Qual cenário ideal para RAID 10?**  
    → Bancos de dados críticos que exigem rapidez e segurança.

40. **RAID 10 é mais indicado que RAID 5 para desempenho? Explique.**  
    → Sim, pois oferece escrita/leitura mais rápidas sem os cálculos de paridade do RAID 5.

---

## 🔹 9. Comparações e Análises Críticas

41. **Qual a principal diferença entre striping e espelhamento?**  
    → Striping divide dados entre discos para desempenho; espelhamento duplica dados para confiabilidade.

42. **Qual RAID oferece maior desempenho puro?**  
    → RAID 0, mas sem redundância.

43. **Qual RAID oferece maior segurança de dados?**  
    → RAID 6 e RAID 10, com maior redundância.

44. **Em que situação RAID 1 é mais adequado que RAID 5?**  
    → Em sistemas com poucos discos, onde confiabilidade é mais importante que capacidade.

45. **Por que RAID 5 é considerado um bom equilíbrio?**  
    → Porque combina tolerância a falhas com eficiência no uso de espaço.

46. **Qual RAID é mais indicado para aplicações domésticas de baixo custo?**  
    → RAID 1, pela simplicidade e confiabilidade.

47. **Qual RAID é mais indicado para data centers críticos?**  
    → RAID 6, pela tolerância a falhas múltiplas.

48. **Qual RAID é mais indicado para bancos de dados de alta performance?**  
    → RAID 10, pela combinação de velocidade e segurança.

49. **Qual a principal limitação de custo nos níveis de RAID com espelhamento?**  
    → O dobro de discos é necessário, elevando o custo total.

50. **Qual o dilema central na escolha de um nível de RAID?**  
    → Equilibrar custo, desempenho e tolerância a falhas de acordo com a aplicação.

---



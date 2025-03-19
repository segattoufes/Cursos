# Eletromagnetismo - Tentativa alternativa {#custom-id}
>[!hint] **Descrição:**
> Notas para a nova versão da disciplina Eletromagnetismo II, à partir de 2025/1.


>[!tldr] Pré Requisitos
>1. Álgebra Linear (autovalores e autovetores)
>2. Equações diferenciais parciais e ordinárias (Cálculo III)
>3. Circuitos Elétricos
>4. Uma sistema de programação, em particular Python ou/e Matlab

>[!tldr] Onde iremos usar?
>1. Ondas
>2. Linhas de Transmissão, incluindo *microstrips*
>3. Guias de Ondas
>	1. Metálicos (Retangular e Circular)
>	2. Dielétricos (Fibras ópticas e dispositivos integrados)
>4. Antenas
>5. Propagação no espaço livre
>	1. *Indoor*
>	2. *Outdoor*


>[!tldr] Quais aplicações?
>1. Transmissão de energia
>2. Sistemas sem fios (IoT, Wifi, 5G, 6G)
>3. Dispositivos integrados para IA
>4. Comunicações Ópticas
>5. ....


>[!tldr] Quais *softwares* iremos usar?
>1. Python, via Anaconda
>2. Matlab
>3. Ansys Lumerical
>4. Ansys HFSS
>5. Photon Design

>[!abstract] Ementa
>Ondas eletromagnéticas, propagação, reflexão e refração de ondas planas, linhas de
transmissão, guias de onda e fibras ópticas, introdução a antenas e propagação, métodos
numéricos em eletromagnetismo. Poluição eletromagnética e seus efeitos.


>[!goal] Objetivos
>Entender a base teórica por trás de campos eletromagnéticos variantes no tempo, os conceitos fundamentais de circuitos magnéticos e transformadores, os conceitos de ondas eletromagnéticas no espaço livre, os conceitos de linhas de transmissão como modos de propagação TEM, a Carta de Smith, transitórios em linhas, os conceitos de modos de
propagação, velocidade de fase, velocidade de grupo e frequência de corte.

>[!danger] Referências
>[1] Sadiku, Matthew N. O., **"Elementos de Eletromagnetismo"**, Ed. Bookman.
>[2] Wentwoth, S. M. **"Eletromagnetismos Aplicado: Abordagem Antecipada das Linhas de Transmissão",** E. Bookman.
>[3] Jennifer E. Houle, Dennis M. Sullivan, **"Electromagnetic Simulation Using the FDTD Method with Python"**, John Wiley & Sons, 15 de jan. de 2020 - 224 páginas

>[!Attention] [[Trilhas]] (Sugestões)
>1. Óptica no espaço livre
>2. Fotônica integrada





>[!attention] Sugestão de Laboratórios
>**Software**
>1. Introdução à Phyton - Comandos básicos, bibliotecas  e gráficos (3 ou 4 aulas)
>2. Métodos numéricos - FDTD 1D e 2D em Python [3] (3 aulas)
>3. Ansys HFSS (2 aulas)
>  **Hardware**
>  1. Resposta  de circuitos simples:
> 	 1. Circuito RC, carga e descarga versus frequência da onda quadrada (1/2 aula)
> 	 2. Varredura em frequência (manual) (1/2 aula)
> 	 3. Varredura usando a função *Sweep* do gerador e FFT do osciloscópio (1 aula)
> 	 4. Resposta ao impulso (pulso curto) (1 aula)
> 1. Medidas de espectro de frequência - Analisador de espectro (2 aulas)
> 2. Resposta em frequência de dispositivos em altas frequências (uso do VNA) (3 aulas)
> 3. Caracterização de antenas (1 ou 2 aulas)
> 4. Experimentos em Óptica no espaço livre (depende dos equipamentos novos)
> 




A relação entre o índice de refração ($n$), a permissividade elétrica ($\epsilon$) e a permeabilidade magnética  ($\mu$) em um meio dielétrico é dada pela seguinte expressão:

$n = \sqrt{\epsilon_{r}\mu_{r}}$

Onde:

- $n$ é o índice de refração do meio,
    
- $\epsilon_{r}$​ é a permissividade elétrica relativa do meio (em relação ao vácuo),
    
- $\mu_{r}$​ é a permeabilidade magnética relativa do meio (em relação ao vácuo).
    

### Explicação:

1. **Permissividade Elétrica $(\epsilon)$**: Mede a capacidade de um material de se polarizar em resposta a um campo elétrico. A permissividade elétrica relativa ($\epsilon_r$) é a razão entre a permissividade do material e a permissividade do vácuo ($\epsilon_0$​).
    
2. **Permeabilidade Magnética $(\mu)$**: Mede a capacidade de um material de se magnetizar em resposta a um campo magnético. A permeabilidade magnética relativa ($\mu_r$​) é a razão entre a permeabilidade do material e a permeabilidade do vácuo ($\mu_0$).
    
3. **Índice de Refração $(n)$**: Descreve como a luz (ou outra onda eletromagnética) se propaga em um meio. Está relacionado à velocidade da luz no vácuo ($c$) e à velocidade da luz no meio ($v$) pela expressão $v = \frac{c}{n}$​.
    

### Relação:

Em muitos materiais dielétricos, especialmente os não magnéticos, a permeabilidade magnética relativa ($\mu_r$) é aproximadamente 1. Portanto, a relação simplifica-se para:

$n = \sqrt{\epsilon_r}$.

Isso significa que o índice de refração é principalmente determinado pela permissividade elétrica relativa do material.

### Considerações:

- Em materiais magnéticos, $\mu_r$​ pode ser significativamente diferente de 1, e a permeabilidade magnética também influencia o índice de refração.
    
- Em meios condutores ou com perdas, a relação pode se tornar mais complexa, envolvendo partes reais e imaginárias das permissividades e permeabilidades.
    

Essa relação é fundamental para entender a propagação de ondas eletromagnéticas em diferentes meios e é amplamente utilizada em óptica, engenharia de materiais e telecomunicações.


---
# Teste com IA
# Carga Elétrica  
A carga elétrica é uma propriedade fundamental da matéria, associada a partículas subatômicas como prótons (carga positiva) e elétrons (carga negativa). Ela é quantizada (medida em múltiplos da carga elementar,  $(\approx 1,6\times 10ˆ{-19} )$  [C] e obedece ao princípio de conservação: a carga total em um sistema isolado permanece constante. Cargas opostas se atraem, enquanto cargas iguais se repelem, conforme descrito pela *Lei de Coulomb*.

---

## História da Descoberta  
1. *Antiguidade: Os gregos antigos (como Tales de Mileto, ~600 a.C.) observaram que o âmbar (em grego, *élektron) atraía pequenos objetos quando atritado, um fenômeno estático.  
2. *Século XVI: William Gilbert estudou o "magnetismo" e cunhou o termo *eletricidade.  
3. *Século XVIII*:  
   - *Benjamin Franklin* propôs a existência de cargas positivas e negativas e relacionou raios à eletricidade (experimento com pipas, 1752).  
   - *Charles-Augustin de Coulomb* quantificou a força entre cargas (Lei de Coulomb, 1785).  
4. *Século XIX*:  
   - *Michael Faraday* explorou a indução eletromagnética e campos elétricos.  
   - *James Clerk Maxwell* unificou eletricidade e magnetismo em equações matemáticas (1860s).  
   - *J.J. Thomson* descobriu o elétron (1897), confirmando a natureza quantizada da carga.  
5. *Século XX*: A física quântica explicou a carga como propriedade intrínseca de partículas, com quarks carregando frações de \( e \).

---

## Importância no Mundo Atual  
1. *Energia e Tecnologia*:  
   - *Eletricidade*: Base da infraestrutura global (iluminação, motores, redes de energia).  
   - *Eletrônica*: Dispositivos como transistores e chips dependem do controle de cargas em semicondutores.  
   - *Comunicação*: Ondas eletromagnéticas (rádio, Wi-Fi, celulares) são geradas por cargas em movimento.  
2. *Medicina*: Equipamentos como tomógrafos e marcapassos utilizam princípios elétricos.  
3. *Transporte*: Veículos elétricos e sistemas ferroviários dependem de correntes controladas.  
4. *Energias Renováveis*: Painéis solares convertem luz em corrente elétrica via efeito fotoelétrico.  
5. *Ciência Fundamental*: Compreender a carga é essencial para áreas como física de partículas, nanotecnologia e estudos do universo (ex.: plasmas cósmicos).  

---

### Impacto Cultural e Ambiental  
A manipulação da carga elétrica revolucionou a sociedade, permitindo avanços como a internet, inteligência artificial e diagnósticos médicos precisos. Além disso, desafios como armazenamento em baterias e geração sustentável de energia são centrais nas discussões ambientais contemporâneas. Em suma, a carga elétrica é um pilar invisível, porém indispensável, da civilização moderna. ⚡
# Tamanho do Elétron e Força de Repulsão entre Dois Elétrons

---

## Tamanho do Elétron  
O *elétron* é considerado uma *partícula elementar* no Modelo Padrão da física de partículas. Isso significa que, até onde se sabe experimentalmente, *não possui estrutura interna ou tamanho definido* – é tratado como um *ponto sem dimensões físicas* ($\text{raio} < 10^{-18}$ metros).  


---

## Força de Repulsão entre Dois Elétrons  
A força de repulsão entre dois elétrons é calculada pela *Lei de Coulomb*:  
$F = k_e \cdot \frac{|q_1 \cdot q_2|}{r^2}$
Onde:  
- \(k_e = 8,988 \times 10^9 \, \text{N·m}^2/\text{C}^2\) (constante de Coulomb),  
- \(q_1 = q_2 = -e = -1,6 \times 10^{-19} \, \text{C}\) (carga do elétron),  
- \(r\) = distância entre os elétrons.  

### Exemplo Prático:  
Se dois elétrons estão separados por *1 metro*:  
\[
F = 8,988 \times 10^9 \cdot \frac{(1,6 \times 10^{-19})^2}{1^2} \approx 2,3 \times 10^{-28} \, \text{N}
\]  
- *Observações*:  
  1. A força é *extremamente fraca* em escalas macroscópicas, mas *intensa em escalas atômicas* (ex.: \(r = 10^{-10}\) m \(\rightarrow F \approx 2,3 \times 10^{-8}\) N).  
  2. A repulsão é *eletrostática*, devido às cargas negativas idênticas.  

---

### Resumo:  
| Propriedade              | Valor/Descrição                        |     |
| ------------------------ | -------------------------------------- | --- |
| Tamanho do elétron       | Pontual $<10^{-18}~\text{m}$           |     |
| Força de repulsão (1 m)  | $\approx 2,3 \times 10^{-28}~\text{N}$ |     |
| Dependência da distância | $F \propto 1/r^2$                      |     |

---

*Nota*: A força entre partículas subatômicas é relevante em contextos como física de materiais, química quântica e engenharia de semicondutores. ⚛







---
| Syntax| Text|
|:------:|----:|
|qqqq | ssss |


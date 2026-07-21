# Curso: Bootcamp Bradesco - GenAI, Dados & Cyber
## Treinando uma IA de Aprendizagem
**Descrição:** Criação de um miniguia NotebookLM utilizando fontes especificas referentes a impressão 3D

[Link de acesso ao NotebooLM](https://bambulab.com/pt-br){:target="_blank"}

# 🧠 Caderno Temático: Domínio em Impressão 3D, Fatiamento e Engenharia de Materiais
### 🔬 1. Contexto e Objetivos
### 📝 Escopo do Caderno Temático
* **Tema Central:** Ecossistema de Impressão 3D (Hardware, Materiais e Fatiadores de Alta Performance).

* **Problema/Cenário:** O mercado de impressão 3D voltado para a criação de peças decorativas e de marketing exige um controle fino sobre os equipamentos e parâmetros de software. A vasta gama de impressoras, filamentos e configurações em softwares fatiadores torna necessário consolidar essas informações para extrair o máximo de qualidade, otimizando o acabamento visual (premium) e o tempo de impressão.

🎯 Objetivos de Estudo
1. **Objetivo Primário:** Mapear e dominar as configurações dos principais hardwares (Anycubic, Bambu Lab, Prusa) e as possibilidades dos fatiadores (AnycubicSlicerNext, Orca, PrusaSlicer, Bambu Studio).

2. **Objetivo Secundário:** Compreender a fundo o comportamento, as qualidades e as diferenças dos tipos de materiais (especialmente configurações precisas para PLA de 1.75mm e variações com efeitos).

3. **Métrica de Sucesso:** Ser capaz de configurar um perfil de fatiamento perfeito e definir o setup ideal para a escala de produção de peças decorativas comerciais com alto apelo visual.

---

## 📚 2. Curadoria de Fontes (Sources)

As fontes abaixo foram injetadas no NotebookLM para criar uma base de dados que combina documentação técnica oficial, softwares de fatiamento e conhecimento prático (know-how de mercado) de criadores de conteúdo especialistas na área:

| #	| Tipo de Fonte	| Canal / Organização	| Foco da Informação | Link de Acesso
|:-:| :--- | :--- | :--- | :--- |
| **1** | Audiovisual / Prática | **3DGeekShow** | Testes de máquinas, dicas de calibração e resolução de problemas. | [YouTube](http://www.youtube.com/@3DGeekShow) |
| **2** | Audiovisual / Prática | **r3lab_xyz** | Técnicas de acabamento, pintura e configurações de impressão FDM. | [YouTube](http://www.youtube.com/@r3lab_xyz) |
| **3** | Audiovisual / Prática | **Hugo Lopes 3D** | Otimização de produção, materiais e tutoriais de fatiadores. | [YouTube](http://www.youtube.com/@hugolopes3d_) |
| **4** | Docs / Hardware | **Anycubic** | Especificações, manuais e ecossistema das impressoras Anycubic. | [Site Oficial](https://www.anycubicofficial.com.br/) |
| **5** | Docs / Hardware | **Bambu Lab** | Tecnologias CoreXY de alta velocidade e impressão multicolorida. | [Site Oficial](https://bambulab.com/pt-br) |
| **6** | Docs / Hardware | **Prusa 3D** | Manuais de calibração, manutenção e ecossistema open-source. | [Site Oficial](https://www.prusa3d.com/) |
| **7** | Software / Slicer | **Orca Slicer** | Documentação e recursos do fatiador com foco em calibrações avançadas. | [Site Oficial](https://www.orcaslicer.com/) |
| **8** | Software / Slicer | **AnycubicSlicerNext**| Recursos nativos e perfis atualizados para a linha de máquinas da Anycubic. | [Download/Docs](https://www.anycubic.com/slicerNextDownload) |
| **9** | Software / Slicer | **PrusaSlicer** | Documentação rica em configurações de camadas, suportes e modificadores. | [Site Oficial](https://prusaslicer.net/) |
| **10**| Software / Slicer | **Bambu Studio** | Funcionalidades de sincronização na nuvem, pintura de modelos e gestão de filamentos. | [Site Oficial](https://bambuslicer.com/) |

---

## 🛠️ 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

### 📜 Prompts Iniciais (Cold Start)
* **Prompt de Exploração de Materiais:** > *"Com base nas fontes técnicas, crie um quadro comparativo focado em materiais de impressão 3D (PLA vs. PETG vs. ABS), detalhando temperatura ideal, taxa de retração e nível de brilho para acabamento estético."*
* **Prompt de Configuração de Slicer:**
  > *"Analise as documentações do Orca Slicer e do AnycubicSlicerNext. Liste o passo a passo para configurar modificadores de parede e costura (seam) visando esconder marcas na impressão final."*


### 🩸 As "Cicatrizes" (Erros, Limitações e Soluções)
1.  **Desafio 1: Viés para peças de alta resistência mecânica.**
    * *Sintoma:* Ao perguntar sobre otimização de fatiamento, a IA começou a sugerir densidades de preenchimento altas (infill) e uso de materiais estruturais adequados para robótica ou peças mecânicas, o que aumenta tempo e custo à toa.
    * *Cicatriz / Solução:* Foi necessário aplicar um prompt de direcionamento estrito: *"Ignore qualquer instrução voltada para desenvolvimento de peças para robótica ou ferramentas mecânicas. O foco absoluto deste caderno são peças decorativas e de marketing para venda. Priorize economia de material e excelência no acabamento externo, usando PLA 1.75mm."*
2.  **Desafio 2: Configurações de texturização premium superficiais.**
    * *Sintoma:* A resposta da IA sobre dar um visual mais requintado às peças foi genérica, citando apenas lixamento manual.
    * *Cicatriz / Solução:* O prompt precisou de especificidade técnica focada em software. Solução: *"Cruze as informações dos fatiadores (especialmente AnycubicSlicerNext e Orca) com as dicas dos canais do YouTube. Extraia os parâmetros exatos para utilizar a função 'Fuzzy Skin' (Pele de Pêssego). O objetivo é dar um acabamento texturizado e premium diretamente na mesa de impressão, sem pós-processamento."*

---

## 📖 4. Miniguia de Estudo (Entrega Final)

### 📌 Resumos Estruturados
* **Módulo 1: O Ecossistema de Hardwares:** Comparativo arquitetônico entre o sistema tradicional cartesiano robusto (Anycubic Kobra/Prusa) e as arquiteturas CoreXY de altíssima velocidade (Bambu Lab). Análise sobre sistemas combo de multicore e impacto na eficiência de produção.
* **Módulo 2: Maestria em Fatiadores:** Como transitar entre AnycubicSlicerNext, Orca Slicer e PrusaSlicer. Mapeamento das funcionalidades cruciais: controle dinâmico de velocidade, calibração de fluxo (Flow Rate), configuração inteligente de suportes orgânicos e costuras escondidas.
* **Módulo 3: Ciência dos Materiais para Decoração:** Comportamento térmico do PLA e suas variações. Como evitar 'stringing' (fios) e 'warping' (empenamento) para garantir peças estéticas sem defeitos em superfícies lisas e anguladas.

  
### 📕 Glossário de Conceitos Aprendidos
* **Slicer (Fatiador):** Software responsável por traduzir o modelo 3D (STL/OBJ) em coordenadas (G-code) que a impressora entende.
* **Fuzzy Skin (Pele de Pêssego):** Algoritmo presente nos fatiadores que causa uma microvibração no perímetro externo da impressão, gerando uma textura rugosa que esconde marcas de camada e entrega um acabamento premium.
* **Costura (Z-Seam):** A marca visual deixada na peça no exato ponto onde o bico inicia e termina a impressão de uma camada perimetral. Pode ser aleatória, alinhada ou escondida em cantos agudos via slicer.
* **CoreXY:** Cinemática avançada de impressoras (comum nas Bambu Labs) onde a mesa se move no eixo Z, e os motores X e Y ficam parados trabalhando em conjunto por correias, permitindo extrema velocidade sem perda de qualidade.

♻️ Biblioteca de Prompts Reutilizáveis (Para Próximas Revisões)
Para Otimização de Tempo de Impressão:

### ♻️ Biblioteca de Prompts Reutilizáveis (Para Próximas Revisões)

* **Para Otimização de Tempo de Impressão:**
    ```text
    "Atuando como um gestor de granja de impressão 3D, analise as opções de fatiamento das fontes e liste 5 configurações de software que reduzem o tempo de impressão de uma peça decorativa em pelo menos 20%, sem impactar a qualidade da parede externa (outer wall)."
    ```
* **Para Resolução de Defeitos (Troubleshooting de Máquina):**
    ```text
    "Estou tendo problemas com bolhas e 'teias de aranha' (stringing) ao imprimir PLA 1.75mm. Utilizando as referências dos canais do YouTube (3DGeekShow, etc), qual é o roteiro de testes em temperatura e retração (retraction) que devo seguir no fatiador?"
    ```
* **Para Inovação de Portfólio (Produtos):**
    ```text
    "Com base nas capacidades das impressoras e nos efeitos de preenchimento (infill patterns) sem parede superior (top layer) descritos nos softwares Prusa/Orca, me dê 3 ideias de texturas vazadas que eu possa usar para criar porta-copos ou brindes de marketing únicos."
    ```

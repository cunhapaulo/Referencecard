# MARKDOWN, MARP & LaTeX (Reference Card)
### Última atualização: 13.mai.2022
Reference card of resourceful informations about LaTeX, Markdown and Marp.

<br><br>

> # MARP

## Listas fragmentadas sem marcadores (bullets)
```markdown
<div data-marpit-fragment>

![h:400](https://www.freebsdnews.com/wp-content/uploads/bsdbike-768x890.jpg)

</div>
```

## Colunas
```markdown
---
<!-- 
---- [ ] ----------------------- [ SLIDE ] ------------------------- [ ] ----
-->

# 

<div class="columns">
<div>


</div>
<div>



</div>
</div>


```





<br><br><br><br><br><br>

> # MARKDOWN
<br>

> ## COMENTÁRIOS
- Comentários para o código:
  ```markdown
  <!-- 
  #~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#
                                [ SECTION ]
  #~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#~#
  -->

  <!-- -:-:-:-:-:-:-:-:-:-:-:-: [ SLIDE ] :-:-:-:-:-:-:-:-:-:-:-:-:- -->
  ```

.
> ## COLUNAS
> **Referência**: [Documentação do PANDOC - Columns](https://pandoc.org/MANUAL.html#columns)
- **SIMPLES**:
  ```markdown

  ## Simple

  ::: columns
  :::: column
    
  ::::
  :::: column
    
  ::::
  :::
  ```

- **SIMPLES and aligned to the center**:
  ```markdown

  ## Simple

  :::::::::::::: {.columns align=center}
  :::: column
  
  \center \Large 

  ::::
  :::: column
  
  ::::
  ::::::::::::::

- **LARGURA DA COLUNA VARIÁVEL**:  

  ```markdown
  ## Largura variável
  ## {.column width="30%"}

  ::: columns
  :::: {.column width="30%"}
    ![](img/.jpg){height="75%" width="75%"}
  ::::
  :::: {.column width="70%"}

  ::::
  :::
  ```

- **ALINHAMENTO VERTICAL**
  ```markdown
  ## Vertical alignment
  ## {.columns align=center}

  :::::::::::::: {.columns align=center}
  :::: {.column width=30%}
    ![](img/.jpg){height="75%" width="75%"}
  ::::
  :::: {.column  width="70%"}

  ::::
  :::::::::::::: 
  ```
- **TAMANHO FIXO DE COLUNA**

  ```markdown
  ## Fixed column width
  ## {.columns align=center totalwidth=8em}

  :::::::::::::: {.columns align=center totalwidth=8em}
  ::: {.column width="40%"}
  contents...
  :::
  ::: {.column width="60%" align=bottom}
  contents...
  :::
  ::::::::::::::
  ```

.
> ## TABELAS
> **Referência**:[Documentação do PANDOC - TABLES](https://pandoc.org/MANUAL.html#tables)

- **TABELA SIMPLES**:
  ```markdown
  | Name          |    CEP     | Address      |         Salary |
  | :------------ | :--------: | :----------- | -------------: |
  | John Kennedy  | 66.050-520 | Washington   |     $ 1.200,00 |
  | Angela Merkel | 66.050-500 | Berlin, 370  |     $ 3.500,00 |
  | Lula da Silva | 98.000-666 | São Bernardo | $ 1.900.000,00 |
  Table: Legenda da tabela.
  ```

  **Resultado**:

  | Name          |    CEP     | Address      |         Salary |
  | :------------ | :--------: | :----------- | -------------: |
  | John Kennedy  | 66.050-520 | Washington   |     $ 1.200,00 |
  | Angela Merkel | 66.050-500 | Berlin, 370  |     $ 3.500,00 |
  | Lula da Silva | 98.000-666 | São Bernardo | $ 1.900.000,00 |
  Table: Legenda da tabela.

.
- **MODELO 2**
```markdown
-------------------------------------------------------------
 Centered   Default       **Right** Left
  Header    Aligned     **Aligned** Aligned
----------- ------- --------------- -------------------------
   First    row                12.0 Example of a row that
                                    spans multiple lines.

  Second    row                 5.0 Here's another one. Note
                                    the blank line between
                                    rows.

   Third    row                 4.0 Material to think about:

                                    - Item 2

                                    - Item 3              
-------------------------------------------------------------
Table: Here's a multiline table without headers.

```

.   
- **MODELO 3**
```markdown
+---------------+---------------+--------------------+
| Fruit         | Price         | Advantages         |
+===============+===============+====================+
| Bananas       | $1.34         | a. built-in wrapper|
|               |               | b. bright color    |
+---------------+---------------+--------------------+
| Oranges       | $2.10         | a. cures scurvy    |
|               |               |       - Brazil     |
|               |               | b. origin:         |
+---------------+---------------+--------------------+
Table: Sample grid table.  
``` 
.
- **MODELO 4**
```latex
\begin{table}[ht]
\caption{Performance After Post Filtering} % title name of the table 
\centering  % centering table

\begin{tabular}{l c c rrrrrrr}    % creating 10 columns
    \hline\hline    % inserting double-line
    Audio                    & Audibility          & Decision & \multicolumn{7}{c}{Sum of Extracted Bits}
    \\ [0.5ex] \hline    % inserts single-line

    % Entering 1st row 
    & & soft & 1 & $-1$ & 1 & 1 & $-1$ & $-1$ & 1 \\[-1ex]
    \raisebox{1.5ex}{Police} & \raisebox{1.5ex}{5} & hard & 2 & $-4$ & 4 & 4 & $-2$ & $-4$ & 4 \\[1ex]

    % Entering 2nd row 
    & & soft & 1 & $-1$ & 1 & 1 & $-1$ & $-1$ & 1 \\[-1ex] \raisebox{1.5ex}{Beethoven} & \raisebox{1.5ex}{5}& hard &8 & $-8$ & 2 & 8 & $-8$ & $-8$ & 6 \\[1ex]

    % Entering 3rd row 
    & & soft & 1 & $-1$ & 1 & 1 & $-1$ & $-1$ & 1 \\[-1ex] \raisebox{1.5ex}{Metallica} & \raisebox{1.5ex}{5}& hard &4 & $-8$ & 8 & 4 & $-8$ & $-8$ & 8 \\[1ex]

    % [1ex] adds vertical space 
    \hline % inserts single-line
\end{tabular}
\label{tab:PPer}
\end{table}

```

.
> ## VARIÁVEIS PARA O BEAMER
> **Referência**: [Documentação do PANDOC - Variables for Beamer slides](https://pandoc.org/MANUAL.html#variables-for-beamer-slides)
> 
.
> ## MODIFICADORES DE APRESENTAÇÃO  
> **Referência**: [Documentação PANDOC - Frame Attributes](https://pandoc.org/MANUAL.html#frame-attributes-in-beamer)

.
- **INCREMENTAL**
  **Referência**: [Documentação do PANDOC - Incremental lists](https://pandoc.org/MANUAL.html#incremental-lists)

  ```markdown
  ## ::: incremental

  ::: incremental
  - Eat spaghetti
  - Drink wine
  :::
  ```

- **SIMPLES**
  ```markdown
  ## {.plain}
  
  .# Agradecimentos {.plain}
  ```

- **RESSALTAR**
  ```markdown
  ## {.standout}

  .# Agradecimentos {.standout}
  ```

- Marcar item para que **NÃO SEJAM NUMERADOS**:
  ```markdown
  ## {.unnumbered}

  .# Referências Bibliográficas {.unnumbered}
  ```
- Marcar o texto para **FRACIONAR** em vários slides.
  ```markdown
  ## {.allowframebreaks}

  .# Conceitos {.allowframebreaks}
  ```
- Marcadores de **MODIFICAÇÃO**:
  ```latex
  {.width="10%"}
  {.height=10%}
  {align=center}
  ```

.  
> ## FUNCIONALIDADES

- **LINKS**:

    ```markdown
        [Texto de referência](URL)
        Ex.: [Link para o site do Pandoc](https://www.pandoc.org)
    ```
    Resultado:
    - [Link para o site do Pandoc](https://www.pandoc.org)
.
- **IMAGENS**:

  ```markdown
    ![Texto de referência.](URL){dimensões}
    ![Este é o exemplo de hipercubo.](img/cube.png){width=10%}
  ```
  Resultado:
  ![Este é o exemplo de hipercubo.](img/cube.png)

  .

- **REFERÊNCIA BIBLIOGRÁFICA**:
  > **Referência**: [Documentação do PANDOC - Conference Papers, Published vs. Unpublished](https://pandoc.org/MANUAL.html#conference-papers-published-vs.-unpublished)
  ```markdown
    [@Kant2002, p. 22]

    @Kant2002 [p. 22]
  ```
  Resultado:
  [@Kant2002, p22]

  .
- **PLACEMENT OF THE BIBLIOGRAPHY**
If the style calls for a list of works cited, it will be placed in a div with id refs, if one exists:

  ```markdown
  ::: {#refs}

  :::
  ```
  .
- NOTA DE **RODAPÉ**:

  ```markdown
    Na Crítica da Razão Pura[^crp], escrita por Kant [...]

    [^crp]: Primeiro livro da fase crítica de Kant.
  ```

  .
- **DEFINIÇÕES** DE TERMOS:

  ```markdown
    Term 1:
    : Definition 1 text wich can span more
    than one line to complete.

    Term 2:
    : Definition 2 text wich can span more
    than one line to complete.
  ```

.
- **EQUAÇÕES** MATEMÁTICAS (SINTAXE DO LATEX):

  ```latex
  $f(x) = 2sin(x)+2cos(x)$
  $$ s_{N}(x) = \sum_{n=-N}^{N} c_{n} e^{i\frac{2\pi n x}{P}} $$
  
  ```
  Resultado:
  - Equação inserido na mesma linhas$f(x) = 2sin(x)+2cos(x)$ do texto.

  - Neste exemplo, a equação está centralizada:
    $$ s*{N}(x) = \sum*{n=-N}^{N} c\_{n} e^{i\frac{2\pi n x}{P}} $$
    $$\nabla \times \mathbf{E} =-\frac{\partial \mathbf{B}}{\partial t} \ \mathrm{and} \ \nabla \times \mathbf{H} =\mathbf{J} +\frac{\partial \mathbf{D}}{\partial t}$$
  
.
- COMANDO DE **TECLADO**: <kbd> ctrl+c </kbd>
  ```markdown
  <kbd> ctrl+c </kbd>
  ```

.
- CAIXA DE MARCAR (sybol):
```markdown
- [ ] text 1
- [x] text 2
- [ ] text 3
```
Resultado:
  - [ ] text 1
  - [x] text 2
  - [ ] text 3

.
> ## ARGUMENTOS NO CABEÇALHO YAML

- `aspectratio=169:` muda a razão de proporção.
- `header-includes: |` usado para inserir pacotes.

.
> ## CÓDIGO LATEX NO TEXTO MARKDOWN:

1. Inserir no cabeçalho YAML a sessão para incluir no cabeçalho **header-includes**:

    ``` latex
    ---
    # YAML Header
    #
    header-includes: |
        \usepackage{tikz,pgfplots}
    ---
    ```
2. Inserir o **código LaTeX** no texto **Markdown**:

   ```latex
   \begin{center}
       \begin{tikzpicture}[->,>=stealth',shorten >=1pt,auto,node distance=3.5cm,
       thick,main node/.style={circle,fill=blue!20,draw,font=\sffamily\Large\bfseries}]

       \node[main node] (1) {1};
       \node[main node] (2) [below left of=1] {2};

       (8) edge node [left] {0.2} (7)
           edge [loop right] node {0.6} (8)
           edge [bend right] node[right] {0.2} (5);

   \end{tikzpicture}
   \end{center}
   ```

.
> ## FONTES IMPORTANTES PARA O LATEX

- **XeLaTeX command to use fonts**:
  ```latex
  \setmainfont[Ligatures=TeX]{Linux Libertine O}
  ```
- **Localização**: 
  - `C:\Program Files (x86)\TeXmacs\fonts\truetype`
  - `C:\Users\paulo.cunha.TJ.PA.GOV.BR\AppData\Local\Microsoft\Windows\Fonts`
  - `C:\Users\paulo.cunha.TJ.PA.GOV.BR\AppData\Roaming\MiKTeX\fonts\opentype`
  - `C:\Users\paulo.cunha.TJ.PA.GOV.BR\OneDrive\_LaTeX\_TYPEFACES\`
.
- **Antiqua**
.
- **Palatino**
.
- **Charter**
  ``` latex
  \usefonttheme{serif} % change font to allow \textbf{}
  \usepackage{charter} % Nicer fonts
  ```
.
- **Fira** 
  > Uso: (`Metropolis`)
  > - Fonte utilizada no estilo [METROPOLIS](https://github.com/matze/mtheme). Está disponível na forma de um um _package_ do LaTeX, sob o nome `Fira` em `\Fonts\Outline fonts`no MiKTeX.

.
- **Flama** 
  > Uso: (`HSRM`) 
  > - Fonte utilizada pelo estilo [HSRM`(Hochschule RheinMain)` ](https://github.com/benjamin-weiss/hsrmbeamertheme) para slides `Beamer`, criado por _Benjamin Weiss_.
  > - Download: [Font Geek](https://fontsgeek.com/flama-font?ref=readme).

.
- **Biolinum** e **Libertine** 
  > Uso: (`ACM`)
  > - Fonte utilizada nos modelos de artigos da `ACM`.
  > - Download: [Font Squirrel - Biolinum](https://www.fontsquirrel.com/fonts/linux-biolinum)  e [DaFont - Libertine](https://www.dafont.com/pt/linux-libertine.font?text=Haskell+is+a+Functional+Programming+Language)
  > - [Site da ACM](https://www.acm.org/publications/taps/accepted-latex-packages)

.
- **Linux Libertine O**
  ``` latex
  \setmainfont[Ligatures=TeX]{Linux Libertine O}
  ```
.
> ## ESTILOS E THEMAS IMPORTANTES
- **EISVOGEL**
    Template para documentos
    Site: https://github.com/Wandmalfarbe/pandoc-latex-template
- **Metropolis** 
    Site: [https://github.com/matze/mtheme](https://github.com/matze/mtheme)
- **HSRM** 
Site da universidade: [https://www.hs-rm.de](https://www.hs-rm.de/de/hochschule/personen/hofmann-karl-heinrich/service-latex/beamer-latex)
    Site: [Hochschule RheinMain Beamer Thema](https://github.com/benjamin-weiss/hsrmbeamertheme)

.
> ## CONTRIBUIÇÕES INTERESSANTES

- Impressão na forma de _handout_
  ``` latex
    $if(handout)$
    \usepackage{pgfpages}
    %\pgfpagesuselayout{2 on 1}[a4paper,border shrink=3mm]
    \pgfpagesuselayout{4 on 1}[a4paper,border shrink=4mm,landscape]
    $endif$
  ```
- Estilos de Fontes para o LaTeX
  > \usepackage[tt=false]{**antiqua**}
  > \usepackage[tt=false]{**palatino}**
  > \usepackage[tt=false]{**libertine**}

- Penn State University

    ```latex
    \definecolor{mpigreen}{HTML}{007977}
    \setbeamercolor{frametitle}{bg=mpigreen}
    ```

- Código **LaTeX** para diferenciar números menores que 10:
  ``` latex  
  \def\artnum#1{\ifnum#1<10 #1º\else #1\fi}

  \artnum{12}

  \newcommand{\arti}[2][]{(art.~\bold{\artnum{#2}}#1)}
  \newcommand{\artii}[3][]{(art.~\bold{\artnum{#2}},~\bold{#3}#1)}
  \newcommand{\artiii}[4][]{(art.~\bold{\artnum{#2}},~\bold{#3}~``\bold{#4}''#1)}
  ```

- Numeração diferente nos Anexos (Appendix) em LaTeX
  ```latex
  <!-- 
  ******************************** A P E N D I C E S ******************************** 
  \renewcommand{\thesection}{\arabic{section}}
  -->

  \appendix

  \newcounter{iSECTION}
  \newcounter{iSUBSECTION}
  \newcounter{iSUBSUBSECTION}

  \def \beginNewChapter{\beginNewSection}
  \def \beginNewSection{\setcounter{iSECTION}{0}}
  \def \beginNewSubsection{\setcounter{iSUBSECTION}{0}}
  \def \beginNewSubsubsection{\setcounter{iSUBSUBSECTION}{0}}


  \renewcommand{\thechapter}{\Alph{chapter}}

  \renewcommand{\section}[1]{
          \refstepcounter{iSECTION}
          \beginNewSubsection
          \vspace{.75cm}
          \textbf{\Large{\theiSECTION \hspace{.1cm} #1}}
          \vspace{.4cm}}

  \renewcommand{\subsection}[1]{
          \refstepcounter{iSUBSECTION}
          \beginNewSubsubsection
          \textbf{\theiSECTION.\theiSUBSECTION} \hspace{.1cm} #1}

  \renewcommand{\subsubsection}[1]{
          \refstepcounter{iSUBSUBSECTION}
          \begin{quote}
          \textbf{\theiSECTION.\theiSUBSECTION.\theiSUBSUBSECTION} \hspace{.1cm} #1
          \end{quote}
  }

  ```


- Resolving the problem with {.standout} slides corrupting the following ones **(Metropolis)**:
  ```markdown
  header-includes: 
      - \usepackage[portuges]{babel}
      # - \usepackage[tt=false]{antiqua}
      # - \usepackage[tt=false]{palatino}
      # - \usepackage[tt=false]{libertine}
      # - \usepackage{multicol}
      # - \usepackage{tabularx}
      # - \usepackage{array}
      # - \usepackage{longtable}
      - '\usetheme{metropolis}'
      - '\makeatletter'
      - '\beamer@ignorenonframefalse'
      - '\makeatother'
  
  ```

-  Usar fontes do modelo **ACM**
   ```latex
      \usepackage{tikz,pgfplots}
      \usepackage[T1]{fontenc} 
      \usepackage[tt=false]{libertine} 
      \setmonofont{inconsolata} 
      \usepackage[varqu]{zi4} 
      \usepackage[libertine]{newtxmath}
    ```
  
  - Modificações feitas por Paulo Cunha:
  
    ``` latex
    %---- begin(paulo.cunha)------------------------------------------------

    %---------------------------------------------------------------------
    % Colors
    %---------------------------------------------------------------------
    \definecolor{red}{rgb}{0.75,0.10,0.20}
    \definecolor{red2}{RGB}{150,0,0}
    \definecolor{blue}{rgb}{0.00,0.25,0.71}
    \definecolor{blue2}{RGB}{36, 25, 200}
    \definecolor{orange}{RGB}{255, 69, 0}
    \definecolor{orange2}{RGB}{255, 94, 14}
    \definecolor{black}{RGB}{100, 100, 100}

    \newcommand{\laranja}[1]{\textcolor{orange}{#1}}
    \newcommand{\azul}[1]{\textcolor{blue2}{#1}}
    \newcommand{\vermelho}[1]{\textcolor{red2}{#1}}
    \newcommand{\negro}[1]{\textcolor{black}{#1}}

    %---------------------------------------------------------------------
    % Markers \sout and \emph
    %---------------------------------------------------------------------
    %\setbeamerfont{negrito}{family=\Medium}
    %\renewcommand{\textbf}[1]{{\usebeamerfont{negrito}\negro{#1}}}
    \renewcommand{\textbf}[1]{{\Medium \negro{#1}}}
    \renewcommand{\emph}[1]{\laranja{#1}}

    \newcommand{\sout}[1]{\azul{#1}}
    \newcommand{\tightlist}{}

    \setbeamercolor{progress bar}{fg=orange,bg=orange2}

    $if(handout)$
    \usepackage{pgfpages}
    %\pgfpagesuselayout{2 on 1}[a4paper,border shrink=3mm]
    \pgfpagesuselayout{4 on 1}[a4paper,border shrink=4mm,landscape]
    $endif$

    %---- end(paulo.cunha)------------------------------------------------

    ```

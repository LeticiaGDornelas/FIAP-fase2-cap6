<img src="logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" border="0" width=30% height=30%>

# **LeiteControl**

---

#### Nomes dos integrantes do grupo
- Letícia Dornelas  


---

## Sumário

[1. Introdução](#c1)

[2. Visão Geral do Projeto](#c2)

[3. Desenvolvimento do Projeto](#c3)

[4. Resultados e Avaliações](#c4)

[5. Conclusões e Trabalhos Futuros](#c5)

[6. Referências](#c6)

[Anexos](#c7)

<br>

# <a name="c1"></a>1. Introdução

## 1.1. Escopo do Projeto

### 1.1.1. Contexto da Inteligência Artificial

A aplicação de **tecnologias de Inteligência Artificial e Análise de Dados no agronegócio** tem crescido de forma significativa, principalmente nas áreas de monitoramento, gestão de produtividade e otimização de recursos.  
A pecuária leiteira, um dos principais segmentos do setor agropecuário brasileiro, demanda soluções tecnológicas que permitam **melhor controle de produção, rastreabilidade e decisões baseadas em dados**.  

Dentro desse contexto, o uso de sistemas inteligentes e de automação contribui para aumentar a eficiência operacional, reduzir perdas e aprimorar o manejo dos animais, apoiando o produtor na modernização da gestão rural.

### 1.1.2. Descrição da Solução Desenvolvida

O projeto **LeiteControl** propõe uma solução tecnológica para o **monitoramento e controle da produção diária de leite** em fazendas de gado bovino leiteiro.  
O sistema foi desenvolvido em **Python** e integra conceitos fundamentais de **lógica de programação, estruturas de dados, manipulação de arquivos e conexão com banco de dados Oracle**.  

A aplicação permite **cadastrar vacas, registrar as ordenhas diárias, calcular médias de produção, detectar quedas de produtividade e gerar relatórios automáticos** em formatos `.txt` e `.json`.  
Os dados também são armazenados no **Oracle Database**, garantindo persistência, integridade e possibilidade de futuras análises em ferramentas como Power BI.

---

# <a name="c2"></a>2. Visão Geral do Projeto

## 2.1. Objetivos do Projeto

O **objetivo principal** do LeiteControl é **informatizar o controle de produção de leite** por vaca, oferecendo uma forma simples, prática e segura de registrar e acompanhar a produtividade diária de cada animal.  

Objetivos específicos:
- Permitir o **cadastro e acompanhamento individual de vacas**;  
- Registrar a **produção de leite diária** de cada animal;  
- Calcular automaticamente **médias e quedas de produção**;  
- Gerar **relatórios automáticos** e armazenar dados de forma persistente;  
- Integrar a aplicação ao **banco de dados Oracle**, garantindo consistência e segurança das informações.

## 2.2. Público-Alvo

O público-alvo do sistema são **pequenos e médios produtores rurais**, técnicos agrícolas e administradores de fazendas que desejam informatizar seus controles produtivos e tomar decisões baseadas em dados reais.  
O sistema também pode ser utilizado em **ambientes acadêmicos** para ensino e demonstração de conceitos de tecnologia aplicada ao agronegócio.

## 2.3. Metodologia

O desenvolvimento do projeto seguiu a **metodologia incremental**, baseada no ciclo **CRISP-DM (Cross Industry Standard Process for Data Mining)** adaptado ao contexto da programação.  
As etapas principais foram:
1. **Entendimento do problema** – análise das dificuldades de controle manual da produção;  
2. **Planejamento da solução** – definição das funcionalidades e modelagem de dados;  
3. **Desenvolvimento em Python** – implementação dos subalgoritmos, estruturas de dados e interface interativa com o usuário;  
4. **Armazenamento e integração com Oracle** – criação das tabelas `VACAS` e `ORDENHAS` e conexão via biblioteca `oracledb`;  
5. **Geração de relatórios e testes** – criação de arquivos `.json` e `.txt` e validação dos cálculos;  
6. **Documentação e versionamento** – produção do README e commit no GitHub.

---

# <a name="c3"></a>3. Desenvolvimento do Projeto

## 3.1. Tecnologias Utilizadas

- **Linguagem:** Python 3.11  
- **Bibliotecas:** `oracledb`, `json`, `datetime`, `typing`  
- **Banco de dados:** Oracle Database (modo Thin)  
- **Ambiente de execução:** Google Colab  
- **Formatos de saída:** `.json` (armazenamento) e `.txt` (relatório)  

## 3.2. Modelagem e Algoritmos

A estrutura do sistema foi baseada em **subalgoritmos** que representam funções e procedimentos para o controle do rebanho:
- `cadastrar_vaca()` – insere novas vacas no sistema;  
- `registrar_ordenha()` – registra a quantidade de leite por data;  
- `media_leite_vaca()` – calcula médias diárias de produção;  
- `detectar_quedas()` – identifica quedas significativas de produtividade (>20%).  

Os dados são armazenados em **listas e dicionários**, formando uma **tabela de memória** (`rebanho`), e exportados em JSON para persistência local.  
No banco **Oracle**, as tabelas `VACAS` e `ORDENHAS` garantem integridade e permitem consultas SQL para gerar médias e comparativos de desempenho.

## 3.3. Treinamento e Teste

O sistema foi testado em ambiente **Google Colab**, com simulações de registros reais de produção diária.  
Foram inseridas vacas com diferentes volumes de ordenha para validar o cálculo de médias e a detecção de quedas de produção.  
Os relatórios `.txt` gerados mostraram corretamente os valores de média e os alertas de redução de produtividade.

---

# <a name="c4"></a>4. Resultados e Avaliações

## 4.1. Análise dos Resultados

O sistema atendeu plenamente aos objetivos propostos.  
Os cálculos de média de produção diária e a detecção de quedas funcionaram conforme esperado, e os dados foram corretamente salvos em JSON e Oracle.  

Os relatórios gerados permitem rápida visualização do desempenho de cada vaca, e a integração com o banco de dados garante rastreabilidade e segurança das informações.  
A partir dos dados armazenados, é possível gerar análises comparativas e gráficos de produtividade em ferramentas externas.

## 4.2. Feedback dos Usuários

Durante os testes simulados, o sistema foi considerado:
- Intuitivo e fácil de usar;  
- Funcional para registrar e acompanhar produções diárias;  
- Eficiente na identificação de anomalias (quedas de produtividade).  

---

# <a name="c5"></a>5. Conclusões e Trabalhos Futuros

O projeto **LeiteControl** atingiu seus objetivos ao automatizar o controle da produção de leite e aplicar os principais conceitos estudados de Python e banco de dados.  
A solução demonstrou que a **integração entre tecnologia e agronegócio** pode gerar ganhos de produtividade e facilitar a gestão rural.

**Pontos fortes:**
- Uso completo dos conteúdos exigidos (subalgoritmos, estruturas, arquivos e Oracle);  
- Interface simples e interativa;  
- Armazenamento seguro e relatórios automáticos.

**Melhorias futuras:**
- Criar uma **interface gráfica (web ou desktop)** para tornar o sistema mais acessível;  
- Integrar **análises preditivas com IA**, estimando a produção futura;  
- Implementar **alertas automáticos por e-mail ou WhatsApp** para quedas de produção.

---

# <a name="c7"></a>Anexos

### A. Estrutura das Tabelas no Oracle

```sql
CREATE TABLE VACAS (
  ID NUMBER PRIMARY KEY,
  BRINCO VARCHAR2(20),
  RACA VARCHAR2(40),
  NASCIMENTO DATE
);

CREATE TABLE ORDENHAS (
  ID_VACA NUMBER REFERENCES VACAS(ID),
  DATA_ORDENHA DATE,
  LITROS NUMBER(10,2)
);

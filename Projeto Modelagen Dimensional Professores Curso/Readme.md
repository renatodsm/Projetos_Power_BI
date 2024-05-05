# Esquema em Estrela para Análise de Dados de Professores e Cursos
---
Este repositório contém a descrição de um esquema em estrela para análise de dados relacionados a professores, cursos e departamentos em uma instituição educacional.

## Estrutura do Esquema em Estrela

### Tabela Fato (Fato_Professor_Curso)

- `professor_id`: Chave Estrangeira relacionada à tabela de Dimensão `Dim_Professor`.
- `curso_id`: Chave Estrangeira relacionada à tabela de Dimensão `Dim_Curso`.
- `departamento_id`: Chave Estrangeira relacionada à tabela de Dimensão `Dim_Departamento`.
- `data_inicio`: Data de início do curso ministrado pelo professor.
- `data_fim`: Data de término do curso ministrado pelo professor.
- `outras_métricas`: Outras métricas relacionadas ao curso ou ao professor.

### Tabelas Dimensão

1. **Dim_Professor:**
   - `professor_id`: Chave Primária.
   - `nome`: Nome do professor.
   - `sobrenome`: Sobrenome do professor.
   - `título_acadêmico`: Título acadêmico do professor.
   - `departamento_id`: Chave Estrangeira relacionada à tabela de Dimensão `Dim_Departamento`.
   - `outras_informações`: Outras informações sobre o professor, como email, telefone, etc.

2. **Dim_Curso:**
   - `curso_id`: Chave Primária.
   - `nome_curso`: Nome do curso.
   - `descrição_curso`: Descrição do curso.
   - `departamento_id`: Chave Estrangeira relacionada à tabela de Dimensão `Dim_Departamento`.
   - `outras_informações`: Outras informações sobre o curso, como carga horária, nível do curso, etc.

3. **Dim_Departamento:**
   - `departamento_id`: Chave Primária.
   - `nome_departamento`: Nome do departamento.
   - `descrição_departamento`: Descrição do departamento.
   - `outras_informações`: Outras informações sobre o departamento, como localização, chefe do departamento, etc.

4. **Dim_Data:**
   - `data_id`: Chave Primária.
   - `data`: Data em diferentes granularidades (ano, mês, dia).
   - `semana`, `trimestre`, `semestre`, `ano_letivo`: Informações temporais associadas à data.
   - `feriado`: Indica se a data é um feriado ou não.

## Relacionamentos

- Relacionamento um para muitos:
   - Um professor pode ministrar vários cursos ao longo do tempo, mas cada curso é ministrado por apenas um professor.
   - Um departamento pode ter vários professores, mas cada professor está associado a apenas um departamento.

- Relacionamento muitos para muitos:
   - Um curso pode ser ministrado por vários professores, e um professor pode ministrar vários cursos ao longo do tempo.
   - Um curso pode ser oferecido em várias datas diferentes, e uma data pode ter vários cursos sendo oferecidos.

Este esquema em estrela permite uma análise abrangente e eficiente dos dados relacionados a professores, cursos e departamentos, facilitando a extração de insights e tomada de decisões na instituição educacional.
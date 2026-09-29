# Modelagem de Banco de Dados – Sistema de RH

# Professora Ellen Martins Lopes da Silva

## 📚 Sobre o Projeto

Este projeto apresenta a modelagem de um banco de dados para um sistema de Recursos Humanos (RH), com entidades, atributos, chaves primárias e relacionamentos entre as tabelas.

## 🗂️ Entidades e Atributos

### 1. Área de Atuação
- `id_area` (PK)
- `cod_centro_custo`
- `endereco`
- `cod_alfa_num_area`
- `nome_area`

### 2. Empregado
- `id_cod_alfa_num_empregado` (PK)
- `nome_area`
- `endereco`
- `documentos`
- `cod_lotacao`
- `cod_nv_salarial`
- `cod_cargo`

### 3. Dependente
- `id_cod_empregado` (PK)
- `nome`
- `data_nascimento`
- `tipo_identidade`
- `num_identidade`
- `tipo_parentesco`

### 4. Cargo
- `id_cod_alfa_num_cargo` (PK)
- `nome_cargo`
- `nv_hierarquico`
- `cod_LR`
- `ind_nv_gerencial`
- `cod_ref_salarial_min`
- `cod_ref_salarial_max`

### 5. Referência Salarial
- `id_cod_alfa_num_ref_salarial` (PK)
- `valor_salarial_ref`
- `data_inicio_vig_ref`
- `data_final_vigref`

## 🔗 Relacionamentos e Cardinalidades

| Entidade | Relacionamento | Entidade | Cardinalidade |
|---|---|---|---|
| Empregado | Atua em | Área de Atuação | (1,1) para (1,n) |
| Empregado | Possui | Dependente | (1,1) para (0,n) |
| Empregado | Ocupa | Cargo | (1,1) para (1,1) |
| Cargo | Atende | Referência Salarial | (1,1) para (1,n) |

## 🎯 Objetivo

Organizar as informações dos empregados, seus dependentes, cargos, áreas de atuação e referências salariais, facilitando o gerenciamento dos dados de Recursos Humanos.

## 🛠️ Conceitos Utilizados

- Modelagem de banco de dados
- Entidades e atributos
- Chave primária (PK)
- Relacionamentos
- Cardinalidade

---

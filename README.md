# 点集拓扑学

## 主要内容

Bourbaki《数学原本》(Éléments de mathématique) 中《点集拓扑学》一卷的自学笔记。

## 说明

本笔记按 Bourbaki 原书的章节层级组织，对应关系如下：

| Bourbaki 原书 | 本笔记 | 本仓库中的示例 |
|---|---|---|
| 章（Chapitre） | `Content/` 下的**章目录** | `1_Topological_Structures/` |
| 节（§） | 章目录下的**节目录** | `1_Open_sets_neighbourhoods_closed_sets/` |
| 小节（1、2、…） | 节目录下的 **`.tex` 文件** | `1_Open_sets.tex` |

- 目录与文件名取该层级标题的**英译**，并加编号前缀（`1_`、`2_`…，不加前导零）。
- 中文标题写在 `\chapter{...}` 与 `\section{...}` 中：`\chapter{}` 用该**节目录**名的中译，`\section{}` 用该**文件**名的中译。
- 每层目录各有一个 `index.tex`，按顺序汇总对下一层的 `\input`。

定理环境用法、交叉引用（`\cref`）、符号库维护等 **tex 层面的规定**，另见模板《笔记写作》的 README。

## 内容结构

```
Content/
├─ 1_Topological_Structures/
│  ├─ 1_Open_sets_neighbourhoods_closed_sets/
│  ├─ 2_Continuous_functions/
│  ├─ 3_Subspaces_quotient_spaces/
│  ├─ 4_Product_of_topological_spaces/
│  ├─ 5_Open_mappings_and_closed_mappings/
│  ├─ 6_Filters/
│  ├─ 7_Limits/
│  ├─ 8_Hausdorff_spaces_and_regular_spaces/
│  ├─ 9_Compact_spaces_and_locally_compact_spaces/
│  ├─ 10_Proper_mappings/
│  └─ 11_Connectedness/
├─ 2_Uniform_Structures/
│  ├─ 1_Uniform_spaces/
│  ├─ 2_Uniformly_continuous_functions/
│  ├─ 3_Complete_spaces/
│  └─ 4_Relations_between_uniform_spaces_and_compact_spaces/
├─ 3_Topological_Groups/
│  ├─ 1_Topologies_on_groups/
│  ├─ 2_Subgroups_quotient_groups_homomorphisms_homogeneous_spaces_product_groups/
│  ├─ 3_Uniform_structures_on_groups/
│  ├─ 4_Groups_operating_properly_on_a_topological_space_compactness_in_topological_groups_and_spaces_with_operators/
│  ├─ 5_Infinite_sums_in_commutative_groups/
│  ├─ 6_Topological_groups_with_operators_topological_rings_division_rings_and_fields/
│  └─ 7_Inverse_limits_of_topological_groups_and_rings/
├─ 4_Real_Numbers/
│  ├─ 1_Definition_of_real_numbers/
│  ├─ 2_Fundamental_topological_properties_of_the_real_line/
│  ├─ 3_The_field_of_real_numbers/
│  ├─ 4_The_extended_real_line/
│  ├─ 5_Real-valued_functions/
│  ├─ 6_Continuous_and_semi-continuous_real-valued_functions/
│  ├─ 7_Infinite_sums_and_products_of_real_numbers/
│  └─ 8_Usual_expansions_of_real_numbers_the_power_of_R/
├─ 5_One-parameter_groups/
│  ├─ 1_Subgroups_and_quotient_groups_of_R/
│  ├─ 2_Measurement_of_magnitudes/
│  ├─ 3_Topological_characterization_of_the_groups_R_and_T/
│  └─ 4_Exponentials_and_logarithms/
├─ 6_Real_number_spaces_and_projective_spaces/
│  ├─ 1_Real_number_space_R^{n}/
│  ├─ 2_Euclidean_distance_balls_and_spheres/
│  └─ 3_Real_projective_spaces/
├─ 7_The_additive_groups_R^{n}/
│  ├─ 1_Subgroups_and_quotient_groups_of_R^{n}/
│  ├─ 2_Continuous_homomorphisms_of_R^{n}_and_its_quotient_groups/
│  └─ 3_Infinite_sums_in_the_groups_R^{n}/
├─ 8_Complex_numbers/
│  ├─ 1_Complex_numbers_quaternions/
│  ├─ 2_Angular_measure_trigonometric_functions/
│  ├─ 3_Infinite_sums_and_products_of_complex_numbers/
│  └─ 4_Complex_number_spaces_and_projective_spaces/
├─ 9_Use_of_real_numbers_in_general_topology/
│  ├─ 1_Generation_of_a_uniformity_by_a_family_of_pseudometrics_uniformizable_spaces/
│  ├─ 2_Metric_spaces_and_metrizable_spaces/
│  ├─ 3_Metrizable_groups_valued_fields_normed_spaces_and_algebras/
│  ├─ 4_Normal_spaces/
│  ├─ 5_Baire_spaces/
│  └─ 6_Polish_spaces_Souslin_spaces_Borel_sets/
├─ 10_Appendix_Infinite_products_in_normed_algebras/
└─ 11_Function_spaces/
   ├─ 1_The_uniformity_of_S-convergence/
   ├─ 2_Equicontinuous_sets/
   ├─ 3_Special_function_spaces/
   └─ 4_Approximation_of_continuous_real-valued_functions/
```

## 文件结构

```
main.tex          编译入口
structure.sty     样式包：页面设置、定理环境、引用、数学符号库
quiver.sty        交换图支持
Content/          分章正文，每章一个目录，由 index.tex 汇总 \input
commit.py         一键提交并推送（说明见 commit.md）
setup_mode.py     习题编排模式切换（说明见 setup_mode.md）
README.md         本文件：项目说明
CHANGELOG.md      更新日志：tex 配置调整与正文内容调整
```

各脚本的选项与功能分别见 [commit.md](commit.md) 与 [setup_mode.md](setup_mode.md)；符号库由上层目录的 `symbols.py` 统一管理。

## 编译

本笔记使用自建的【笔记写作】模板（样式包 `structure.sty`），须用 **XeLaTeX** 编译：

```bash
xelatex main.tex
```

- **编译环境**：XeLaTeX。模板依赖 ctexbook 与 XeLaTeX 特性，**不支持 pdfLaTeX**。
- **TeXStudio**：建议 4.0 或更高版本。
- `main.pdf` 未纳入版本控制，需本地编译生成。

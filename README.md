# PHD_data
PhD附录中相关表格和图片
所有均在Detail_data中呈现，展示结果包含以下方法：
锚定：Bucher;STC;MAIC;K-STC;RA-MAIC
无锚定：Naive;STC;MAIC;K-STC;RA-MAIC


字段说明：
一、情景标识与参数列（每行代表一个模拟情景）
1) Scenario：情景序号。
2) file_id：情景编码字符串，将关键参数（如N_AC、b_X、b_EM、meanX_AC、corX、sdBC、shapeBC）拼接为可读标识，便于检索与核对。
3) N_AC：AC样本量。
4) b_X：预后效应强度（用于控制协变量对结局的预后作用强弱）。
5) b_EM：效应修饰强度（用于控制效应修饰因子对治疗效应的交互强弱）。
6) meanX_AC：试验间基线差异（重叠程度）参数，刻画AC与外部对照总体在协变量均值层面的偏移幅度。
7) corX：协变量相关系数（用于控制协变量间相关结构）。
8) sdBC：BC协变量标准差（用于控制外部对照总体协变量离散程度）。
9) shapeBC：BC协变量分布形状（例如normal表示正态分布；其他取值对应你设定的分布形状类别）。

二、间接比较方法
本研究在该表中包含以下间接比较方法的结果列组（以列名前缀区分）：
锚定：Bucher（Bucher），maic（MAIC），stc（STC），K_STC（K-STC），RA_MAIC（RA-MAIC）。
非锚定： NAIVE（Naïve），maic（MAIC），stc（STC），K_STC（K-STC），RA_MAIC（RA-MAIC）。

三、各方法的性能指标列
1) .ate：该方法对目标效应的点估计值（ATE估计）。
2) .bias：Bias，点估计的平均偏倚。
3) .mae：Mean absolute error (MAE)，平均绝对误差。
4) .mse：Mean squared error (MSE)，均方误差。
5) .empse：Empirical standard error (EmpSE)，基于重复模拟得到的经验标准误。
6) .vr：Variability ratio (VR)，模型标准误与经验标准误的比值，用于诊断不确定性估计的校准程度。
7) .cov：Coverage，置信区间覆盖率。
8) .ciwidth：CI width，置信区间宽度。
9) .std.bias（或NAIVE.std_bias）：Standardized percent bias，标准化百分比偏倚。
10) .aess.mean（仅适用于maic与RA_MAIC）：Effective sample size (ESS) 的平均值。

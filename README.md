# Applicable for tentatively processed IC50 data in xlsx format (see example format below)
# 能够批量处理经过初步加工的excel存储的IC50数据(见下方数据格式示例)
# Able to deal with an excel file with multiple sheets. Sheets containing non-IC50 data causing fitting failure
# 一个xlsx文件中可以包含多张sheet，但是包含非IC50数据的sheet中的数据会拟合失败
# Export IC50 data and response curve
# 产出IC50和lg剂量-活性曲线图
# Please set the working directory in 2.1
# 请在2.1中设置工作目录，只需要设置一次
# Please ONLY put IC50 data xlsx in the working directory. Other xlsx files will let this script catch the wrong source data
# 工作目录只能存在一个包含初步IC50数据的excel文件，否则脚本会抓取错误
# Default model for fitting include 4PL model and Weibull model. Change model choices in 5.2
# 默认拟合模型包括4PL和Weibull模型（设限或不设限），可以在5.2中添加或删减模型
# Default unit of drug concentration is μM. Change the unit in 6.1
# 默认药物浓度单位为μM，在6.1中可以改变单位



# Applicable formart:
# 数据格式示例
# First line: numeric drug concentration, no unit
# 第一行: 数字类型的药物浓度，无浓度单位
# Second line and latter: Relative cell viability, NO need for Control data, each cell represents a replicate
# 第二行起: 相对细胞活力，不需要对照组数据, 每格代表一次重复
# No string data in the table
# 表格中不应包含文本类型的数据
# Example:
# |100        | 50        | 25        | 12.5     | 6.25     | ... |
# |-----------|-----------|-----------|----------|----------|-----|
# | -0.02513  | -0.00416  | -0.00416  | 0.52889  | 0.58212  | ... |
# | -0.01384  | -0.00013  |  0.01034  | 0.51841  | 0.57163  | ... |
# | -0.02594  | -0.00981  |  0.01196  | 0.68212  | 0.59663  | ... |

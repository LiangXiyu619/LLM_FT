# LLM_FT

https://docs.google.com/document/d/1Qz3DE7_HsR2cDx3Ed43p3ZfGV_GkfaQlFXrWKvWxSss/edit?usp=sharing

## 数据源

https://github.com/amazon-science/esci-data?tab=readme-ov-file

## 数据处理

- scripts/data.ipynb 数据处理代码
- LLaMA-Factory/data/esci/esci_alpaca_train.json 训练集
- LLaMA-Factory/data/esci/esci_alpaca_test.json 测试集
- LLaMA-Factory/data/esci/esci_alpaca_train_2.json 训练集(调整分布后)

## 模型初筛

- scripts/model.ipynb 模型初筛代码
- scripts/data.ipynb 数据处理代码，含模型初筛数据集生成
- data/test_pretrain_model.jsonl 模型初筛数据集
- prediction_results/qwen_test_100_failed_1.jsonl 千问测试结果(格式混乱版)
- prediction_results/qwen_test.jsonl 千问测试结果
- prediction_results/mistral_test_100.jsonl mistral 测试结果

## 微调

https://github.com/hiyouga/LlamaFactory

LLaMA-Factory 文件夹的文件应放在 LLaMA-Factory 库对应位置

- LLaMA-Factory/config/esci_train.yaml 训练配置
- LLaMA-Factory/config/esci_test.yaml 测试配置
- LLaMA-Factory/data/esci/esci_alpaca_train.json 训练集
- LLaMA-Factory/data/esci/esci_alpaca_train_2.json 训练集(调整分布后)
- LLaMA-Factory/data/dataset_info.json 数据集配置，3 个数据集添加到 LLaMA-Factory 对应配置中
- 训练后的 lora 文件和 merge 后的模型文件 to be uploaded

## 评估

- LLaMA-Factory/data/esci/esci_alpaca_test.json 测试集
- prediction_results/baseline_test_output.jsonl qwen 微调前
- prediction_results/lora1_test_output.jsonl qwen 第一次微调
- prediction_results/lora2_test_output.jsonl qwen 第二次微调
- scripts/test_predict.ipynb 评估代码

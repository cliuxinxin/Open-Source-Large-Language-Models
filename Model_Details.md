# Chinese-LLaMA-Alpaca

https://github.com/ymcui/Chinese-LLaMA-Alpaca

这个代码不错，文档很详细，不过并没有给出数据来。


# 悟道·天鹰

https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila

智源研究院开源了其悟道·天鹰大模型，具备中英双语知识。开源版本的基础模型参数量包括70亿和330亿，同时其开源了AquilaChat对话模型和quilaCode文本-代码生成模型，且都已经开放了商业许可。

预训练使用了Pile，RedPajama-Data-1T, Wikipedia, C4, 悟道中文数据集、电子书、专利、百科、论坛, github数据等, 详情可见下图。

采用GPT-3、LLaMA等Decoder-only架构，同时针对中英双语更新了词表，并采用其加速训练方法。其性能上的保障不仅依赖于模型的优化改进，还得益于智源这几年在大模型高质量数据上的积累。

最低硬件需求：运行Aquila-7B系列需要内存30G, 显存18G，生成最大长度 2048 tokens。

# ChatGLM

https://github.com/THUDM/ChatGLM-6B

清华技术成果转化的公司智谱AI开源的GLM系列的对话模型，支持中英两个语种，目前开源了其62亿参数量的模型。其继承了GLM之前的优势，在模型架构上进行了优化，从而使得部署和应用门槛变低，实现大模型在消费级显卡上的推理应用。

经过约 1T 标识符的中英双语训练，辅以监督微调、反馈自助、人类反馈强化学习等技术的加持
62 亿参数

# stanford-alpaca

https://github.com/tatsu-lab/stanford_alpaca

斯坦福发布的alpaca（羊驼模型），是一个基于LLaMA-7B模型微调出一个新模型，其基本原理是让OpenAI的text-davinci-003模型以self-instruct方式生成52K指令样本，以此来微调LLaMA。

该项目已将训练数据、生成训练数据的代码和超参数开源，该项工作由于成本低廉、数据易得，大受欢迎，也开启了低成本ChatGPT的效仿之路。

# belle

https://github.com/LianjiaTech/BELLE

链家推出的

模型机基于llama的，调优的数据一直在优化，可以去这里找找数据。不过数据都是chatgpt生成的。这里也有基于deepspeed的训练代码。

# Falcon

https://huggingface.co/tiiuae

其拥有7B和40B两个参数量尺度，采用GPT式的自回归解码器模型，但其在数据上下了大功夫，从公网上抓取内容构建好初始预训练数据集后，再使用CommonCrawl转储，进行大量过滤并进行大规模去重，
最终得到一个由近5万亿个token组成的庞大预训练数据集。同时又加进了很多精选语料，包括研究论文和社交媒体对话等内容。
但该项目的授权饱受争议，采用"半商业化"授权方式，在收益达到100万后开始有10%的商业费用。

# pile 公开数据集

https://pile.eleuther.ai/

825g 数据，22 个不同的数据源

# OPT

https://ai.facebook.com/blog/democratizing-access-to-large-scale-language-models-with-opt-175b/

800g，180b数据训练


# pythia

https://github.com/EleutherAI/pythia#models

基于 pile 训练的模型，有重复和去重两个部分。

模型类似gpt3，可以看到模型大小和模型结构，

# GPT-NeoXT

https://github.com/EleutherAI/gpt-neox

在 pile 数据集上训练的类似gpt3 的模型

# OIG 指令数据

https://huggingface.co/datasets/laion/OIG

lion 公司整理的 instruct 数据

# GPT-NeoXT-Chat-Base-20B

https://github.com/togethercomputer/OpenChatKit/blob/main/docs/GPT-NeoXT-Chat-Base-20B.md

在OIG上微调了GPT-NeoX 的 20b 版本

# OpenChatKit

前OpenAI研究员所在的Together团队，以及LAION、Ontocord.ai团队共同打造。

可以支持GPT-NeoXT-Chat-Base-20B和 pythia ，而且还有训练模型的代码

# RedPajama-Data

https://github.com/togethercomputer/RedPajama-Data

目前LLama的授权比较有限，只能用作科研，不允许做商用。为了解决商用完全开源问题，RedPajama项目应运而生，其旨在创建一个完全开源的LLaMA复制品，可用于商业应用，并为研究提供更透明的流程。

完整的RedPajama包括了1.2万亿token的数据集，其下一步将着手开始进行大规模训练。

基于这个数据，有开源模型
RedPajama
MPT

# MOSS

https://github.com/OpenLMLab/MOSS

开源的MOSS支持中英两个语种。

且支持插件化，如解方程、搜索等。参数量大16B，在约七千亿中英文以及代码单词上预训练得到，后续经过对话指令微调、插件增强学习和人类偏好训练具备多轮对话能力及使用多种插件的能力。


# ChatYuan

 https://github.com/clue-ai/ChatYuan

元语智能开发团队开发和发布的，
该模型目前只支持中文

底层采用7亿参数规模的T5模型
并基于PromptClue进行了监督微调形成了ChatYuan。

# Colossal AI

https://github.com/hpcaitech/ColossalAI

该项目开源了 instructgpt 的训练方法。使用的时候需要搭配他们的云服务。

# PaLM-rlhf-pytorch

https://github.com/lucidrains/PaLM-rlhf-pytorch

基于 palm 开源了训练rlhf的代码

# ChatLLaMA

https://github.com/nebuly-ai/nebuly/tree/main/optimization/chatllama

基于llama和 deepspeed 的 rlhf 训练过程。

# deepspeed chat

https://github.com/microsoft/DeepSpeed/tree/master/blogs/deepspeed-chat

微软开源的chatgpt的训练方法。还提供付费算力让你自己训练

# PEFT

https://github.com/huggingface/peft

huggingface 开发的一个框架，支持lora等微调方式


# databricks-dolly-15k

https://huggingface.co/datasets/c-s-ale/dolly-15k-instruction-alpaca-format

databricks的员工自己写的对话数据

# AlpacaDataCleaned

https://github.com/gururise/AlpacaDataCleaned

针对羊驼数据进行了清洗。

# gpt-4-llm

https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM

还是使用了gpt生成数据，不过是使用的gpt4来生成的

# 骆驼

https://github.com/LC1332/Luotuo-Chinese-LLM

基于llama和52k数据微调

# 丝绸之路

https://github.com/LC1332/Luotuo-Silk-Road

各种数据翻译成中文

# dolly

https://github.com/databrickslabs/dolly

基于databrick训练的模型，也是基于llama

# chinese-vicuna

https://github.com/Facico/Chinese-Vicuna

进一步降低了微调的难度，在2080上面都可以调llama

# FastChat

https://github.com/lm-sys/FastChat/

训练小羊驼的代码，所有的功能都支持

# LMFLOW


https://github.com/OptimalScale/LMFlow/blob/main/readme/README_zh-hans.md

扩展工具箱，低资源训练模型，感觉是一个缝合怪，里面什么东西都有

# baize

https://github.com/project-baize/baize-chatbot

有一些回答的数据，也是lora的架构





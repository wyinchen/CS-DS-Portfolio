G03 想不到組名 
======================

成員：朱修平、盧德原、楊舒晴、陳宛瑩

## 題目

國寫在升大學考試之國文科目中，與選擇題各佔一半分數之比重，惟我國之國文教學，向來重視古文閱讀、國學常識等，在教學大綱中以選擇題的答寫作為主要教學方向，許多學生對於國寫部分之掌握能力相對不足。因此，本組希望透過分析國寫情意題佳作詞頻，進一步洞察國寫在我國命題方向與佳作取材等寫作方式。


## 結果呈現專案網站

[![Website](https://img.shields.io/website?down_message=offline&up_color=lime&url=https%3A%2F%2Fderekdylu.github.io%2F)](https://rlads2021.github.io/project-derekdylu/index.html)


## 連結

- [投影片](./G03_slides.pdf)
- [書面報告](./G03_report.pdf)  
- [專案網站](https://rlads2021.github.io/project-derekdylu/index.html)
- [Original Repository](https://github.com/derekdylu/LING5505-Final-Project-Group3)


## 根目錄說明文件

- [assets/](./assets/): 入口網頁相依檔案。
- [index.html](./index.html): 入口網頁。


## 其他

### Things required for compiling the Python file

You have to download all the potentially required package according to the commands below,

  **(1) Install required package**
  ```py
    !pip install gdown
    !pip install tensorflow
    !pip install torch
    !pip install transformers
    !pip install CwnSenseTagger
    !pip install CwnGraph
    !pip install ckiptagger
  ```

  **(2) Download required file for ckiptagger**: The commands below let you to save the downloaded file outside the folder that connected to GitHub repository since the file is quite big (about 2GB)
  ```py
    import os
    data_utils.download_data_url(os.path.abspath(os.path.join(os.getcwd(), os.path.pardir)))
  ```

  **(3) Import them**
  ```py
    import numpy as np
    import pandas as pd
    import gdown
    
    import torch
    import transformers
    
    import CwnSenseTagger
    CwnSenseTagger.download()

    import CwnGraph
    CwnGraph.download()
    
    from CwnGraph import CwnBase
    from ckiptagger import data_utils, construct_dictionary, WS, POS, NER
  ```
  **(4) Set the ckiptagger worker**
  ```py
    ws = WS(os.path.abspath(os.path.join(os.getcwd(), os.path.pardir)) + '/data')
    pos = POS(os.path.abspath(os.path.join(os.getcwd(), os.path.pardir)) + '/data')
    ner = NER(os.path.abspath(os.path.join(os.getcwd(), os.path.pardir)) + '/data')
  ```

  **(5) For more information, visit [ckiplab/ckiptagger](https://github.com/ckiplab/ckiptagger)**

### Part of Speech Index
Visit this [page](http://ckipsvr.iis.sinica.edu.tw/papers/category_list.pdf) for the index of part of speech from CKIP Lab.

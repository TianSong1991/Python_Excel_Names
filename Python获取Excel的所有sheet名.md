

```python
import openpyxl
import pandas as pd
```


```python
wb = openpyxl.load_workbook("G:\R\data\DIS\DIS-费用.xlsx")
```

    D:\ProgramData\Anaconda3\lib\site-packages\openpyxl\worksheet\header_footer.py:49: UserWarning: Cannot parse header or footer so it will be ignored
      warn("""Cannot parse header or footer so it will be ignored""")
    


```python
#获取workbook中所有的表格  
sheets = wb.get_sheet_names()  
  
print(sheets) 
```

    ['市场费用', '广告费用', '海外广告支持', '国家电视台', '地方电视台', '交互营销', '网络交互', '体验交互', '参展费用', '门头展台', '渠道促销', '终端价格政策', '促销物资', '样机费', '佣金', '市场调研', '人工成本', '组织运营', '研发费用-主要设计开发2.6；模具0.4', '物流', '运输费', '进出口费用', '保修', '海外售后', 'IT', '财务', '税费', '生产费用', '折旧及摊销', '收入']
    


```python
len(sheets)
```




    30




```python
sheetsname = pd.DataFrame(sheets)
```


```python
sheetsname.to_excel('G:\R\data\DIS\sheetsname.xlsx')
```

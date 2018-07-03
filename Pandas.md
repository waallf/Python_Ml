pip install pandas  
import pandas as pd
## pandas 使用pd.read_csv来读取csv数据  
`csv_data = pd.read_csv("a.csv")`  
* pd.read_csv会将数据载入一个DataFrame中，可以调用head()来粗略观看数据集情况 
`csv_data.head()`  

* describe(),这个函数会罗列出DataFrame的一些相关数据  
`csv_data.describe(include='all')` 

* 扰乱数据  
`csv_data = csv_data.sample(frac=1).resnet_index(drop_True)` 
* 处理数据集中单独的某一列，只需要使用括号标注出那一列，将改名字作为参数传入即可，使用.columns
以数组形式输出DataFrame中所有的列名称  
`csv_data.columns`  
`csv_data['sepal_len']` 
* 得到DataFrame中索引为i的行，需要使用.iloc[i]得到该行数据  
`csv_data.iloc[5]`
* 同时处理行和列的数据  
`csv_data["speal_len"].iloc[5]`
* 处理一个范围内的数据  
`csv_data[['a','b']]` 
### 直接通过列名称来指定  
```
cols_2_4 = csv_data.columns[2:4]  
csv_data[cols_2_4]
csv_data.iloc[5:10]
```
* 混合行，列范围选择  
``` 
clos_2_4 = csv_data.columns[2:4]  
cols_2_4 = csv_data[cols_2_4]  
cols_2_4.ilos[5:10]
```   

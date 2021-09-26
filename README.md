# FDS_Practical_1
my_dict = {    'name' : ['a','b','c','d','e', 'f','g'],
               'age' : [ 20,27,35,55,18,21,35],
               'designation' : ["VP","CEO","CFO","VP","VP","CEO","MD"]}
import pandas as pd
import numpy as np
df=pd.DataFrame(my_dict)
df
	name	age	designation
0	a	20	VP
1	b	27	CEO
2	c	35	CFO
3	d	55	VP
4	e	18	VP
5	f	21	CEO
6	g	35	MD

df.to_csv('csv_fds')
df

df_csv=pd.read_csv('csv_fds')
df_csv

df.to_csv('csv_fds',index=False)
df_csv=pd.read_csv('csv_fds' )
df_csv

import pandas as pd
Location = r"C:\Users\gauta\OneDrive\Desktop\FDS\student-mat.csv"
df = pd.read_csv(Location)
df.head()

import pandas as pd
names =['Bob','Jessica','Mary','John','Mel']
grades=[76,95,77,78,99]
bsdegrees = [1,1,0,0,1]
msdegrees = [2,1,0,0,0]
phdegrees = [0,1,0,0,0]
Degrees = zip(names,grades,bsdegrees,msdegrees,phdegrees)
columns = ['Names','Grades','BS','MS','phD']
df = pd.DataFrame(data = Degrees, columns=columns)
df


import pandas as pd
Location = r"C:\Users\gauta\OneDrive\Desktop\FDS\gradedata.xlsx"
df=pd.read_excel(Location)
# changing columns name
df.columns = ['first','last','sex','age','exer','hrs','grd','addr']
df.head()

import pandas as pd
names =['Bob','Jessica','Mary','John','Mel']
grades=[76,95,77,78,99]
GradeList = zip(names,grades)
df = pd.DataFrame(data = GradeList,columns = ['Names','Grades'])
writer = pd.ExcelWriter('dataframe_FDS.xlsx', engine = 'xlsxwriter')
df.to_excel(writer, sheet_name = 'Sheet1')
writer.save()




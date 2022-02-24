# read_sentence_sql_server
##Connect to SQL Server

import pyodbc

conn = pyodbc.connect('DRIVER={SQL Server};SERVER=xxxxxxx;UID=tomas;PWD=xxxxx')

df= pd.read_sql_query ('''
select  Name, Industry from xxxserverxxx.namedatabase.nametable where column='yyy'
''', conn)

df.head(6)

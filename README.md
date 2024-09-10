# file-tyransfer
https://colab.research.google.com/drive/1Ys44kVvmeZtnICzWz0xgpRnrIOjZAuxp?usp=sharing#scrollTo=SXd9bTZd1aaL
import pandas as pd
import json

with open('trial_1_30.json', 'r') as file:
    data = json.load(file)

df = pd.DataFrame(data)
df = df.drop(columns=['text'])
df.rename(columns={"Input": "input", "Instruction": "instruction","Response":"output"}, inplace=True)

df.head()

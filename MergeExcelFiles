#fileName= array that includes excel files
#header= same headers obtained from excel files
#name= specify the new excell file name
#folderpath= specify the file path to save new file

def getTotalFiles(fileName,header,name,folderpath):
    total=pd.DataFrame(columns=header)

    for file in fileName:
        files=pd.read_excel(file)
        selectedcolumns=files.loc[:,header]
        total=pd.concat([selectedcolumns,total],ignore_index=True)

          # Specify the file path in the target folder
    file_path = os.path.join(folderpath, name + '.xlsx')

    total.to_excel(file_path, index=False)

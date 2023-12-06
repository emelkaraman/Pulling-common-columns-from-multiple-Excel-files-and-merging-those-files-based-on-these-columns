def getHeaders(array):
    headers = set()

    # Read the first file to get headers
    df = pd.read_excel(array[0])
    headers = set(df.columns)

    # Loop through the remaining files
    for file in array[1:]:
        # Read the excel file using pandas
        df = pd.read_excel(file)
        # Get the intersection of headers between current file and headers set
        headers.intersection_update(set(df.columns))

    # Convert the set to a list
    headers = list(headers)
    realheaders=np.array(headers)

    return(realheaders)

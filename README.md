def zvyrazni_bunku(dataframe, r, s):
    def style_func(x):
        df_style = pd.DataFrame("", index=dataframe.index, columns=dataframe.columns)
        df_style.loc[r, s] = "background-color: #4CAF50; color: white"
        return df_style
    return dataframe.style.apply(style_func, axis=None)

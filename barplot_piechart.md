## Reading Data file

To analyse categorical variables, let us load the data set containing information related to the survey on Lung capacities of smokers and non smokers in a state. The data is stored in *LungCapData.txt* .

```{r, loading LungCapData.txt}
LungCapData=read.table(file="LungCapData.txt", header = TRUE,sep="\t")
#LungCapData=read.table(file="LungCapData.txt", header = TRUE,sep="\t")
LungCapData$Gender=as.factor(LungCapData$Gender)
attach(LungCapData)
str(LungCapData)# structure of data
names(LungCapData) # name of variables
class(LungCapData) # type of the variable "smoke"
```

## Creating a Barplot

Barplot is used to analyse catagorical variables. It is important to note that bar plot can be generated only for frequency tables. In R, we use *table()* function on a categorical variable to generate frquency table in a single line code.

```{r, bar plot}
freq_tab=table(Gender)
freq_tab #
barplot(freq_tab,las=1,col=3)
```

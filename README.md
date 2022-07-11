# Handling-datasets-with-NA-values-


data<-read.table("worms.missing.txt", header = TRUE)
View(data)
attach(data)

# Removing NA values
na.omit(data)
newdata<-na.omit(data)
View(newdata)

newdataframe <- na.exclude(data)
View(newdataframe)

#This is quite different because it gives different behaviors in 
#functions in making use of residuals and predictions 


# to test for the completeness of the presence of missing values across a dataframe 
complete.cases(data)


#Replacing NAs with zeros 
data[is.na(data)] <-0
View(data)

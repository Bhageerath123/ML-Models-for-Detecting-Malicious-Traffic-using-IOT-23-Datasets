# ML-Models-for-Detecting-Malicious-Traffic-using-IOT-23-Datasets
Among 23 datasets in IoT-23 dataset, some of them are very small in size i.e., in kilobytes and some are in size more than 2 GB. Also, all 23 datasets in IoT-23 are severely imbalanced.12 malicious labels and a benign label are identified in all 23 datasets. Among these 12 malicious labels, Malicious PartOfHorizontalPortScan, Malicious C&C okiru and Malicious DDoS labels are huge in number(millions) and rest of the malicious labels are less in number. All these labels are not present in every dataset. The description of each dataset is explained in .  So, it is decided to create one file for one label such that all the data of that label taken from the datasets containing that label is grouped into the file. So, total 13 files are created for 13 labels which has now the data from all the 23 datasets.  
To balance the dataset and overcome the issue of underfitting and overfitting on the IoT-23 datasets, 3 datasets were created by taking random amount data from all the 13 files. In this process, randomness in data selection was always maintained. 
For creating 'Dataset_1', N random data was selected from each 12 malicious files and mixed with the benign entries. It contains all 12 malicious labels and benign labels. In this dataset, benign labels are encoded as 1 and all malicious labels are encoded as 0. 
For creating ‘Dataset_2’, N random data was selected from 3 big malicious labels files and mixed with the benign entries in a balanced way. This dataset contains Benign, Malicious DDoS, Malicious PartOfAHorizontalPortScan and Malicious Okiru labels. 
For creating 'Dataset_3', the other malicious labels which are small are taken randomly and mixed with benign label. Oversampling technique was used to make the dataset balanced. This dataset includes 10 different types of labels. The labels taken in this dataset are Benign, Malicious   C&C-FileDownload, Malicious   C&C, Malicious   C&C-Mirai Malicious   FileDownload, Malicious   Attack, Malicious   C&C-HeartBeat, Maliicous   Torii, Malicious   C&C-PartofAHorizontalPortscan, and Malicious   C&C-HeartBeat-FileDownload. 

The labels and their encoded value can be seen in the below table
![image](https://user-images.githubusercontent.com/20298176/111230848-df78bb80-85ad-11eb-9a00-6316712ef44e.png)

After deep examination of IoT-23 datasets, it was observed that most of the datasets are imbalanced. A lot of data preprocessing was conducted to prepare three final datasets out of the 23 smaller datasets in IoT-23. Various machine learning models were implemented using these final datasets but only five models, namely Logistic Regression, Decision Tree Classifier, Random Forest Classifier, XG Boost Classifier and Artificial Neural Network are considered for this research based on the time taken to train the models. Among these five models, the time taken to train Decision tree model and Artificial Neural network model is less when compared to the Logistic Regression, Random Forest and XG Boost models. In terms of model evaluation metrics, with the exception of Logistic Regression, the other four model’s performance is almost 100 percent across the three datasets. 


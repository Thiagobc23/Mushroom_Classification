## Classification

#### The objective was to classify mushrooms between edible and poisonous with the following attributes:

    cap-shape:                  bell=b,conical=c,convex=x,flat=f, knobbed=k,sunken=s
    cap-surface:                fibrous=f,grooves=g,scaly=y,smooth=s
    cap-color:                  brown=n,buff=b,cinnamon=c,gray=g,green=r,pink=p,purple=u,red=e,white=w,yellow=y
    bruises:                    bruises=t,no=f
    odor:                       almond=a,anise=l,creosote=c,fishy=y,foul=f,musty=m,none=n,pungent=p,spicy=s
    gill-attachment:            attached=a,descending=d,free=f,notched=n
    gill-spacing:               close=c,crowded=w,distant=d
    gill-size:                  broad=b,narrow=n
    gill-color:                 black=k,brown=n,buff=b,chocolate=h,gray=g, green=r,orange=o,pink=p,purple=u,red=e,white=w,yellow=y
    stalk-shape:                enlarging=e,tapering=t
    stalk-root:                 bulbous=b,club=c,cup=u,equal=e,rhizomorphs=z,rooted=r,missing=?
    stalk-surface-above-ring:   fibrous=f,scaly=y,silky=k,smooth=s
    stalk-surface-below-ring:   fibrous=f,scaly=y,silky=k,smooth=s
    stalk-color-above-ring:     brown=n,buff=b,cinnamon=c,gray=g,orange=o,pink=p,red=e,white=w,yellow=y
    stalk-color-below-ring:     brown=n,buff=b,cinnamon=c,gray=g,orange=o,pink=p,red=e,white=w,yellow=y
    veil-type:                  partial=p,universal=u
    veil-color:                 brown=n,orange=o,white=w,yellow=y
    ring-number:                none=n,one=o,two=t
    ring-type:                  cobwebby=c,evanescent=e,flaring=f,large=l,none=n,pendant=p,sheathing=s,zone=z
    spore-print-color:          black=k,brown=n,buff=b,chocolate=h,green=r,orange=o,purple=u,white=w,yellow=y
    population:                 abundant=a,clustered=c,numerous=n,scattered=s,several=v,solitary=y
    habitat:                    grasses=g,leaves=l,meadows=m,paths=p,urban=u,waste=w,woods=d
    
Inspired by https://www.kaggle.com/coolman/different-classification-techniques-python  
Adapted to categorical classification on https://www.kaggle.com/uciml/mushroom-classification  
  
Imports:  
numpy  
pandas  
sklearn  
matplotlib  
xgboost  
ipywidgets  

### Feature Selection  

I used Recursive Feature Elimination (RFE) to recursively test logistical regression models and select the subcategories that were most accurate at predicting the output.  
The selected categories were: odor, gill-size, stalk-surface-above-ring, stalk-color-below-ring, spore-print-color  

### Methods tested  

Naive Bayes  
Nearest Neighbors  
Decision Tree  
Random Forest  
XGBoost  
Support Vector Machine (SVM)  
Stochastic Gradient Descent (SGD)  
Multi Layer Perceptron (MLP)  

### Results  
  
Tests were performed without assigning a random seed, replicating this tests will bring similar but no equal results. 

| CLASSIFIER                        | Accuracy with 90% training | Accuracy with 80% training | Accuracy with 70% training |
|-----------------------------------|----------------------------|----------------------------|----------------------------|
| Naive Bayes                       | 98.40%                     | 98.65%                     | 98.76%                     |
| Nearest Neighbors                 | 100%                       | 100%                       | 100%                       |
| Decision Tree                     | 100%                       | 100%                       | 100%                       |
| Random Forest                     | 100%                       | 100%                       | 100%                       |
| XGBoost                           | 100%                       | 100%                       | 100%                       |
| Support Vector Machine (SVM)      | 100%                       | 100%                       | 100%                       |
| Stochastic Gradient Descent (SGD) | 99.88%                     | 99.87%                     | 98.31%                     |
| Multi Layer Perceptron (MLP)      | 100%                       | 100%                       | 100%                       |

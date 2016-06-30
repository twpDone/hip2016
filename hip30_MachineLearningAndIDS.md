#Machine Learning

Focused on anomaly detection, to prevent *DOS* ans so much more.

##Very Commercial But
Usefull for spam protection

Few years ago Gmail implemented a spam filter, 
which worked much better than the hotmail's one 

##Common uses
* "User who bought this also bought ..."
* "You might be instressted by ..."

##ML + Anomaly Detection
To a Wider approach, to detect for exemple:
* new attacks
* bad behaviors
* weird behaviors
* ...

##Bad if system is wrong
* *very* intollerant to errors (eg bitshift, ..)

##Lack of training data
* On what data train the system
* very hard to gather *clean* datas

##Evaluation pb
Its very hard to devise the model, its much harder than building the system
Hard to evaluate *wrong behavior* because bad behavior can be derivated from good ones

##AD system failed
* Many false positives
* 

##Do
* generate time series
* select representative features
* train and tune the model of '*normality'*
* *alert* if incoming points *deviate* from model

##"Model"
* centroid clusters
* good for online learning

Easy to see if behavior is outside your clusters

###Selecting feature
* *most challenging* problem
* Can be shorten by "parameter optimisation problem" 

*Many issues* to define what you need
You can use automation by statistics rank to select theses

###How good is my anomaly detector
* Evaluating *false* positives
* Evaluating *true* positives
* ..*

##Attack This ?
* manipulate learning system (to permit a specific attack)
* degarde performance

"Chaff" *???* (ML term ?)
###Attack on PCA-Based sys
Similar to "chaff" based on unprecise detection

The Detection "Shift" and detect something different than what was expected.
You have the detect that shift.

`Much more clear with the graphic of the slides`

#Results
* Generating the chaff is hard
* Evade about 38% of the time
* Still vulnerable
  * need an human to check things

see @CCHIO on twitter




# Hand-Posture-Recognition

Hand gestures are natural, intuitive and require almost no learning or remembering for humans but for machines it is very difficult to understand as every person is unique and gives a slightly different input. 

There are motion capture gloves available which translate physical hand gestures into digital coordinate data.

I am using this data to correctly identify 5 unique hand postures in digital world by classifying various hand positions from spatial data.

The Dataset contains motion capture data of the left hand of 12 users.

Each user wears a glove which has markers along the all fingers and thumb as well as a rigid pattern of markers on the back of the glove was used to establish a local coordinate system for the hand.

These markers give the spatial data of the hand in 3D space, which can be used to recreate this information digitally on a computer.

The data consists of 78096 rows and 38 columns(having User, Class and columns for coordinates). 
User: It contains data of 12 users
Class: The given record ranges from 
1 to 5 = Fist(with thumb out)
2 = Stop(hand flat)
3 = Point 1(pointer finger)
4 = Point 2(middle finger)
5 = Grab(fingers curled)

Markers: this variable consists of three coordinates Xi, Yi and Zi. 
Where i ranges from 0 to 11.
Each record is a set of all three coordinates with respective i-th value. The i-th value does not necessarily corresponds to the i-th marker of a different record.

I then proceeded with EDA where i did outlier treatment, missing value imputation

I then used Logistic Regression using Leave One Out Cross Validation, then Random Forrest and lastly XGBoost, Random Forest giving best results!






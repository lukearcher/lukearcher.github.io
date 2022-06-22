# Excel Stuff

SMALL and LARGE formulas<br>
TRANSPOSE formula<br>

#### clustering
convert variables to numeric<br>
standardize them... subtract mean and divide by standard deviation<br>
set up the cluster centers... at the bottom of the variables... one row per customer<br>
set up the distance calcs... {sqrt(sum(((variables - centers)^2))}<br>
calc the min distance per customer<br>
find the cluster<br>
set up the total distance... sum of of the min distances<br>
<i>solver</i>:
* set total distance to min
* by changing the cluster centers
* subject to the constraints that the centers are <= 1
* make unconstrained variables non negative
* use the evolutionary algorithm
* play around with the options...<br>
insights:<br>
* conditional format the cluster centers... see where the splits are

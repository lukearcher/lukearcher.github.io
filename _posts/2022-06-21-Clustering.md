# Clustering

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
* play around with the options

<i>insights</i>:<br>
* conditional format the cluster centers... see where the splits are

<i>silhouette scores</i>:<br>
create the distance matrix<br>
calculate the distance of each person from all people in the other clusters<br>
calculate the closest distance<br>
calculate the second closest distance<br>
calculate the distance to the assigned cluster<br>
calculate the distance to the neighboring cluster<br>
calculate the silhouette value... neighbouring - assigned / max of these <br>
get the silhouette score<br>

<i>spherical k-means (k medians with cosine distance) - best used for binary problems</i>:<br>
calculate the cosine difference: iferror(1 - sumproduct(variables - cluster centers)/(sqrt(sum(variables)) * sqrt(sum(cluster centers))),1)<br>
solve - this time change the <= 1 constraint to be binary

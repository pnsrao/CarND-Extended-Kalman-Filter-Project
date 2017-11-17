# Writeup

The initial version mostly used the code from the lectures and integrated the Lidar and Radar data. 
Note that the velocity was initialized to zero.

It was seen that the RMSE was very high in the beginning and did not converge to a steady state by the 
end of the data file. On further debugging, it seemed that the issue was with Radar updates. On removing Radar 
data, I did see lower RMSE values, even though they were a bit higher than the rubric requirements.

The inability to initialize velocities with measurements seemed to have affected Radar updates much more 
significantly. Since the computation of the error vector relies on the velocity term. 

As an initial debug effort, I skipped the first 4 Radar updates until Lidar converged to a true value.

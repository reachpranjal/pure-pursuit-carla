# Lane Centering using Pure Pursuit Controller in Carla

In the Pure Pursuit method, a target point is identified at a distance called look-ahead distance away from the vehicle on the desired path. The steering angle is computed based on Kinematic Bicycle Model. The look-ahead distance is proportional to the forward velocity, which gives rise to a tuning factor called proportional gain.

## Algorithm

![fig](/img/diagram.jpg)
```
For each instant in time {
 - Compute 𝑙_𝑑 = tuning_factor x forward_vel
 - Find TP = (𝑡_𝑝𝑥, 𝑡_𝑝𝑦) as intersection of desired path with circle of radius 𝑙_𝑑 around the rear wheel
 - Determine α = 𝑡𝑎𝑛^(−1) (𝑡_𝑝𝑥  , 𝑡_𝑝𝑦)
 - Finally, calculate steering angle  
 }
 ```
 
 ![output](/img/pure_pursuit_gif.gif)

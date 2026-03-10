# Containers and Orchestration

## Docker
Quickly deploy and scale applications into any environment.
Think of docker I think like a stamp? So you have an image, and you can use that image over and over again, and it'll be the same.

What's the difference between a docker image and a container?

Docker image is the template. It's the blueprint dbt that we make.
The container is the thing it gets passed into? Or it's the instance of that image running. It's an image-instance.
So the image, the template, that persists. The container itself can be temporary, because it's just the one occasion of it running.

With docker, we tell it how to build our image with a dockerfile. 

Anaology, why we use containers
So in the old days, we had 2 lunch boxes. Those 2 lunch boxes sat in 2 completely different buildings. Those buildings had to be separately maintained, their foundations, walls, patching, everything. They can't communicate particularly efficiently between the buildings.
So instead someone said, just take those 2 lunch boxes, make sure they're sealed so nothing can spill out, and put them in the same building, on the same shelf. Suddenly they can talk to eachother much better. Also they're in the same space, so there's just one space to maintain and they'll keep in sync better.


![Container_vs_VMs](https://github.com/Prumita/Learning-Journal/blob/main/Screenshots/5.3_Containers_vs_VMs.png)

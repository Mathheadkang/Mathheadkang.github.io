---
layout: page
title: Introduction
permalink: /research/introduction/
---

# Description

My research focus on the objects called "[Manifold](https://en.wikipedia.org/wiki/Manifold)", which you may think they are higher dimensional "surfaces".
- **Definition**: a *Manifold* is space that around each point it "likes" Euclidean space.

One sentence to summerize my research:
- My research explores the "universe" of all possible geometric shapes on manifolds, classifying how complex spaces can collapse into extreme boundaries and proving how they evolve over time to reveal their fundamental structure.

# Contents
- [Geometry and Topology](#geometry-and-topology)
- [Metric Equivalence](#metric-equivalence)
- [Moduli space of metrics](#moduli-space-of-metrics)
- [Study of Moduli space: Sequential Limit](#study-of-moduli-space-sequential-limit)
- [Study of Moduli space: Flow Method](#study-of-moduli-space-flow-method)

# Geometry and Topology
I will introduce two concepts first: Geometry and Topology

Let's fix our discussion on 2 dimension surfaces for now. In dimension one, there is actually no geometry. All of the "closed" 1 dimensional curves are just loops, they are "equivalent" geometrically and topologically. In dimension 2, we call a 2 dimensional manifold a *surface*. Below are some examples of surfaces.
![Riemann_surface](../../assets/images/Riemann_surfaces.png)
## What is Topology?
*Topology* is the study of shape in a very relaxed sense. Two objects are topologically the same if you can turn one into the other using only those allowed moves. Topology ignores exact sizes and distances.
It only cares about *connectivity* and *holes*.

Imagine objects made of perfectly stretchy rubber:
- You are allowed to stretch, bend, twist, and squish
- You are not allowed to:
- tear the object
- glue parts together
- punch new holes

Try <a href="{{ site.baseurl }}/research/high_level_research/surface_deformation.html"><button type="button">Surface Deformation</button></a> yourself! 

![surface deformation](../../assets/images/surface_deformation.gif)

You may have a cool observation: 
- If two (closed) surfaces are topologically equivalent if they have the same number of "holes".

This is absolutely correct. In dimension 2, the reverse direction is also correct:
- If two (closed) surfaces have the same number of "holes", then they are topologically equivalent.

So the number of holes is a permanent fingerprint. Mathematically, this is called [Genus](https://en.wikipedia.org/wiki/Genus_(mathematics)), which is the simplest *topological invariant*. 

You may see the topology in this case is "discrete" in nature (Genus can only be positive integers instead of real number).

## What is Geometry?
If we view topology property is something which is "soft", then *Geometry* is the "hard" contrary. For topological property, we ignore "wrinkles", "bumps" and other weird distortions. But for geometric property, we care.
The simplest "hard" object on surfaces is *distance* of two points.

How can we define the distance on a surface? Recall on Euclidean space, we have: 
- Among curves connecting two points, the straight line is the shortest.

Thus the distance between two points are defined to be the length of the straight line segment connecting two points. 

On surfaces, we use similar definition:
- The distance between two points is the minimal length among all curves connecting these two points.

Now, we are ready to see an example distinguishes geometry and topology:

![geodesic](../../assets/images/geodesic_sphere.png)

Take the picture for example. A "sphere" is topologically equivalent to a "potato", since there is no hole at all. But the disance between the "north pole" and "south pole" are not the same. Thus, distance is not a topological property, it tides with the shape.

We see different "shape" admits different distance between points. We shall call the "shape" as [metric](https://en.wikipedia.org/wiki/Riemannian_manifold), as it determines distance. We can say in the <a href="surface_deformation.html"><button type="button">Surface Deformation</button></a> you produce a lot of different metrics on the same surface.

You may see the geometry is "continuous" in nature (We can continuously deform a surface without changing its topology). 

# Metric Equivalence
As a differential geometor, I am more interested in metrics. We see that a surface can admit a lot metrics. Here is a big problem:
- How can we distinguish two metrics?

This question is hard. I will answer this question in two steps.

## Metric Local Equivalence: Curvature
We can first formulate it locally. What I mean is
- How can we distinguish two metrics near the same point, say the origin?

Previously, we have seen a metric can determine the distance. But it is a complicated function and not "local" enough. One may think we can let the neighborhood to shrink to the origin. However, since surface is locally "like" Euclidean space $\mathbb{R}^2$, at the origin, it should be exactly Eculidean space, which is the same for each point. So distance is not a suitable invariant.

![Curvature_locally](../../assets/images/local_curvature.png)

Then, what should be the correct invariant? If you take a look at the picture above, you can observe the difference: the left picture is more "spiky" and right picture is "flatter". In geometry, there is a concept to decribe it: [*curvature*](https://en.wikipedia.org/wiki/Curvature). 
- Curvature describe how manifold is "bent" at each point and is a local invariant.

In the surface case, we can consider "curvature" is a number defined at each point, whose value is how "spiky" it is around this point.

## Metric Global Equivalence

If you agree with this local picture, we can move on to the global question. Think about these two metrics on sphere:
![Two_metrics](../../assets/images/two_metrics.png)

These two "spiky" spheres are exactly the same surfaces, but just differ by an angle. However, if we look at the corresponding point on the right of the red dot on the left (not the red dot on the right since they are differ by an angle). The curvatures are different, hence these two metric locally are not equivalent. But can we say these two metrics are not equivalent? They are exactly the same "spiky" spheres but in a different angle!!

Motivate from this, we need to be more careful about what we mean "metric equivalence". 

- Two metrics are equivalent if they are only differed by a "rotation".

In general, the "rotation" is defined by [diffeomorphism](https://en.wikipedia.org/wiki/Diffeomorphism). 

Now, our metric equivalence definition matches with our intuition. The same spirit holds in physics, where we should always find the quantities that is [independent of observors](https://en.wikipedia.org/wiki/Frame_of_reference).
# Moduli space of metrics
As we have seen, on a surface with fixed the topology, it can admits a lot of metrics, where we count the equivalent metric as one metric. If we put all of these metrics into a space and consider them as whole, it becomes the concept of [Moduli space](https://en.wikipedia.org/wiki/Moduli_space) of metrics.

## Geometric Application
In the modern view point of geometry, instead of looking at isolated metrics itself, we should regard all of the metrics as a whole and look at its property. Study such moduli space can lead to the answer of the following two core questions of differential geometry:
- Manifold with which topology property can admit certain metric;

- Manifold with which metric must have certain topology property.

For example, in dimension 2, the famous [uniformization theorem](https://en.wikipedia.org/wiki/Uniformization_theorem) can be stated.

**Theorem**
- A closed surface admits a positive constant curvature metric if and on if the genus is 0 (sphere);
- A closed surface admits a zero curvature metric if and on if the genus is 1 (torus);
- A closed surface admits a negative constant curvature metric if and on if the genus is $\geq 2$.

You can image that we need to go and scan the whole moduli space to find such metric. And different underlining topology resulting different moduli space, give us existence and non-existence results. 

## Distance on Moduli space: Gromov-Hausdorff distance
Here comes the fun part. On a surface, like we have seen, no matter how weird the metric is, we can still measure the distance between two points. One suprising fact is that for two metrics, we can also measure the "distance". That is to say that we can equip the moduli space with a metric structure. This metric is called [Gromov-Hausdorff distance](https://en.wikipedia.org/wiki/Gromov–Hausdorff_convergence).

The precise definition of Gromov-Hausdorff distance is involved. However, conceptually it is simple. In one sentence:
- Two spaces are close in Gromov–Hausdorff distance if you can match their points so that all distances are almost preserved.

It is still kind of abstract. Let's see some examples.

The first example: If you still remember the case that two indentical spiky spheres with different rotation angle. Then what is the Gromov-Hausdorff distance? In fact, we can rotate one spiky sphere so that the metric after rotation is a equivalent metric to the other. Thus, their Gromov-Hausdorff distance should be 0. This is intuitively true: since they represent the "same point" in the moduli space, their distance should be 0.

To get a Gromov-Hausdorff distance close example, take a look at this picture:
![GH_close](../../assets/images/GH_close.png)
The spikes on the left ball is very thin. If we put both spaces into a common “room”, the spherical part are almost identical, which the spikes are almost negligible. Gromov-Hausdorff distance captures global shape while ignoring small geometric noise.

Try this interactive example: <a href="{{ site.baseurl }}/research/high_level_research/GH_surface.html"><button type="button">Gromov-Hausdorff</button></a>

![torus_collapsing](../../assets/images/torus_collapse.gif)

In this example, we can continuosly deform the metric on sphere and torus in the Gromov-Hausdorff sense. Does this looks familar to you? In fact, <a href="{{ site.baseurl }}/research/high_level_research/surface_deformation.html"><button type="button">Surface Deformation</button></a> can be seen in this way: 
- *the Gromov-Hausdorff distance between the moving metric and the model metric (spherical or standard torus) is becoming smaller and smaller.* 

A slight difference is that in Gromov-Hausdorff sense, the metric can be closed to a different dimensional space, which means the topology is changed. As the picture shows, torus can "collapse" to a circle, which is a lower dimensional space.

Intuitively speaking,
- What you look like close are close in Gromov-Hausdorff distance.

# Study of Moduli space: Sequential Limit
Finally, I can introduce my research part.

Like I said, my research focus on the moduli space of metrics. I mainly work on higher dimension spaces, so let's restore the terminology "manifold".

One interesting question is:
- What is the boundary of the moduli space?

We have introduced the Gromov-Hausdorff distance. To say "boundary", which is like a finite distance thing, so we may need to impose some "conditions" on the metrics and consider a "subset" of metrics to avoid distance tends to infinity. I worked on a subset of the moduli space whose metrics satisfies a very natural "condition" in high dimension. 

A way to understand the boundary is to find a sequence of metrics to approach to the boundary. Like in the real number, we can take a [limit](https://en.wikipedia.org/wiki/Limit_(mathematics)). Under Gromov-Hausdorff distance, we can also take a [limit](https://en.wikipedia.org/wiki/Limit_(mathematics)). But the problem is that, the limit may not be "manifold" anymore. Metric degenerations can happen, and topology will change. The "collapsing" is one type of degenerations. There are a lot of degenerations which are unknown. So one of my work can be stated in this way. See details in my [research](../Expert/index.md).
- **Theorem** Consider the moduli space satisfies the natural "condition", 
  - If we assume they are not "collapsing", in dimension 3 and 4, all of the "boundaries" are classified. In any dimension, the classification of the "boundaries" becomes an "algebraic" ([group theory](https://en.wikipedia.org/wiki/Group_theory)) problem.
  - If we allow "collapsing", new examples are discovered.

An illustration of this new examples is like the one in my homepage:
![geometry_singularity](../../assets/images/geometric_singularity.gif)

We can see the left manifold is roughly "unchanged", while the right manfiold is "collapsing" to lower dimension. The "linking neck" region is shrinking to a point. 

A fun fact is that the "linking neck" region is actually a [Schwarzschild_metric](https://en.wikipedia.org/wiki/Schwarzschild_metric), which is actually a mathematical model for the [black hole](https://en.wikipedia.org/wiki/Black_hole).

# Study of Moduli space: Flow Method
Another way to study the moduli space is to using the so-called "flow method". The most famous flow among others is [Ricci flow](https://en.wikipedia.org/wiki/Ricci_flow).

"Flow method" often seeks the answer to the above two questions:

- Manifold with which topology property can admit certain metric;

- Manifold with which metric must have certain topology property.

Let's mainly focus on Ricci flow and ponder the question. 
- Why Ricci flow is a suitable "weapon" to answer the above two question?

For every point on a manifold, there is a curvature, which at the begining, could be different for different points. Image the manifold is like a closed chamber and 
the curvature is like "[heat](https://en.wikipedia.org/wiki/Heat)" distribution. If there is no other heat source, the heat distribution will be more and more "homogeneous", and eventually, the heat will be evenly distributed in the chamber. Ricci flow is an analog of the [heat flow](https://en.wikipedia.org/wiki/Heat_equation). Idealy, it will make everywhere on the manifold the constant curvature.

You may recall this picture:
![Ricci flow](../../assets/images/RF.gif)

On 2 dimension sphere, you can see the "bumps" are like the curvature distribution on sphere, and Ricci flow will make the high and low curvatrue region more "spherical". In the end, it will get the desired metric with constant curvature everywhere, the round metric. With some proof, we can say:
- A 2 dimension sphere (topological condition) admit a positive constant curvature metric.

However, this intuition fails in 3 and higher dimension. The biggest issue is that "singularity" will occure, and prevent the flow to extend further. What I mean "singularity" is the place where curvature tends to infinity. This does not happen in the heat flow, but inevitable in Ricci flow. That is why it took a generation to fully solve the [Poincaré conjecture](https://en.wikipedia.org/wiki/Poincaré_conjecture), the main difficulty is how to deal with singularites. The whole proof basically can be summerized into two steps.
- A 3 dimensional "simply connected" manifold admit a metric that [Ricci flow with surgery](https://en.wikipedia.org/wiki/Poincaré_conjecture#Ricci_flow_with_surgery) that will terminate in finite time for all componenents.
- A 3 manifold admit a metric that [Ricci flow with surgery](https://en.wikipedia.org/wiki/Poincaré_conjecture#Ricci_flow_with_surgery) that will terminate in finite time for all componenents must be a 3 dimensional sphere.

To wrap it up, Ricci flow solves a pure topological conjecture, which is very impressive. I will write "A higher level introduction to Poincaré conjecture" in the future.

Now, I want to summerize what I have done. We consider a flow which is very natural and closed related to Ricci flow. We call this $\alpha$-Ricci flow. Me and my coauthors show the following results (we are still working on some part of the proof).
- **Theorem** Consider the $\alpha$-Ricci flow.
    - The $\alpha$-Ricci flow on 2-torus will either "collapse" to a circle or to a point in the Gromov-Hausdorff distance, depending on a rationality condition initially;
    - The $\alpha$-Ricci flow with surgery on some 3 manifold will exist forever and converge to the desired metric in the Gromov-Hausdorff distance.

If you are interested in the details, please take a look at my [research](../Expert/index.md).
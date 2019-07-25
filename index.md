<script>var clicky_site_ids = clicky_site_ids || []; clicky_site_ids.push(101198209);</script>
<script async src="//static.getclicky.com/js"></script>
<noscript><p><img alt="Clicky" width="1" height="1" src="//in.getclicky.com/101198209ns.gif" /></p></noscript>

<p align="center">
    <img src="nick_rogers_cropped.png" width="256">
</p>

A self-taught programmer, I love problem solving and enjoy spending time building tools and front-end projects that inspire and excite. I have published a few iOS apps and I am comfortable working in C/C++, Swift, Objective-C and Python. Here you will find a curated list of some of my favorite and most current projects. [Check out my GitHub account](https://github.com/mnickrogers) for more.

<p align="center">
[LinkedIn](https://www.linkedin.com/in/mnickrogers/)
</p>

# Noteworthy Projects

## EatUp - iOS

Remember what you like to eat each time you visit a restaurant.

<p align="center">
    <img src="eatup.gif" height="400">
</p>

[EatUp](https://apps.apple.com/us/app/eatup-save-restaurants-and-food/id1224974237) gives users the ability to save food, restaurants and recipes; food can be associated with a given restaurant and restaurants can be displayed by nearby location, allowing folks to recall exactly what they've had before when they return to a restaurant. Designing and coding EatUp required writing a lot of custom views in order to get the overall desired look and feel. The light animations are supposed to contrast the heavy solid blocks of colored space created by the UI elements. From an engineering perspective, EatUp utilizes Core Data to store information and also needed to optimize custom user images to efficiently layout and display in a collection view without overusing system resources.

## MapMark - iOS

Location bookmarking and grouping done right.

<p align="center">
<img src="mapmark.gif" height="400">
</p>

### About

[MapMark](https://apps.apple.com/us/app/mapmark/id1131505775) is a navigational and reference utility that allows users to bookmark locations and organize them under different "bags." For example, you could create a bag for your upcoming vacation and save all the places you wish to visit within it. You can add notes to pins that you have saved as well. Additionally, you can get routes through all the pins within a bag. MapMark allows you to export your bookmarked locations, within their associated bags, as a CSV file.

Building MapMark was an exciting challenge in both interface design and software engineering. In terms of interface design, the goal was to strike a balance between presenting information about bookmarked locations within a bag while also not distracting from the map that helps to visualize this information. From an engineering perspective, achieving my desired look required writing my own custom interface elements (such as the unique dark-themed buttons); it also required learning how to store and manipulate geospatial information. 

### Design

While other navigational apps may make a zero-sum trade-off by presenting a full-screen map in one view and then a list of bookmarked locations in another view, MapMark combines these two views into one so that users can see both a map of their pins and the names of their saved pins in one view. This creates a more logical interface structure and hierarchy since we logically associate a bookmarked location on a map with that location's name (and vice versa) anyways. It also means that notes about a pin can be saved in a separate view without adding additional complexity; this makes since anyways as additional details about a pin can be safely disassociated with the map-based visualization of that pin. With this design, getting access to all of the information about a bookmarked location takes at most two taps from the launch screen. Nice and efficient :)

### Engineering

From an engineering perspective, my favorite challenge was building the routing feature of MapMark. This is the part that allows users to get an efficient route connecting all of their bookmarked locations within a given bag. Solving this was an exercise in data structures and algorithms where I used a graph to store pins and implemented a custom variant of breadth-first-search (BFS) to search the graph, starting from a given node, along the shortest path to the next node. Of course, the underlying assumption is that the shortest path between nodes A and B for the whole graph will always render the shortest possible path tree. We can contrive cases where this would not hold, but on average it works just fine. 

I opted for a modified BFS method over some others for two reasons. The first was simplicity; I'm going to keep developing MapMark, so I wanted to get a feel for what parts to focus on. Minimizing complexity at the start was an important goal. Second, it's efficient and it works. Simplicity doesn't matter if something doesn't do what it's supposed to. Given that the BFS method works, I prefer it to some other traveling salesmen-esque solutions.

In the future, I can update this to show some stats other than just visualize a route (for example, it could list the route's length, driving time, etc.).

## Other Github Repos

## Bayesian-Sequence (C++)
[Check it out here!](https://github.com/mnickrogers/Bayesian-Sequence) This is one I'm still in the middle of, but the idea is pretty simple: Bayesian inference gives us a method of calculating probabilities based on our prior knowledge and observed events. This project creates a way to sequence observations into a synchronized prediction.

## Collapsible-TableView (Swift)
Located [here](https://github.com/mnickrogers/Collapsible-TableView). An implementation of a data model allowing a UITableView to be collapsed by its headers.

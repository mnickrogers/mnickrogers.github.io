<script>var clicky_site_ids = clicky_site_ids || []; clicky_site_ids.push(101198209);</script>
<script async src="//static.getclicky.com/js"></script>
<noscript><p><img alt="Clicky" width="1" height="1" src="//in.getclicky.com/101198209ns.gif" /></p></noscript>

<p align="center">
    <img src="nick_rogers_cropped.png" width="256">
</p>

I love problem solving and computers are tools that let us solve amazing problems — everything from what user interfaces best allow people to freely share their thoughts with each other to how best to design an algorithm to search across vast records stored in a database.

# Noteworthy Projects

## EatUp - iOS
<p align="center">
    <img src="eatup.gif" height="400">
</p>

## MapMark - iOS
<p align="center">
<img src="mapmark.gif" height="400">
</p>

MapMark is a navigational and reference utility that allows users to bookmark locations and organize them under different "bags." For example, you could create a bag for your upcoming vacation and save all the places you wish to visit within it. You can add notes to pins that you have saved as well. Additionally, you can get routes through all the pins within a bag. MapMark allows you to export your bookmarked locations, within their associated bags, as a CSV file.

Building MapMark was an exciting challenge in both interface design and software engineering. In terms of interface design, the goal was to strike a balance between presenting information about bookmarked locations within a bag while also not distracting from the map that helps to visualize this information. While other navigational apps may make a zero-sum trade-off by presenting a full-screen map in one view and then a list of bookmarked locations in another view, MapMark combines these two views into one so that users can see both a map of their pins and the names of their saved pins in one view. This creates a more logical interface structure and hierarchy since we logically associate a bookmarked location on a map with that location's name (and vice versa) anyways. It also means that notes about a pin can be saved in a separate view without adding additional complexity; this makes since anyways as additional details about a pin can be safely disassociated with the map-based visualization of that pin anyways. With this design, getting access to all of the information about a bookmarked location takes at most two taps from the launch screen. Nice and efficient :)

From an engineering perspective, my favorite challenge was building the routing feature of MapMark. This is the part that allows users to get an efficient route connecting all of their bookmarked locations within a given bag. Solving this was an exercise in data structures and algorithms where I used a graph to store pins and implemented a custom variant of breadth-first-search (BFS) to search the graph, starting from a given node, along the shortest path to the next node. Of course, the underlying assumption is that the shortest path between nodes A and B for the whole graph will always render the shortest possible path tree. We can contrive cases where this would not hold, but on average it works just fine. I opted for this method over some others for two reasons. The first was simplicity; I'm going to keep developing MapMark, so I wanted to get a feel for what parts to focus on. Minimizing complexity at the start was an important goal. Second, it's efficient and it works. Simplicity doesn't matter if something doesn't do what it's supposed to. Given that the BFS method works, I prefer it to some other traveling salesmen-esque solutions.

In the future, I can update this to show some stats other than just visualize a route (for example, it could list the route's length, driving time, etc.).

## Bayesian-Sequence
[Check it out here!](https://github.com/mnickrogers/Bayesian-Sequence) This is one I'm still in the middle of, but the idea is pretty simple: Bayesian inference gives us a method of calculating probabilities based on our prior knowledge and observed events. This project creates a way to sequence observations into a synchronized prediction.

## Github Repos

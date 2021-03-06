---
title: 📊 Cred
description: A metric for contribution.
---

# Cred

SourceCred, as the name might suggest, is all about attributing cred. Cred is a metric that describes every contribution and contributor in a project to give a sense of how important they were.

For example, forum posts can earn cred. If I post on the [sourcecred discourse](https://discourse.sourcecred.io/) and earn 5 cred, and another user posts and their post earns 10 cred, we can say that the other post is considered twice as important as my post.

The contributions are arranged in a [graph](https://en.wikipedia.org/wiki/Graph_(discrete_mathematics)) where contributions are nodes, and have edges indicating how they relate to other contributions. Contributors — like you or me — are also nodes in the graph, and are connected to the contributions that they create. So there is an "AUTHORS" edge connecting me (the author node) to my post node. As a more complete example, if someone writes a reply to my post, there will be a "REPLY" edge connecting that reply to my post. Edges are directional, indicating the flow of cred. For instance, when I created my post node, I got an "inbound" edge from that post, flowing cred to me. If I referenced another contributor in my post, it would create an “outbound” edge from that post to the referenced contributor.

SourceCred converts this graph into a numerical score via a modified [PageRank](https://en.wikipedia.org/wiki/PageRank) algorithm. Basically, we assign cred to the nodes such that every node receives cred from every node that connects to it. The amount of cred a node receives is the same as the amount that it sends to other nodes. This means that being connected to a high-cred node is much more valuable than being connected to a low-cred node, especially if that high-cred node isn't connected to many other nodes. In other words, cred accumulates at important nodes. For example, a core maintainer is connected to all of the posts, comments, and issues that they’ve written, so they have a lot of cred. On the other hand, a spam post on the forum may be sparsely connected, or connected to almost no other nodes, so it will have very little cred. (PageRank is a very interesting algorithm, and was actually the basis of Google search! If you want to learn more, I recommend the original [PageRank paper](http://ilpubs.stanford.edu:8090/422/1/1999-66.pdf)).

We can explore all of this in the [SourceCred explorer](https://sourcecred.io/cred/timeline/@sourcecred/). To walk through this in detail, see this [post](https://discourse.sourcecred.io/t/a-gentle-introduction-to-cred/20).

### References

 - [cred on discourse](https://discourse.sourcecred.io/t/a-gentle-introduction-to-cred/20)


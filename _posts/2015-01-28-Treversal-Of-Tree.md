---
layout: post
title: "Summary of Binary Tree Traversal"
description: "Custom written post descriptions are the way to go... if you're not lazy."
tags: [algorithm, technology]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true
share: true
---

I guess some people think that iterative version of tree traversal is tedious to implement. But I found a very interesting fact that could make it as simple as recursive version.

As a reminder, for recursive version of pre/in/post-order traversal, the only difference is the order of following three lines:
{% highlight java %}
dfs(root.left);//rec-l1
print(root);//rec-l2
dfs(root.right);//rec-;3
{% endhighlight %}

Similarly, if we take advantage of dummy node, for iterative version, the only difference is also the order of three lines:
{% highlight java %}
if(node.right!=null) stack.push(node.right);//iter-l1
stack.push(node); stack.push(null);//iter-l2
if(node.left!=null) stack.push(node.left);//iter-l3
{% endhighlight %}

You may have noticed that the above two clips of code both represent the inorder traversal. And if we follow the order of rec-l1, rec-l3, rec-l2 or iter-l2, iter-l1, iter-l3, then we could get the postorder traversal. The source code of iterative version is shown at:

- [inorder (iterative)](https://github.com/si-yao/ArtOfLeetcode/blob/master/src/binaryTreeInorderTraversal/DummyNode.java)
- [postorder (iterative)](https://github.com/si-yao/ArtOfLeetcode/blob/master/src/binaryTreePostorderTraversal/DummyNode.java)

Most interestingly, there is another property of postorder traversal. Suppose we have a tree T, and the mirror tree of T is T'. Then *postorder(T).reverse()* equals to *preorder(T')*. So, if we use two stacks, then we could solve the postorder problem more simpler! The source code is shown at: 

- [postorder (two stacks)](https://github.com/si-yao/ArtOfLeetcode/blob/master/src/binaryTreePostorderTraversal/TwoStack.java)

Both 2 solutions for postorder traversal can be extended to solve the n-ary tree postorder traversal (which could be a follow-up in a interview!). 
[[Click here and read this article in the Wiki with images|https://www.fancade.com/wiki/what_is_execution_order]]

**Execution Order** is something that determines which script is after the current one. In Fancade we follow the execution order **Top to Bottom, Left to Right** (i.e. __The way you read an English Paragraph__)

Thus, a set of scrips arranged in the following order:
```
AB
CD
```
will be executed as A→B→C→D
[[https://imgur.com/gkZWtHD.jpg]]

That's helpful, but what if you want to modify it? Here comes **Execution Wires**. Those yellow wires at the top and bottom of some scripts named *Before* and *After* are what we call as Execution Wires. Execution Wires overrides the default Execution Order.

Once a script executes according to the default execution order, __it'll execute all the scripts connected to it via Execution Wires__ before moving on the next script. A picture is worth a thousand words. So check these out:
[[https://imgur.com/e0EYbHB.jpg]]
[[https://imgur.com/qsPi1I0.jpg]]

Check out some common problems related to execution order [[here|https://www.fancade.com/wiki/what_are_some_common_problems_related_to_execution_order]]
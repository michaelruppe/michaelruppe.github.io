# Algorithms to Live By - a summary of important points

### Caching

Think about the pile of clothes next to the bed that is accessed quickly and most frequently.

**The Noguchi Filing System**: A self-organising list.
Find a file, use it, then *always* return it to the left. Don't attempt to organise or classify. Files used most frequently will be closest to the left, while less-frequently accessed will migrate across. Files to the far right can be archived or thrown away.

---

### Scheduling

Don't waste time by over-managing time. Pick an algorithm and stick to it.

 - **Earliest due date** Sort all tasks by deadlines and start from what's due earliest.
 - **Moore's Algorithm** If it's too late for *Earliest due date* because you *know* you won't make it, skit the task that takes the longest to free up as much time as possible. Repeat until you have a shot at getting everything done.
 - **Shortest processing time** Knock out the smallest first. Danger - this can lead to pre-crastination. Doing trivial and seemingly meaningless tasks.


### Overfitting

about where you can think too much on a problem and consider too many extraneous details. At the outset, the first few ideas you have are probably the most important. This is like analysis paralysis.

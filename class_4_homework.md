## Lesson 4 Homework: Command Line Chipotle

1. Look at the head and the tail of chipotle.tsv in the data subdirectory of this repo. Think for a minute about how the data is structured. What do you think each column means? What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)

  ```
  head chipotle.tsv
  tail chipotle.tsv
  ```

  * order_id - every order has an individual order id. multiple items can be in each order.
  * quantity - quantity of each item within each order.
  * item_name - name of the item
  * choice_description - item details
  * item_price - price per item

- - - -

2. How many orders do there appear to be?

```
tail chipotle.tsv
```

1,834

3. How many lines are in this file?

```
wc -l chipotle.tsv
```

4,623


4. Which burrito is more popular, steak or chicken?

```
grep 'Chicken Burrito' chipotle.tsv > chipotlechickenburrito.tsv
wc -l chipotlechickenburrito.tsv
```
553 Chicken Burritos ordered

```
grep 'Steak Burrito' chipotle.tsv > chipotlesteakburrito.tsv
wc -l chipotlestealburrito.tsv
```
360 Steak Burritos ordered

Chicken is more popular

5. Do chicken burritos more often have black beans or pinto beans?

```
grep 'Black Beans' chipotlechickenburrito.tsv > chipotleblackbean.tsv
wc -l chipotleblackbean.tsv
```
282 Chicken Burritos with Black Beans

```
grep 'Pinto Beans' chipotlechickenburrito.tsv > chipotlepintobean.tsv
wc -l chipotlepintobean.tsv
```
105 Chicken Burritos with Pinto Beans

Black beans are more popular in chicken burritos

6. Make a list of all of the CSV or TSV files in the our class repo. repo (using a single command). You will be working on your local repo on your laptop. Think about how wildcard characters can help you with this task.


7. Count the approximate number of occurrences of the word "dictionary" (regardless of case) across all files of our class repo.
8. Optional: Use the the command line to discover something "interesting" about the Chipotle data. Try using the commands from the "advanced" section!

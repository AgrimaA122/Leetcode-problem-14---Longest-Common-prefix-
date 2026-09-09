# Leetcode-problem-14---Longest-Common-prefix-
Solution for problem 14 on leetcode

## Approach

Use the **first string as the initial prefix** and compare it with each remaining string. Whenever characters don't match, shorten the prefix to the matching part.

For example:

`["flower", "flow", "flight"]`

* Start with `"flower"`
* Compare with `"flow"` → `"flow"`
* Compare `"flow"` with `"flight"` → `"fl"`
* Final prefix → `"fl"`

## Algorithm

1. Store the first string as `prefix`.
2. Compare `prefix` with every other string.
3. Compare characters one by one.
4. Stop when:

   * Characters are different, or
   * One of the strings ends.
5. Keep only the matching characters as the new `prefix`.
6. If `prefix` becomes empty, return `""`.
7. After all strings are checked, return `prefix`.

## Time Complexity

**O(n × m)**

Where:

* `n` = number of strings
* `m` = length of the shortest string

We may compare up to `m` characters for each of the `n` strings.

## Space Complexity

**O(m)**

The prefix can contain at most `m` characters.


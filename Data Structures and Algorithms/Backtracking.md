## Backtracking

If you are able to built a state space tree (requiring all possible solutions), 
Backtracking is usually the approach.

Choices, Constraints, and Goals.

### Generic approach pseudocode

```python
function backtrack(candidate): 
	if is_solution(candidate): 
		process_solution(candidate) 
	else: 
		for choice in generate_choices(candidate): 
			if is_valid(choice): 
				make_choice(choice) 
				backtrack(candidate) 
				undo_choice(choice)
```

### Problems

1. **Easy** [1863. Sum of All Subset XOR Totals](https://leetcode.com/problems/sum-of-all-subset-xor-totals/)
2. **Medium** [797. All Paths From Source to Target](https://leetcode.com/problems/all-paths-from-source-to-target/description/)
3. **Medium** [78. Subsets](https://leetcode.com/problems/subsets/description/)
4. **Medium** [46. Permutations](https://leetcode.com/problems/permutations/description/)

### Resources
- [Intro to Backtracking](https://www.youtube.com/watch?v=Nabbpl7y4Lo)

tactics: tools to prove theorems by applying them in the right order

theorem == goal

`rfl` >> proves all theorems of the form X = X
<!--LEARN:JBJToAkn-->

`rw [theorem]` 
?
rewrite. substitute inputs with outputs of theorem
- you may also chain them, e.g. `rw [theorem1, theorem2]`
- `rw [\l theorem]` to substitute the opposite way
- `repeat rw [theorem]` will rewrite all that apply in the expression
- `rw [theorem some_var]` to apply to specific var
<!--LEARN:EW0My3DC-->


# 2+2=4 example!
```lean
nth_rewrite 2 [two_eq_succ_one] -- only change the second `2` to `succ 1`.

rw [add_succ]

rw [one_eq_succ_zero]

rw [add_succ, add_zero] -- two rewrites at once

rw [← three_eq_succ_two] -- change `succ 2` to `3`

rw [← four_eq_succ_three]

rfl
```
src https://adam.math.hhu.de/#/g/leanprover-community/NNG4/world/Tutorial/level/8

---
# tips
- `... + succ ...` is normally well substituted with `rw [add_succ]`
- 

# cool 
observations
- `succ` precedes any addition function!! woaw
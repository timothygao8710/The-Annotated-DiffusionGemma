Prompt: 

```
Solve this Sudoku puzzle. 0 marks an empty cell. Reply with the completed 9x9 grid.
490673028
160805003
087001500
010400037
006908050
530160000
908014276
000709300
270580914
```

Model: 

```
495673128
162895743
387241569
819452637
726938451
534167892
958314276
641729385
273586914
```

---

## Plots

Tokens are laid out in the canvas in reading order (left to right, top to bottom).

### Entropy (canvas)

Entropy of each position's predicted token distribution at each denoising step, with the current argmax token overlaid ([mp4](canvas_00_entropy_canvas.mp4)).

![Entropy canvas](canvas_00_entropy_canvas.gif)

### Entropy (trajectories)

Entropy of each position's predicted token distribution across denoising steps.

![Entropy trajectories](canvas_00_entropy_trajectories.png)

### Step-to-step KL (canvas)

KL divergence $D_{KL}(p_t \,\|\, p_{t-1})$ at each denoising step — how much each position's distribution changed since the previous step ([mp4](canvas_00_kl_previous_canvas.mp4)).

![Step-to-step KL canvas](canvas_00_kl_previous_canvas.gif)

### KL to final (canvas)

KL divergence $D_{KL}(p_{final} \,\|\, p_t)$ at each denoising step — how far each position's distribution still is from its final one ([mp4](canvas_00_kl_final_canvas.mp4)).

![KL to final canvas](canvas_00_kl_final_canvas.gif)

### KL to final (trajectories)

KL divergence $D_{KL}(p_{final} \,\|\, p_t)$ across denoising steps.

![KL to final trajectories](canvas_00_kl_final_trajectories.png)

### Finalization (canvas)

Positions whose argmax token already matches their final token, at each denoising step ([mp4](canvas_00_finalized_canvas.mp4)).

![Finalization canvas](canvas_00_finalized_canvas.gif)

### Finalized fraction

Percentage of positions whose argmax token matches their final token, at each denoising step.

![Finalized fraction](canvas_00_finalized_fraction.png)

### Acceptance transitions

Number of positions in each accepted/unaccepted transition of the sampler's entropy-bound acceptance rule, at each denoising step.

![Acceptance transitions](canvas_00_acceptance_transitions.png)

### Position vs. finalization step

Each token's canvas position against the step where it permanently settles on its final token, pooled across all canvases with a linear regression.

![Position vs. finalization step](all_canvases_position_finalization_regression.png)
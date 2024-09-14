#concept-pamphlet #paper [Paper](https://arxiv.org/pdf/2310.06770) [Cognition's technical report](https://www.cognition.ai/blog/swe-bench-technical-report) [OpenReview](https://openreview.net/forum?id=VTF8yNQM66)

Roughly how many issues and pull requests are in SWE-bench?
?
2,294 issues and pull requests
<!--SR:!2024-10-11,81,252-->

In SWE-bench, what was the original number of PRs that were then filtered down?
?
90,000 PRs with corresponding issues
<!--SR:!2024-10-17,87,270-->

In SWE-bench, what is the difference between "assisted" and "unassisted" tasks?
?
In SWE-bench, LLMs are either given the set of correct files to edit (“assisted”); or a separate system retrieves the files to edit based on similarity to the issue text (“unassisted”).
<!--SR:!2024-10-23,93,250-->


In SWE-bench, what is the model input?
?
issue text description and complete codebase
<!--SR:!2024-09-10,50,230-->

In SWE-bench, what does the high-level process look like to evaluate a generated patch?
?
To evaluate a proposed solution, we apply the generated patch, using unix’s patch program, to the codebase and then execute the unit and system tests associated with the task instance. If the patch applies successfully and all of these tests pass we consider the proposed solution to have successfully resolved the issue. The metric for our benchmark is the percentage of task instances that are resolved. (3)
More granularly, the following steps are performed per prediction on the target task instance:
1. Remove any file changes and checkout the task instance’s base commit. This sets the repository to codebase C.
2. Activate the executable context corresponding to the task instance’s version.
3. Run installation command to instantiate codebase C.
4. Apply test patch T to codebase C.
5. Apply prediction patch ˆδ to codebase C with tests T.
6. If the previous step fails, we attempt to fix prediction patch ˆδ automatically and reapply it.
7. Run the testing script, determined from test patch T, to generate test result logs logδˆ.
Steps 1 through 4 reliably do not fail due to verification during the task instance validation process. If applying the prediction patch (Step 5) fails, we attempt to repair the prediction patch file by removing unnecessary context lines and recalculating the header values (Step 6). If the remaining patch fails again or running the test command (Step 7) fails, then the prediction is automatically given a score of 0. Assuming these steps succeed, the output log logδˆ can then be converted to a test-to-status mapping, identical in structure to the via the appropriate, repository-specific parser introduced in § A.3. (21)
<!--SR:!2024-10-08,41,210-->


In SWE-bench tasks, what's the median number of words for a problem description?::140 words
<!--SR:!2024-06-01,3,250-->

In SWE-bench repositories, what's the median number of files and lines for a repository?::1900 files and 400k lines
<!--SR:!2024-05-30,1,230-->

In SWE-bench, what is FAIL_TO_PASS and PASS_TO_PASS?
?
They are both keys to indicate quality of a code edit.
-  FAIL_TO_PASS: a test previously that was failing now passes, given the gold patch
- PASS_TO_PASS: a test previously that was passing is still passing
<!--SR:!2024-10-27,97,290-->

What are some weaknesses of the SWE-bench paper?
?
- Generating a patch file, and generating code, are two very different tasks. Existing models are pretrained on code, not patch files, so at least some of the poor performance could simply be due to the fact that the models are operating out of distribution on this data set. (The authors mention this issue in the paper.)
- SWE-bench is a cool benchmark with evaluations but doesn't provide a novel solution to itself. SWE-llama is not super novel.
- Data contamination given that the dataset is public
<!--SR:!2024-12-18,112,230-->
# learning notes

### Summary 

![[Screenshot 2024-05-22 at 10.54.36 AM.png]]

Prompt used: 
```
You will be provided with a partial code base and an issue statement explaining a problem to resolve. 

<issue>
{ISSUE TEXT} 
</issue>

<code> 
[start of README.md] 
{README.md text} 
[end of README.md] 
[start of file_1.py] 
{file_1.py text} 
[end of file_1.py] 
...
</code>

Here is an example of a patch file. It consists of changes to the code base. It specifies the file names, the line numbers of each change, and the removed and added lines. A single patch file can contain changes to multiple files. 

<patch>
--- a/file.py 
+++ b/file.py 
@@ -1,27 +1,35 @@ 
def euclidean(a, b): 
- while b: 
-   a, b = b, a % b 
- return a 
+ if b == 0: 
+   return a 
+ return euclidean(b, a % b) 

def bresenham(x0, y0, x1, y1): 
  points = [] 
  dx = abs(x1 - x0) 
  dy = abs(y1 - y0) 
- sx = 1 if x0 < x1 else -1 
- sy = 1 if y0 < y1 else -1 
- err = dx - dy 
+ x, y = x0, y0 
+ sx = -1 if x0 > x1 else 1 
+ sy = -1 if y0 > y1 else 1

...
return points 

</patch>

I need you to solve the provded issue by generating a single patch file that I can apply directly to this repository using git apply. Please respond with a single patch file in the format shown above. 

Respond below:
```

- Model Generated Patch
- Gold Patch
## Related materials
[Cognition Devin's run on it](https://www.cognition.ai/blog/swe-bench-technical-report)
https://github.com/CognitionAI/devin-swebench-results
[[Devin swe-bench results 2024]]
[[EvalAI -Towards Better Evaluation Systems for AI Agents]]


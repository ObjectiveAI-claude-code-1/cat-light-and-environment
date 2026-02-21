# cat-light-and-environment

Evaluates how well the light and surrounding environment in a cat photograph serve the cat as a subject. Given a single image of a cat, this scalar function produces a score between 0 and 1 reflecting whether the photograph's visual world cooperates to let the cat be seen clearly and appreciated fully.

This function rewards **service over spectacle**. A humble kitchen counter with soft window light and a plain wall behind the cat will outscore a stunning botanical garden where dappled light creates confusing shadows across the cat's face and overlapping foliage clutters the background. What matters is not the beauty or prestige of the setting, but whether light and environment work together to let the viewer's eye settle on the cat with ease and comfort.

## Input

| Type | Description |
|------|-------------|
| `image` | A cat photograph to evaluate for light and environment — whether the lighting reveals the cat effectively and the background supports the subject without distraction. |

The function accepts cat photographs as they exist in the real world — taken on kitchen counters, in cardboard boxes, on windowsills, in gardens, on beds, under tables, and in every other setting that no one designed with photography in mind. The light may come from a window, a lamp, an overcast sky, or the midday sun. The background may be a plain wall or a tangle of household objects. This variety is the reality to be evaluated, not a problem to be solved.

## Output

A **scalar value between 0 and 1**, where:

- **Scores near 1.0** indicate the lighting effectively reveals the cat, the background is calm and non-distracting, and the overall setting feels harmonious and inviting.
- **Scores near 0.0** indicate the lighting fails the subject (overexposed, underexposed, harsh contrast, or unnatural color casts), the background competes with the cat for attention, or the visual elements clash rather than cooperate.

The final score is a weighted average across three sub-function evaluations, each assessing a distinct dimension of the visual stage.

## What It Evaluates

### 1. Lighting Effectiveness on the Subject
Does the light let the viewer see the cat? This sub-function scores whether the cat's key features — face, eyes, fur texture, color, and body form — are visible and legible. It penalizes overexposure that washes out detail, underexposure that buries the cat in shadow, extreme contrast that fractures the subject, and unnatural color casts that distort appearance. It rewards any light source — humble or dramatic — that functionally reveals the cat.

- Sub-function: [cat-subject-lighting-score](https://github.com/ObjectiveAI-claude-code-1/cat-subject-lighting-score)

### 2. Background Cleanliness and Distraction Level
Does the viewer's eye go to the cat, or does it wander? This sub-function scores whether the visual territory behind and around the cat is calm enough to let the subject stand out. A background does not need to be empty or blurred — it simply needs to not compete. It penalizes visually noisy, cluttered, or chaotic backgrounds and rewards settings where the cat is the clear focal point, regardless of location.

- Sub-function: [cat-background-calm-score](https://github.com/ObjectiveAI-claude-code-1/cat-background-calm-score)

### 3. Overall Harmony Between Subject and Setting
Does the photograph feel like a place where a cat can be seen and appreciated? This sub-function is the most holistic evaluation. It steps back from individual dimensions and scores whether light and environment work *together* to create a coherent, inviting visual experience. It captures the emergent quality that arises when elements cooperate — or the tension when they conflict. A photograph where both lighting and background are merely adequate but work in concert should outscore one where a single dimension excels while the other undermines it.

- Sub-function: [cat-setting-harmony](https://github.com/ObjectiveAI-claude-code-1/cat-setting-harmony)

## Use Cases

- **Pet adoption listings** — Shelter volunteers choosing among multiple photos of an adoptable cat can identify which image presents the animal most clearly and invitingly, increasing the likelihood of adoption.
- **Social media curation** — Anyone selecting cat photos for a feed or post can filter for images where the visual conditions support the subject, ensuring a more polished and engaging presentation.
- **Photography review** — Cat photographers reviewing their own work can understand which shots succeeded because the light and environment cooperated, independent of the cat's pose or expression.
- **Personal collection management** — Cat owners sorting through hundreds of photos can surface the ones where their cat is most clearly and beautifully presented by its surroundings.
- **Automated quality filtering** — Platforms or applications processing large volumes of cat imagery can use the score to programmatically rank or filter photos by visual presentation quality.

## Philosophy

Every photograph is a small stage. The purpose of `cat-light-and-environment` is to evaluate whether that stage serves its performer. Light should reveal. Background should recede. The overall environment should create a sense of quiet welcome. This function does not chase prestige or spectacle — it asks only whether the visual world is willing to step aside and let the cat be seen.
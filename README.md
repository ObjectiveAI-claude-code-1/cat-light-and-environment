# cat-light-and-environment

Evaluates the light and environment of a cat photograph, scoring how well the visual stage serves the cat as subject. This function answers a fundamental question about any cat photograph: does the visual world of the image let the viewer see and appreciate the cat clearly, or do lighting failures and environmental distractions get in the way?

## Input

The function accepts a single input: a **cat photograph** (image). The image is evaluated as a complete visual experience — no metadata, camera settings, or contextual information is required. Everything the function needs is present within the photograph itself: the light as it falls across the cat, the environment surrounding the cat, and the relationship between these elements.

The photograph may come from any source — a professional portrait, a phone snapshot, an outdoor scene, or an indoor candid. The function does not privilege any particular type of setting or equipment.

## Output

A **scalar score between 0 and 1**.

- **High scores (near 1.0)** indicate that light and environment work together generously to present the cat. The lighting reveals the subject clearly, the background stays calm and subordinate, and the overall image feels harmonious and inviting.
- **Low scores (near 0.0)** indicate that light and environment fail the subject. The cat may be lost in shadow, blown out by overexposure, competing with a cluttered background for attention, or caught in a visually disjointed scene.

The final score is a weighted average of the three sub-function evaluations described below.

## What It Evaluates

The function decomposes the evaluation into three distinct dimensions of the visual stage, each handled by a dedicated sub-function:

### 1. Lighting Effectiveness on the Subject
[{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

Examines how the light falls on the cat and whether it reveals or obscures the cat's features, texture, and form. Considers visibility of the face and eyes, detail in the fur, and dimensionality of the body. Penalizes deep shadows that swallow the subject, harsh overexposure that washes out detail, extreme backlighting that creates silhouettes, and unnatural color casts. The standard is functional lighting — not studio perfection, but light that does its job of making the cat visible and comfortable to look at.

### 2. Background Cleanliness and Distraction Level
[{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

Examines the space surrounding the cat and whether it remains visually subordinate to the subject. A clean background is not necessarily empty — it is one that occupies space without demanding attention. Penalizes cluttered surfaces, busy scenes with competing visual elements, and aggressive patterns that merge with the cat's form. The evaluation measures degree, not perfection: a moderately busy background where the cat still reads clearly as subject is acceptable; a chaotic background where the cat disappears into visual noise is a failure.

### 3. Overall Harmony Between Cat and Environment
[{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

Steps back from individual assessments to examine the photograph as a unified visual experience. Evaluates whether light and environment come together to create a coherent, settled feeling — whether colors complement rather than clash, the mood feels consistent rather than contradictory, and the cat looks like it belongs in its space. Identifies disharmony from mismatched tones, overwhelming color palettes, or fragmented visual registers where different elements seem to belong to different photographs.

## Use-Cases

- **Quality scoring and ranking**: Provides a baseline measurement of whether a cat photograph's visual stage supports its subject, before higher-level questions of composition or artistic merit are considered.
- **Photographer feedback**: Isolates light and environment as a specific, actionable dimension of improvement — helping photographers understand whether their lighting reveals or obscures, and whether their chosen background supports or competes.
- **Curation and filtering**: Acts as a filter for selecting photographs that feel inviting and clear, surfacing images where the cat is presented in a visually generous setting.

## Philosophy

This function evaluates generosity. It asks whether the photograph's visual world is generous to its subject — whether light and environment give the cat the conditions it needs to be seen, appreciated, and enjoyed. A humble kitchen with soft window light can score beautifully. A pristine garden with dappled light creating confusing patterns across the cat's face can score poorly. What matters is not the beauty or prestige of the setting, but whether light and setting work together to let the cat be seen clearly and appreciated fully.
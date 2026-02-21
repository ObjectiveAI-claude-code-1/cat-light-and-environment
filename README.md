# cat-light-and-environment

Evaluates whether the lighting and environment in a cat photograph work together to support the cat as the subject. Every cat photo is a small stage — the cat is the performer, and the light and space around it determine whether the audience can truly see the performance. This function scores that stage.

## How It Works

`cat-light-and-environment` is a **scalar function**. It receives a single cat photograph as input and returns a score between 0 and 1, where higher values indicate that the light and environment more effectively serve the cat as a subject.

The final score is a weighted combination of three sub-function evaluations, each examining a distinct dimension of the photograph's visual stage.

## Input

| Field | Type | Description |
|-------|------|-------------|
| input | `image` | A cat photograph to evaluate for light and environment — whether the lighting reveals the cat effectively and the background supports the subject without distraction. |

## Output

A scalar value between **0** and **1**.

- **Scores near 1.0** — The cat is clearly visible, the background is calm and supportive, and the entire image feels unified. Light and environment work together to present the cat.
- **Scores near 0.5** — Light or environment partially support the cat but with notable issues — perhaps the lighting is adequate but the background is cluttered, or the background is clean but the cat is partially lost in shadow.
- **Scores near 0.0** — The cat is obscured by poor lighting, overwhelmed by a chaotic background, or the visual elements clash so strongly that the image feels incoherent.

## What It Evaluates

The function decomposes the evaluation into three qualities that move from the specific to the holistic:

### 1. Lighting Effectiveness on the Subject
[`{{ .Task0 }}`](https://github.com/{{ .Owner }}/{{ .Task0 }})

Can you **see** the cat? This sub-function evaluates whether the light — regardless of source or style — reveals the cat's features clearly. It looks for legible fur texture, visible facial structure, eye depth, and body contour. It penalizes harsh overexposure that washes out detail, deep shadows that absorb the cat into darkness, unnatural color casts, and glare or hot spots that pull focus. A humble kitchen light that evenly illuminates the cat scores well. A dramatic sunset that turns the cat into a silhouette does not. Effectiveness is measured by visibility and clarity, not beauty or mood.

### 2. Background Cleanliness and Distraction Level
[`{{ .Task1 }}`](https://github.com/{{ .Owner }}/{{ .Task1 }})

Will you **look at** the cat? This sub-function evaluates whether the non-subject elements in the photograph recede to let the cat command attention or compete with it. A clean background is not necessarily empty — a couch with a few pillows or a garden with soft greenery can be perfectly clean. What matters is whether visual noise fragments the viewer's attention: cluttered objects, competing colors, busy patterns, text on packaging, other animals partially in frame, or bright elements that rival the cat. The question is whether the space acts as a supportive setting or a rival subject.

### 3. Overall Harmony Between Cat and Environment
[`{{ .Task2 }}`](https://github.com/{{ .Owner }}/{{ .Task2 }})

Does the cat **belong** in this visual world? This sub-function captures the holistic unity of the image — something neither lighting nor background can express alone. It evaluates whether light, space, color, and subject participate in one coherent image rather than existing in tension. A cat curled on a warm blanket in soft lamplight feels harmonious. A cat lit by harsh flash in an otherwise dark room feels jarring. This quality rewards coherence: the quiet agreement between all parts of the image that everything exists to let the viewer see the cat.

## Use Cases

- **Photo curation** — Select the strongest images from a batch of cat photos for social media, publications, or personal collections based on environmental and lighting quality.
- **Pet adoption listings** — Surface the most visually clear and inviting photos of shelter cats, where good light and a calm background can make the difference in catching an adopter's eye.
- **Photographer feedback** — Understand whether the light and setting in an image worked for or against the subject, applicable to amateurs and experienced photographers alike.
- **Automated ranking** — Sort or filter large collections of cat photographs by how well each image's environment supports the subject.

## Philosophy

This function does not chase beauty or prestige. It chases **clarity, calm, and coherence**. A cat on a simple concrete step in even daylight with a plain wall behind it can score higher than a cat in an extravagant room with chandelier lighting, if the humble setting better reveals and supports the subject. What matters is whether light and environment work together to let the cat be seen clearly and appreciated fully.
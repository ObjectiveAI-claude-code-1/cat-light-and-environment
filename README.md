# cat-light-and-environment

Scores how well a cat photograph's lighting and environment support the cat as the subject. Evaluates lighting effectiveness, background cleanliness, and overall harmony between subject and space. Prioritizes functional clarity over aesthetic prestige — good light and a quiet background outscore a stunning but visually noisy setting.

## Input

The function accepts a single **image** — a cat photograph to evaluate for light and environment.

The photograph can come from any source or context: a studio portrait, a casual phone snapshot, an outdoor scene in a garden or on a street. The function makes no assumptions about equipment, intent, or setting. It meets the photograph wherever it is and evaluates one thing: whether the visual world of the image serves the cat as a subject.

## Output

A **scalar score between 0 and 1**.

- **Scores near 1.0** indicate that the lighting clearly reveals the cat, the background is calm and non-distracting, and the overall scene feels coherent and inviting around the subject.
- **Scores near 0.0** indicate that the cat is lost — swallowed by darkness, bleached by overexposure, buried in visual clutter, or placed in an environment that feels hostile or disjointed.
- **Mid-range scores** reflect photographs where some dimensions work well but others fall short — for example, good lighting but a distracting background, or a clean background but poor lighting on the subject.

## What It Evaluates

The function evaluates three distinct dimensions of the visual stage that a photograph creates for its feline subject:

### 1. Lighting Effectiveness on the Subject

> Sub-function: [cat-light-revelation](https://github.com/ObjectiveAI-claude-code-1/cat-light-revelation)

Does the light reveal the cat? This dimension assesses whether the cat's form, features, and texture — fur, ears, eyes, body contour — are clearly visible and legible to the viewer. The standard is *functional revelation*: the light does not need to be perfect or dramatic, but it must do enough work that the viewer can perceive the cat without effort or strain.

**Scores well:** Soft window light illuminating a cat's face. Even, diffused afternoon light. A slightly dim room where the cat is still clearly discernible.

**Scores poorly:** Harsh shadows fragmenting the cat's features. Overexposure washing out light-colored fur. Underexposure burying the cat in darkness. Backlighting reducing the cat to a silhouette.

### 2. Background Cleanliness and Distraction Level

> Sub-function: [rate-cat-photo-background](https://github.com/ObjectiveAI-claude-code-1/rate-cat-photo-background)

Does the background defer to the cat? This dimension shifts attention to everything in the photograph that is *not* the cat and assesses whether the surrounding environment recedes gracefully behind the subject or surges forward to compete with it. A clean background is not necessarily empty — it simply must not fragment the viewer's attention.

**Scores well:** Muted cushions behind a cat on a couch. A softly blurred garden. A simple wall or floor that stays quiet and subordinate.

**Scores poorly:** Visual clutter from scattered objects. Competing focal points like screens, bright signage, or other animals. Chaotic environments where the cat must fight for attention.

### 3. Overall Harmony Between Cat and Environment

> Sub-function: [cat-scene-harmony](https://github.com/ObjectiveAI-claude-code-1/cat-scene-harmony)

Does the photograph feel like a coherent, unified scene? This holistic dimension captures what the first two cannot capture alone — the *feeling* of the photograph as a whole. It evaluates whether light, textures, colors, and spatial relationships converge to make the cat feel naturally at home in its setting, or whether the scene feels disjointed despite its individual parts being adequate.

**Scores well:** A cat on a sun-warmed windowsill where warm light, soft textures, and a quiet background all breathe together. A cat on a bed where color palette, lighting warmth, and spatial composition create a gentle mood.

**Scores poorly:** A technically visible cat against a technically clean background where the color temperature clashes, the spatial relationship feels awkward, or the mood is fractured. Environments that feel hostile or incoherent around the subject.

## Use Cases

- **Cat photo quality systems** — Use as one dimension in a composite scoring system that also evaluates pose, expression, sharpness, and emotional appeal.
- **Photo curation and ranking** — Surface the best cat photos on social media platforms, community galleries, or content feeds by filtering for images where the subject is clearly presented.
- **Pet adoption services** — Select the most effective profile photo for a shelter cat by identifying which snapshot actually lets a potential adopter see the animal.
- **Photography feedback** — Help photographers understand when a beautiful cat has been lost in a chaotic background or drowned in shadow.

## Philosophy

This function is a measure of *visual hospitality*. It asks whether the photograph has given its cat the one thing every subject deserves: a stage that supports it. A humble photograph taken in a modest room with good light and a quiet background embodies everything this function values. A spectacular photograph taken in a stunning location that overwhelms its subject with visual noise embodies everything this function cautions against.

The light must serve the cat. The environment must respect the cat. And together, they must create a space where the viewer can simply, peacefully, *see* the cat.
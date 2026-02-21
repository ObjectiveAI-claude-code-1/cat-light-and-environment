# cat-light-and-environment

A scalar function that evaluates the light and environment of a cat photograph. It scores how well the lighting reveals the cat and how effectively the background and surrounding space support the subject rather than competing with it. Light and environment together determine whether the photograph feels harmonious and inviting or chaotic and confusing.

This function is not a judgment of photographic artistry or the beauty of a setting. It asks a more fundamental question: can the viewer see the cat clearly, and does the surrounding scene let them appreciate it without struggle or distraction? A casual snapshot on a kitchen floor under soft afternoon light can score beautifully, while a photograph taken in a stunning location where visual noise overwhelms the subject can score poorly. What matters is whether light and setting work together to let the cat be seen and appreciated.

## Input

The function accepts a single **image** input: a photograph containing a cat.

The photograph may come from any source — a phone camera, a professional shoot, or a candid moment captured in passing. The function makes no assumptions about the setting, equipment, or intent behind the image. It meets each photograph on its own terms and evaluates only whether the visual conditions within that specific image serve the cat well.

## Output

The function returns a **scalar score between 0 and 1**, where higher values indicate that the lighting and environment more effectively support the cat as a subject. The score is a weighted average of three sub-evaluations, each assessing a distinct dimension of the photograph's visual stage.

## What It Evaluates

The score rests on three essential qualities. Each examines a different dimension of the visual stage, and together they capture the full relationship between the cat, the light, and the space.

### 1. Lighting Effectiveness on the Subject

[{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

Evaluates how effectively the lighting reveals the cat. Scores how well the light allows the viewer to clearly see the cat's face, fur texture, and body form without straining. Penalizes harsh overexposure that washes out detail, deep shadows that swallow the cat into darkness, and distracting artifacts like extreme glare or unnatural color casts. The standard is functional lighting — light that works for the cat by making it visible and appreciable. Studio-perfect lighting is not required; soft window light, overcast sky glow, or warm ambient room light all qualify as effective if they reveal the cat clearly.

### 2. Background Cleanliness and Distraction Level

[{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

Evaluates how clean and non-distracting the background and surrounding space are in relation to the cat. Scores whether the cat stands out clearly as the subject or is lost in a visual crowd of competing elements. Penalizes scattered objects, bold patterns, bright signage, other animals, or a general tangle of visual information that fractures the viewer's focus. The background does not need to be empty or sterile — a bookshelf, a garden, or a kitchen counter can serve well — but it must remain visually secondary to the cat, respecting the subject's role as the center of attention.

### 3. Overall Harmony Between Subject and Setting

[{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

Evaluates the overall harmony between the cat, the light, and the surrounding environment as a unified visual experience. Scores whether the photograph feels settled, coherent, and inviting as a whole — whether the cat appears to exist comfortably within its visual world. Penalizes jarring mismatches between the subject and its setting, such as a warmly colored cat under cold and clinical light, or a calm subject in a visually chaotic space. Harmony does not require beauty or prestige — a humble room with consistent gentle light can radiate harmony — but it requires that the visual elements feel unified in their service to the cat.

## Use Cases

- **Content curation**: Surface cat photographs where cats are clearly visible and pleasantly situated, ensuring viewers enjoy what they see rather than struggling to parse cluttered or poorly lit scenes.
- **Photography workflow**: Use as a first-pass filter when reviewing a batch of cat photos, identifying which images have the strongest visual foundation before investing time in further editing.
- **Recommendation systems**: Weight alongside other quality dimensions — such as sharpness, composition, or the cat's expressiveness — to rank photographs by overall appeal.
- **Composable evaluation**: Combine with other cat photograph functions to build a richer, multi-dimensional assessment of photograph quality. This function isolates light and environment as a distinct dimension, making it a natural building block in larger evaluation pipelines.

## Scoring Philosophy

A simple kitchen counter with soft window light can score beautifully. A pristine garden with dappled light creating confusing patterns across the cat's face can score poorly. The evaluation rewards visual hospitality — the degree to which a photograph's light and environment work together to let the cat be the clear, comfortable, and visible subject of the image. A humble, imperfect environment with good light and a clean background should always outscore a stunning location where visual noise overwhelms the subject.
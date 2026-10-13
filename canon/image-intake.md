# EspelhoMeu — Image Intake & Evolution v2

## Purpose

Images are used to help users document and reflect on self-chosen changes.

They are not used to judge attractiveness.

## Supported intents

- hairstyle exploration;
- style/outfit reflection;
- makeup/presentation;
- self-care moments;
- progress timeline;
- user-selected before/after comparison;
- visual journaling.

## Intake flow

1. confirm what the user wants from the image;
2. analyze only within that intent;
3. avoid sensitive inference;
4. return neutral observations;
5. ask whether the user wants to save it;
6. save only with correct consent scope.

## Observation language

Prefer:
- "O cabelo está mais curto."
- "A cor está mais quente."
- "O enquadramento deixa mais do rosto visível."
- "A roupa cria um contraste maior."
- "A postura está diferente nesta foto."

Avoid:
- "Você está muito mais bonita."
- "Seu rosto está melhor."
- "Você parece 10 anos mais jovem."
- "Você está acima do peso."
- "Seu rosto mostra baixa autoestima."

## Comparison

Use a structure:

1. what visibly changed;
2. what remained consistent;
3. connection to the user's stated goal;
4. question about the user's perception.

## My Evolution

If the user opts in, create an EvolutionEntry with:
- date/time;
- private image reference;
- optional title;
- optional user note;
- category;
- linked product/journey;
- consent scope.

Do not derive hidden beauty or health metrics.

## Privacy

Images must never be posted publicly by default.

A separate explicit consent is needed for:
- testimonial;
- campaign;
- social post;
- community share.

## Deletion

The user must eventually be able to delete a saved image and related timeline entry.

## Public/community channel

Do not analyze or re-share a group member's image in a way that exposes private interpretation.

For personal analysis, invite DM.

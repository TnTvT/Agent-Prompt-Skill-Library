# Print-friendly visual modifier

Use only when `print_friendly: true`. Append the resolved instructions below to the base prompt. This mode guides the image toward easier subsequent modeling; it does not generate or certify printable geometry.

```text
Adapt the woven design as a visual reference for later 3D modeling:
- Use broader, visually substantial strips and compact connected intersections.
- Remove hairlike fibers, splinters, loose ends, and isolated decorative strips.
- Reduce tiny gaps and deep narrow crevices. Prefer shallow woven relief on visually continuous surfaces where practical, retaining readable over-under construction.
- Make rims, handles, loops, and projecting details appear securely joined to the body. Keep genuine functional openings recognizable.
- Simplify dense micro-weave in small features while preserving their outline, placement, expression, and color contrast.
- Preserve the original silhouette and proportions. Do not add a pedestal, supports, or new components unless requested.
Keep the result recognizably woven bamboo. Do not flatten it into an engraved grid or erase the construction to make it appear solid.
```

## Resolve competing settings

- `fine` density: retain the impression of fine weaving, but group or broaden the smallest strands. State any visible simplification.
- `hexagonal`: use fewer, larger openings and more substantial junctions where the geometry permits. Do not close a user-required open lattice without discussing the tradeoff.
- `random`: use controlled connected crossings; remove stray strands rather than producing a nest of disconnected fibers.
- If preserving a very thin source feature conflicts with simplification, keep its identifying outline and explain the limitation. Ask only when a material design choice is needed.

## Review

Look for visibly connected elements, no floating ends, fewer micro-holes, and readable identifying details. Do not infer hidden connections or numerical wall thickness from the image. Real minimum feature sizes require known scale, process, material, and a 3D model; never invent millimeter values or claim that this image passes slicing or strength checks.

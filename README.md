# Hideki Yukawa — GA3 model

Student-provided Meshy reconstruction, optimized for the TDS September2026 GA3 Q6 submission.

- Direct submission asset: `yukawa.glb`.
- Size: 1,874,520 bytes (limit:2,000,000).
- 35,583 vertices / 43,196 triangles; embedded1536x1536 JPEG texture.
- glTF2.0, no required compression extensions, no external textures or buffers.
- glTF Validator:0errors,0warnings (one informational non-power-of-two texture notice).
- SHA256:af9117493c7f21c7608b5aae7210473785069b4bffa55406b4813330aa48e052.

The original72,788,140-byte model remains on the student's computer and is not included here.
Optimization is lossy. Geometry and texture were reduced while retaining the supplied model's structure and appearance; grading likeness is determined separately by the course.

Reference photograph supplied by the assignment: https://upload.wikimedia.org/wikipedia/commons/7/7b/Yukawa.jpg .

## Reproduce

With Node.js and glTF Transform CLI4.5.1:

```powershell
npx --yes --package=@gltf-transform/cli@4.5.1 gltf-transform optimize INPUT.glb yukawa.glb --compress false --simplify-ratio 0.018 --simplify-error 0.002 --texture-size 1536
```

Use spaces between the option names and values (`--simplify-ratio 0.018`, `--simplify-error 0.002`, `--texture-size 1536`).


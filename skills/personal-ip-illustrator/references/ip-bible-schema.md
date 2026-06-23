# IP Bible Schema

Use this structure after the user selects a candidate or provides a reference image. The IP Bible is the generation contract for future illustrations.

The user should not have to read the full IP Bible. Show the user a short IP Card first, then keep the full IP Bible as the internal consistency contract.

## Required Fields

```json
{
  "ip_name": "",
  "version": "1.0",
  "entity_type": "human | animal | robot | object | symbol | abstract_creature | fictional_species",
  "core_identity": "",
  "content_role": "",
  "silhouette": "",
  "face_or_front": "",
  "body_or_structure": "",
  "clothing_or_surface": "",
  "signature_objects": [],
  "palette": {
    "primary": [],
    "accent": [],
    "background": [],
    "forbidden": []
  },
  "style_rules": {
    "rendering": "",
    "shape_language": "",
    "texture": "",
    "composition": "",
    "typography": ""
  },
  "personality": "",
  "allowed_expressions": [],
  "allowed_actions": [],
  "default_roles_in_illustrations": [],
  "forbidden_variations": [],
  "consistency_prompt_block": "",
  "negative_prompt_block": "",
  "usage_notes": ""
}
```

## Field Guidance

- **core_identity**: what the IP represents, not just how it looks.
- **content_role**: why this IP belongs in the creator's articles.
- **silhouette**: the highest-priority recognition feature.
- **signature_objects**: only include objects that can recur without clutter.
- **forbidden_variations**: include drift risks such as changing species, age, proportions, color, clothing, or emotional tone.
- **consistency_prompt_block**: write a reusable paragraph that can be pasted into every image prompt.
- **negative_prompt_block**: list exclusions that protect the IP and style.

## Consistency Rules

- Preserve species, silhouette, palette, and signature objects across all prompts.
- Let pose, camera angle, prop scale, and scene vary.
- Do not make the IP a copy of a real person unless the user explicitly owns that likeness and asks for it.
- Do not rely on a single reference image. Convert the image into stable verbal rules.

## Minimal IP Bible

When the user wants a fast draft, return these fields first:

- `ip_name`
- `entity_type`
- `core_identity`
- `silhouette`
- `palette`
- `style_rules`
- `signature_objects`
- `forbidden_variations`
- `consistency_prompt_block`

## User Confirmation Rule

Confirm with images and the short IP Card. Do not ask the user to approve raw JSON or a long technical description unless the user asks to inspect it.

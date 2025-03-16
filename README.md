## Hi there 👋

<!--
**maro666-space/maro666-space** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->import bpy

# Usuń domyślny sześcian
bpy.ops.object.select_all(action='SELECT')
bpy.ops.object.delete(use_global=False)

# Dodaj tułów (sfera)
bpy.ops.mesh.primitive_uv_sphere_add(radius=1, location=(0, 0, 1))

# Dodaj głowę (sfera)
bpy.ops.mesh.primitive_uv_sphere_add(radius=0.5, location=(0, 0, 2.5))

# Przykładowe skalowanie i przemieszczanie
bpy.ops.transform.resize(value=(0.8, 0.8, 1.2))
bpy.ops.transform.translate(value=(0, 0, 0.2))

# Dodaj modyfikator Subdivision Surface
bpy.ops.object.modifier_add(type='SUBSURF')
bpy.context.object.modifiers["Subdivision"].levels = 2


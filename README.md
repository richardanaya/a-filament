# pbr-scene

A simple web component for using [filament](https://github.com/google/filament/) easily.

# Before you start

Google created a really awesome physically based rendering library with a catch that you have to convert your meshes and define materials to its `.filamesh` and `.filamat` formats. So don't be confused if you see these file formats you don't recognize. They are just generated from the tools `filamesh` and `matc` you can download here https://github.com/google/filament/releases.

If you need a material shader file, just use the default `pbr.mat`, or learn how to invent your own at https://google.github.io/filament/Materials.md.html

# Hello cube

The most basic cube with no material.

![no material cube](cube.png)

```html
<script src="https://cdn.jsdelivr.net/npm/filament@1.1.0/filament.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gl-matrix/2.8.1/gl-matrix-min.js"></script>
<script src="../../pbr-scene.js"></script>
<pbr-scene width="500" height="500">
  <pbr-asset name="c_mesh" src="cube.filamesh"></pbr-asset>
  <pbr-camera></pbr-camera>
  <pbr-model mesh="c_mesh"></pbr-model>
</pbr-scene>
```

See live [demo](https://richardanaya.github.io/pbr-scene/examples/cube/index.html)

# Suzanne

![pbr rendered suzanne](suzanne.png)

```html
<script src="https://cdn.jsdelivr.net/npm/filament@1.1.0/filament.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gl-matrix/2.8.1/gl-matrix-min.js"></script>
<script src="https://unpkg.com/pbr-scene@latest/pbr-scene.js"></script>
<pbr-scene width="500" height="500">
  <pbr-asset name="sz_mat" src="assets/textured.filamat"></pbr-asset>
  <pbr-asset name="sz_mesh" src="assets/suzanne.filamesh"></pbr-asset>
  <pbr-asset name="sz_alb" src="assets/albedo_s3tc.ktx"></pbr-asset>
  <pbr-asset name="sz_ao" src="assets/ao_etc.ktx"></pbr-asset>
  <pbr-asset name="sz_mtl" src="assets/metallic_etc.ktx"></pbr-asset>
  <pbr-asset name="sz_nrm" src="assets/normal_etc.ktx"></pbr-asset>
  <pbr-asset name="sz_rgh" src="assets/roughness_etc.ktx"></pbr-asset>
  <pbr-asset name="env_indirect" src="assets/syferfontein_18d_clear_2k/syferfontein_18d_clear_2k_ibl_s3tc.ktx"></pbr-asset>
  <pbr-asset name="env_sky" src="assets/syferfontein_18d_clear_2k/syferfontein_18d_clear_2k_skybox.ktx"></pbr-asset>
  <pbr-sun></pbr-sun>
  <pbr-environment indirect-map="env_indirect" sky-map="env_sky"></pbr-environment>
  <pbr-camera></pbr-camera>
  <pbr-model material="sz_mat" mesh="sz_mesh" albedo="sz_alb" roughness="sz_rgh" normal="sz_nrm" metallic="sz_mtl" ao="sz_ao"></pbr-model>
</pbr-scene>
```

See live [demo](https://richardanaya.github.io/pbr-scene/examples/suzanne/index.html)

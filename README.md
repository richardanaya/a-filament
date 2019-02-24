# pbr-scene

A simple web component for using [filament](https://github.com/google/filament/) easily.

```html
<script src="https://cdn.jsdelivr.net/npm/filament@1.1.0/filament.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gl-matrix/2.8.1/gl-matrix-min.js"></script>
<script src="../../pbr-scene.js"></script>
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
  <pbr-model material="sz_mat" mesh="sz_mesh" albedo="sz_alb" roughness="sz_rgh" normal="sz_nrm" metallic="sz_mtl" ao="sz_ao"[></pbr-model>
</pbr-scene>

```
 

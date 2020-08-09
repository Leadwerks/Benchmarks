# Benchmarks #

Comparative performance benchmarks for testing Ultra Engine against Unity3D. Framerate and GPU utilization are measured. All tests are performed with an Nvidia GEForce 2060.

## Shadows ##

This test evaluates the update and render speed of point lights. The moving objects in the scene are designed to trigger a redraw on every point light, and to demonstrate that shadows are working.

The shadow map size in Ultra Engine is set to 128 to prevent the GPU from running out of video memory. I do not know what exact resolutions correspond to the Unity shadow map settings.

Culling in this test is very minimal, since there are only three renderable objects, so it's purely just a test of updating draw speed. In a more complex scene I would expect to see a larger discrepency between the two renderers, as we see in the culling test.

## Draw Calls ##

This test evaluates efficiency when drawing a large number of unique models, as we would see in a game. Each box is unique and not instanced, with frustum culling performed on the CPU on all objects. "Static batching" in Unity is disabled, because that would disable the functionality we are trying to test.

## Animation ##

This test evaluates each engine's efficiency when performing skinned animation. Each model has a unique skeleton that animates independently.



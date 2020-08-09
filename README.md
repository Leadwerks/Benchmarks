# Benchmarks #

Comparative performance benchmarks for testing.

## Culling ##


## Draw Calls ##


## Animation ##

This test evaluates each engine's efficiency when performing skinned animation. Each model has a unique skeleton that animates independently.

## Shadows ##

This test evaluates the update and render speed of point lights. The moving objects in the scene are designed to trigger a redraw on every point light, and to demonstrate that shadows are in fact working.

The shadow map size in Ultra Engine is set to 128 to prevent the GPU from running out of video memory. I do not know what exact resolutions correspond to the Unity shadow map settings.

Culling in this test is very minimal, since there are only three renderable objects, so it's purely just a test of updating draw speed. In a more complex scene I would expect to see a larger discrepency between the two renderers, as we see in the culling test.

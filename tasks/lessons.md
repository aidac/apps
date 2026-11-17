# Lessons

- **Tracing printed scales off a photo:** never hand-type tick endpoints. Extract the ticks from the photo's pixels
  (threshold, connected components, line fit), look for the geometry (common centre, even spacing, end circles) and
  generate from it; then draw the result over the photo and look at it before calling it done. (E36 economy gauge,
  Nov 17 2026: hand-traced ticks crossed the real ones and nobody overlaid them.)
- **Symmetric print from an angled photo:** before tracing a part the real thing prints symmetric (a gauge, its window),
  check its axis against a face-on photo; when the traced photo is shot at an angle, keep the fitted sizes but generate
  the part mirrored about the true axis, and test the mirror. (E36 economy window, Nov 17 2026: traced off the angled EU
  photo it came out 21 px off the rev counter's centre with uneven corners, and the user saw it.)
- **Realism means the real part, not a generic look:** before shading a part to look "3D" (domes, highlights, gloss),
  check how it looks on the car's photos: the E36's needle hubs are flat caps of fine-grained plastic, not domes. Give a
  part only the depth it really has (its shadow) and the surface it really has (grain). (E36 realism pass, Nov 17 2026:
  domed, highlighted hubs; the user corrected it.)
- **Moving a value by a clock the app can't read:** when a shader extrapolates from the renderer's clock (`u_time`)
  along a path the app sends, anything outside the window where the app's idea of that clock is trusted must hold a
  sent value, never run on along a slope; and the bench's clock has to be the service's, with the bench restarted
  (server.js and page.html don't live-reload) before judging it. (E36 needle paths, Nov 17 2026: a 0.25 s back
  extrapolation sent the needles jumping on the user's bench, whose page still had the old clock.)
- **Making room for BMW's own items under a period face:** don't cut a one-off notch or tab into the design to let one
  item through; change the design's own proportions evenly (a whole strip taller, the parts above moved with it), so it
  still reads as the original part. (E36 drive mode, Nov 17 2026: an 8 px notch over SPORT / INDIVIDUAL "looks dumb";
  the user asked for the whole footer raised, the small gauges and badge moved up.)

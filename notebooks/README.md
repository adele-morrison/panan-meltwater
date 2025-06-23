### Things to fix

In these files I am fixing:
- [ ] Convert temperatures to be same: going to use conservative temperature for everything.  
      - Use gsw library.  
      - Convert PanAntarctic temperatures from potential to conservative  (`gsw.CT_from_pt()`)
- [ ] Correct the times that I am doing (area*values/area) with corrected area (multiply by zero, add ones).  
      - (Optional): replace all uses of `.weighted()` with manual corrected area.
- [ ] Check longitude selections (e.g. using string vs value)
- [ ] Fix thickness weighting: don't weight by `thick['z_l']`, just weight by `thick`.
- [ ] Add the `fillna(0)` to SWMT analysis (to make sure anomalies are not just the intersection of the control and perturbation density masks).

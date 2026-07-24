# sar-crop-mapping

## Notebook 1 : primary-capella - MSE : 739.246
About: uses the competition's capella x-band radar as the main dataset (70% of the answer), with a little help from public Sentinel-1 radar (30%). The Capella part is the simple physical rule  a patch of land is "farmed" if it's not water (radar-dark), not a building (rough texture), and changes across the four dates (crops grow and get harvested; roads and rooftops don't). capella can only see 4 dates and misses some villages, so sentinel-1's denser season and full coverage gently adjust the pattern between villages .

## Notebook 2 : crop-mapping - MSE : 262.416 (👑) *Best submission till now
About: uses several radars together  capella X-band, Sentinel-1, ALOS-2, and InSAR coherence  with a machine-learning model that learns cropland from all of them at once,training labels come from a public optical crop map (Dynamic World), used only while the model learns, never at prediction time so the model itself reads radar only,instead of a hand-written rule,it learns which mix of radar signals means "farmed." Most accurate of the three, because it uses the most information .

## Notebook (Additional): Pure Capella - MSE : 822.710 
About : uses only the competition's capella X-band radar, nothing else noo other satellites, no machine learning, no training labels. It's a simple physical rule: a patch of land is "farmed" if it's not water (radar-dark), not a building (rough texture), and changes across the four dates (crops grow and get harvested; roads and rooftops don't).

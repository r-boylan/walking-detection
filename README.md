

# Walking Detection
Can wearable sensor data predict whether a person is walking?

<iframe
  src="spectral_entropy_scatter.html"
  width="100%"
  height="600"
  frameborder="0"
></iframe>


This scatter plot shows the relationship between accelerometer spectral entropy and accelerometer variability (raw_acc:magnitude_stats:std). Walking tends to appear at higher values of acceleration variability, while non-walking observations are more concentrated at lower values. However, there is noticeable overlap between the two, indicating that these features are informative but not sufficient on their own for perfectly separating walking from non-walking. This suggests that a combination of multiple sensor features is needed for reliable prediction.


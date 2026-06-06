

# Walking Detection

This project explores whether wearable sensor data contains enough information to distinguish walking from non-walking activity. The dataset consists of observations collected from mobile and smartwatch sensors across multiple users. Each row represents a short segment of sensor readings paired with an activity label.

I wanted to explore can wearable sensor data predict whether a person is walking?

This is treated as a binary classification problem where the target variable is:
  label:FIX_walking: 1 indicates walking, 0 indicates not walking.

#Relevant Features
  raw_acc:magnitude_stats:std — measures variability in movement intensity; higher values often indicate more active motion such as walking
  
  raw_acc:magnitude_stats:percentile75 — captures upper-range acceleration values, helping distinguish bursts of movement from steady activity
  
  raw_acc:magnitude_autocorrelation:normalized_ac — measures how repetitive the signal is over time; walking tends to produce more structured patterns
  
  raw_acc:magnitude_autocorrelation:period — estimates the dominant cycle length in movement, useful for detecting rhythmic activity
  
  raw_acc:magnitude_spectrum:spectral_entropy — measures how ordered or random the signal is in the frequency domain; lower entropy often indicates more regular motion

  Detecting walking activity from wearable sensors can help quantify physical activity in everyday life. If walking can be reliably identified from sensor signals, it can support applications such as activity tracking, fitness monitoring, and encouraging regular movement throughout the day.

<iframe
  src="spectral_entropy_scatter.html"
  width="100%"
  height="600"
  frameborder="0"
></iframe>


This scatter plot shows the relationship between accelerometer spectral entropy and accelerometer variability (raw_acc:magnitude_stats:std). Walking tends to appear at higher values of acceleration variability, while non-walking observations are more concentrated at lower values. However, there is noticeable overlap between the two, indicating that these features are informative but not sufficient on their own for perfectly separating walking from non-walking. This suggests that a combination of multiple sensor features is needed for reliable prediction.


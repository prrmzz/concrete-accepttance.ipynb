# concrete-accepttance.ipynb
# Concrete Acceptance Check

This Python function evaluates the acceptance of concrete based on its compressive strength. It checks whether the concrete meets the specified minimum and average compressive strength values required for structural use.

## Formula Logic

The acceptance of the concrete is determined by the following conditions:

### Unacceptable Concrete

If the minimum compressive strength of the sample (`x_min`) is less than 90% of the specified compressive strength (`f_c`), the concrete is deemed unacceptable.

\[
\text{If } x_{\text{min}} < 0.9 \times f_c \text{, the concrete is unacceptable.}
\]

### Acceptable Concrete

If the minimum compressive strength is greater than or equal to 90% of the specified compressive strength, and the average compressive strength (`x_mean`) is greater than or equal to the specified compressive strength (`f_c`), the concrete is considered acceptable.

\[
\text{If } x_{\text{min}} \geq 0.9 \times f_c \text{ and } x_{\text{mean}} \geq f_c \text{, the concrete is acceptable.}
\]

### Structurally Acceptable Concrete

If the minimum compressive strength meets the 90% threshold but the average compressive strength is less than the specified strength, the concrete is structurally acceptable.

\[
\text{If } x_{\text{min}} \geq 0.9 \times f_c \text{ and } x_{\text{mean}} < f_c \text{, the concrete is structurally acceptable.}
\]

### Unknown Status

If none of the above conditions are met, the function returns "Unknown status".

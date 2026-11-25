# SPC Analysis Tools

Набор функций для обработки спектров.

## Пример использования

```python
from spc_tools import fit_segment_coeffs, integrate_spectrum, subtract_dark

y_corr = subtract_dark(y, n_points=50)
area = integrate_spectrum(x, y_corr, peak_range=(510, 550))
n, b = fit_segment_coeffs(powers, integrals, segment=(10.0, 45.0))
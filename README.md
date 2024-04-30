# Yield Curve Analysis Tool

This is a Python-based tool for fetching, processing, and visualizing yield curve data for French and US Treasury bonds. The tool uses the `requests`, `pandas`, `numpy`, `matplotlib`, and `ipywidgets` libraries.

## Class: `yield_curve`

The `yield_curve` class is the main component of this tool. It includes methods for fetching and processing yield curve data, as well as an interactive plotting tool.

### Attributes

- `range_dict`: A dictionary that maps time range strings (e.g., '1D', '1W') to corresponding `pandas.Timestamp` objects.
- `_oat_df`: A placeholder attribute for a `pandas.DataFrame` object that will store fetched and processed French Treasury bond data.
- `_tbond_df`: A placeholder attribute for a `pandas.DataFrame` object that will store fetched and processed US Treasury bond data.

### Methods

- `__init__`: The class initializer. It sets the `range_dict` attribute and the placeholder attributes for the yield curve data.
- `tbond`: A method that fetches US Treasury bond data from the US Department of the Treasury's website, processes the data, and stores it in the `_tbond_df` attribute.
- `oat`: A method that fetches French Treasury bond data from the Banque de France's website, processes the data, and stores it in the `_oat_df` attribute.
- `plot`: A method that creates an interactive plot of the yield curve for a selected treasury type and date range(s).
- `show`: A method that launches the interactive plotting tool.

## Usage

To use this tool, first make sure that you have the required libraries installed. You can install them using `pip`:
```
pip install requests pandas numpy numpy matplotlib ipywidgets
```
Next, create an instance of the `yield_curve` class and launch the interactive plotting tool:
```python
yc = yield_curve()
yc.show()
```
In the interactive plotting tool, select a treasury type ('FR' for French Treasury bonds, 'US' for US Treasury bonds) and one or more date ranges. The tool will fetch and process the yield curve data (if necessary), and then plot the yield curve for the selected date range(s). 

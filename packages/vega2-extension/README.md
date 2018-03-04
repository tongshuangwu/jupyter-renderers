# @jupyterlab/vega2-extension

A mime-renderer extension for JupyterLab that provides support for rendering Vega and Vega-Lite documents and mimebundles.


Example in Python:


```python
from IPython.display import display

display({
    "application/vnd.vegalite.v1+json": {
        "$schema": "https://vega.github.io/schema/vega-lite/v1.json",
        "description": "A simple bar chart with embedded data.",
        "data": {
            "values": [
                {"a": "A", "b": 28}, {"a": "B", "b": 55}, {"a": "C", "b": 43},
                {"a": "D", "b": 91}, {"a": "E", "b": 81}, {"a": "F", "b": 53},
                {"a": "G", "b": 19}, {"a": "H", "b": 87}, {"a": "I", "b": 52}
            ]
        },
        "mark": "bar",
        "encoding": {
            "x": {"field": "a", "type": "ordinal"},
            "y": {"field": "b", "type": "quantitative"}
        }
    }
}, raw=True)
```

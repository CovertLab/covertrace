# covertrace

API to handle live-cell time-series produced by covertrack. 


### Installation
```
git clone --recursive https://github.com/braysia/covertrace.git
cd covertrace
python setup.py install
```

### Examples
See doc/jupyter_examples

```
# Sample Usage
from covertrace.data_array import Sites
from covertrace import ops_plotter, ops_filter, ops_bool

sites = Sites(parent_folder='data/sample_result/', 
              subfolders=['Pos005', 'Pos006'], conditions=['IL1B', 'IL1B'])
operation = partial(ops_plotter.plot_tsplot)
ops_plotter.plot_tsplot(sites['cytoplasm', 'TRITC', 'mean_intensity'])
```



# akram
pip install tfcausalimpact
import pandas as pd
from causalimpact import CausalImpact


data = pd.read_csv('https://raw.githubusercontent.com/WillianFuks/tfcausalimpact/master/tests/fixtures/comparison_data.csv', index_col=['DATE'])
pre_period = ['2019-04-16', '2019-07-14']
post_period = ['2019-7-15', '2019-08-01']
ci = CausalImpact(data, pre_period, post_period, model_args={'fit_method': 'hmc'})

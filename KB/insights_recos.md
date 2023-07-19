|Feature|Insights API| Parameters|Remarks|
|-------|------------|---------|----------|
|Workspace|/service/insights/metrics| metric_label,dimension_label <br/> channels <br/> insight_impact_value|support both in and not in for metric_label and dimension_label <br/>support in for channels <br/> sort by insight_impact_value|
|Deep dive| metrics/insights| metric_label,dimension_label,dimension_value <br> channels <br>insight_impact_value|support in for metric_label, dimension_label, dimension_value <br> support in for channels <br/> sort by insight_impact_value|


|Feature|Recos API| Parameters|Remarks|
|-------|------------|---------|----------|
|Workspace/Deep dive|/recommendations/get| metrics<br>channels<br>recommendation_category<br> revenue_impact<br>enduserstatus|support both in and not in for metrics<br>support in for channels<br>equals/not equals for recommendation_category<br> sort by revenue_impact<br>support in for enduserstatus|

# Visual-Analytics-for-CRF

This project involved the creation of an interactive dashboard 📊 to analyze the performance of a Conditional Random Field (CRF) model trained for Thai address extraction 🇹🇭. The dashboard provides insights ✨ into the model's accuracy in identifying key address components, particularly provinces.

<div class='tableauPlaceholder' id='viz1746515563146' style='position: relative'><noscript><a href='#'><img alt='ทำความเข้าใจโมเดล CRF สำหรับ Address Extractionผ่านการทำนายของโมเดลโดยใช้ข้อมูลจาก Thai NER v2.2 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;In&#47;InfoVisModelInterpretation2&#47;2_1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='InfoVisModelInterpretation2&#47;2_1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;In&#47;InfoVisModelInterpretation2&#47;2_1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-GB' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1746515563146');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.height='1427px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>

![Link to Dashboad](https://public.tableau.com/app/profile/nipun.angkavichai3120/viz/InfoVisModelInterpretation2/2_1)

![visual analytics for crf](visual_analytics_crf.png)

## Key Visualizations

- **Province Prediction Accuracy:** A bar chart 📈 visualizing the percentage of correct province predictions ✅, along with the frequency of each province in the dataset. This allows for a direct comparison 🔍 of prediction success across different provinces.
- **Incorrect Province Tagging:** A stacked bar chart 📊 illustrating the percentage of times each province (LOC tag📍) was incorrectly predicted as other tags ❌. This highlights common misclassifications.
- **Surrounding Word Tagging Analysis:** A 100% stacked bar chart 💯 showing the distribution of predicted tag categories for words surrounding correctly 👍 and incorrectly 👎 identified O, ADDR, and POST tags 🏷️. This helps understand the contextual factors 🤔 influencing prediction accuracy.

## Interactive Features

- **Regional Filtering:** Users can filter ⚙️ the visualizations to focus on specific regions: Bangkok and Metropolitan area 🏙️, and other provinces 🏞️.
- **Details-on-Demand:** Hovering 🖱️ over elements in the visualizations reveals additional information ℹ️. For example, hovering over a segment in the "Incorrect Province Tagging" chart displays the specific incorrect tag and its percentage for that province.
- **Sortable Province Accuracy Chart:** The "Province Prediction Accuracy" bar chart can be sorted ⇅ in ascending or descending order based on the accuracy rate.
Data and Task:

The dataset utilized was derived from the pythainlp/thainer-corpus-v2.2 📚. The original NER tags B-LOCATION and I-LOCATION for provinces, sub-districts, and districts were unified into a single LOC tag 📍. Similarly, B-ZIP was relabeled as POST 📮 to align with the model's predicted tags and facilitate analysis. Thai province, sub-district, and district data from https://github.com/ThepExcel/download/blob/master/ThepExcel-Thailand-Tambon.xlsx 🔗 was used for this tag transformation.

## Insights and Findings

Our initial hypothesis 💡 was that the CRF model would perform less accurately on provinces outside of Bangkok and its vicinity. The developed analytical system 🔎 confirmed this hypothesis:

- **Regional Accuracy Disparity:** The "Province Prediction Accuracy" chart 📈, in conjunction with the regional filter ⚙️, clearly demonstrates a higher percentage of correct LOC predictions ✅ for Bangkok and Metropolitan provinces 🏙️ compared to other provinces 🏞️. Furthermore, when examining performance by region, the Northern region ⬆️ showed the highest accuracy among non-Bangkok areas, while other regions exhibited similar performance. The "Incorrect Province Tagging" chart 📊 further revealed that incorrect LOC predictions frequently resulted in the ADDR tag.
- **Frequency vs. Accuracy:** The "Province Prediction Accuracy" bar chart 📈 indicated that the frequency 🔢 of a province's appearance in the dataset did not directly correlate with the model's prediction accuracy for that province 🤔.
- **Contextual Tagging Patterns:** Analysis of the surrounding words for misclassified POST tags 🏷️ showed a prevalence of the URL tag 🌐. Conversely, correctly identified POST tags 📮 were often surrounded by B-LOCATION or I-LOCATION tags 📍, as evidenced by the "Surrounding Word Tagging Analysis" chart 💯.

  
This project showcases my ability to:

- Perform data preprocessing and feature engineering 🛠️ for Natural Language Processing tasks.
- Develop insightful data visualizations 📊 to communicate complex model performance metrics.
- Design interactive dashboards ⚙️ to facilitate exploratory data analysis.
- Formulate and validate hypotheses 🤔 through data-driven analysis.
- Extract meaningful insights ✨ from model behavior and present them clearly 📢.

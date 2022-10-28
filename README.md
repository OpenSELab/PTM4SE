# PTM4SE
Recent years, deep learning has achieved excellent performance in Software Engineering (SE) tasks. However, excellent performance relies on large-scale training sets, which prevents the application of deep learning techniques in practical tasks. With the release of pre-trained models (PTMs) in the field of deep learning, researchers in SE have begun to pay attention to PTMs, and introduced PTMs into SE tasks. PTMs has made a qualitative leap in SE tasks, which makes intelligent software engineering enter a new era. However, none of the studies have refined the success, failure, and opportunities of pre-trained models in SE. To clarify the work in this cross-field (PTM4SE: Pre-trained models for Software Engineering), we systematically review the current studies related to PTM4SE. Specifically, we firstly describe the framework of the intelligent software engineering methods based on pre-trained models. We then analyze and discuss the commonly used pre-trained models in SE. Meanwhile, we introduce the downstream tasks in SE with pre-trained models in detail, and compare and analyze the performance of pre-trained model techniques on these tasks. We then present the datasets used in SE for training and fine-tuning the PTMs. Finally, we discuss the challenges and opportunities for PTM4SE.

## Research Framework
In order to solve the problem that intelligent SE methods based on DL methods require a large amount of labeled data, researchers in the field of SE have proposed methods that use PTMs to solve tasks in the field of SE, that is, pre-trained model-based intelligent software engineering methods. This method uses a small amount of labeled SE downstream task data to train an intelligent model built on the existing PTMs, so as to form the final PTMs4SE intelligent method to solve downstream tasks in the field of SE (e.g., code generation, program repair, issue report classification, etc.).  

The specific construction process mainly includes four parts: SE downstream task data collection and processing, intelligent method construction based on pre-trained model, model training and model evaluation.<br><br>

<img src="pictures/Research%20framework%20of%20intelligent%20software%20method%20based%20on%20pre-trained%20model.png" width="600px"><br>

## PTMs in SE
Since 2018, researchers in the field of software engineering have begun to study intelligent methods based on PTMs. According to the dataset source of the trained PTMs, the used PTMs can be divided into Off-the-shelf models in DL, Domain-specific models, and source code models.<br><br>

<img src="pictures/Distribution%20of%20pre-trained%20models%20used%20in%20the%20software%20engineering.png" width="800px"><br>

## Dataset
Data sets are the basis of DL models, and their quality directly affects the performance of the model. In particular, intelligent software methods based on PTMs are more inseparable from SE data sets. For example, domain-specific PTMs or source code PTMs need a large number of SE data sets to train the model, and a small amount of SE downstream task data is needed to fine-tune the PTM to complete downstream tasks. In order to better understand the datasets used in intelligent methods based on PTMs, we summarized and analyzed datasets from the field of SE in terms of PTM datasets and downstream task datasets.

### PTM Dataset

<table class="MsoNormalTable" border="0" cellspacing="0" cellpadding="0" width="603" style="width:452.4pt;border-collapse:collapse">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt">
  <td width="33" valign="top" style="width:25.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Type</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.75pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Dataset</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Programming Language</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Source</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Scale</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Open Time</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Link</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">PTMs</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:7.1pt">
  <td width="33" rowspan="6" valign="top" style="width:25.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeSearchNet+C/C#
  datasets<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Ruby/JavaScript/GO/Python/Java/PHP/C/C#<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub+BigQuery<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">8.35G<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://github.com/salesforce/CodeT5<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[28]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub C
  language repositories<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">5.8 G<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C-BERT<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[31]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java and
  TypeScript datasets<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/TypeScript<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CugLM<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[59]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java
  datases&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">/<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">/<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SynFix<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[50]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CLCDSA dataset<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/C/C++<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">AtCoder+CodeJam<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">17.6M<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://github.com/Kawser-nerd/CLCDSA/<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">IR-BERT<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[51]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java
  datasets&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">32G<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://s3.amazonaws.com/code2vec/data/java14m_data.tar.gz"><span style="color:windowtext;text-decoration:none;text-underline:none">https://s3.amazonaws.com/code2vec/data/java14m_data.tar.gz</span></a><o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">InferCode<sup>[35]</sup>/Code2vec<sup>[27]</sup><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:7.1pt">
  <td width="33" rowspan="2" valign="top" style="width:25.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">NL<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SE textual data<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Stack
  Overflow/GitHub/Jira<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">119.7G<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://github.com/smartshark/seBERT/tree/main/data<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">seBERT<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[21]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CoNLL-2003<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Stack Overflow<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">3.16M<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://aclanthology.org/attachments/2020.acl-main.443.Dataset.zip<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BERTOverflow<sup>[21][44]</sup>/CosSensBERT<sup>[44]</sup><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:7.1pt">
  <td width="33" rowspan="4" valign="top" style="width:25.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">NL+<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java datasets
  from CodeSearchNet+SO posts<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/English<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub+SO<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">52.5M<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2022<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://zenodo.org/record/5387856#.Y1TB2nZByUl<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">T5<sup>[24]</sup><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java datasets
  from CodeSearchNet+SO posts<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/English<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1.5M<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">T5<sup>[47]</sup><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java and Python
  from BigQuery+SO posts<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/Python/English<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BigQuery+GitHub<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">655G<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://github.com/wasiahmad/PLBART<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PLBART<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[33]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;mso-yfti-lastrow:yes;height:7.1pt">
  <td width="85" valign="top" style="width:63.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeSearchNet<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Ruby/JavaScript/GO/Python/Java/PHP/English<o:p></o:p></span></p>
  </td>
  <td width="83" valign="top" style="width:61.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="51" valign="top" style="width:38.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">3.5 G<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
  <td width="146" valign="top" style="width:109.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://github.com/github/CodeSearchNet<o:p></o:p></span></p>
  </td>
  <td width="70" valign="top" style="width:52.4pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">T-BERT<sup>[48]</sup>/Graphcodebert<sup>[30]</sup>/CodeBERT<sup>[29]</sup><o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

### Downstream Task Dataset

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" width="590" style="width:442.75pt;border-collapse:collapse;border:none;mso-border-top-alt:
 solid black 1.0pt;mso-border-bottom-alt:solid black 1.0pt;mso-border-insideh:
 1.0pt solid black">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt">
  <td width="39" valign="top" style="width:29.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Type</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="52" valign="top" style="width:39.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Tasks</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Dataset name</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Programming Language</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Scale</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Open Time</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p class="aff3" align="center" style="text-align:center;text-indent:18.6pt"><span style="font-family:宋体;mso-ascii-font-family:&quot;Times New Roman&quot;;mso-hansi-font-family:
  &quot;Times New Roman&quot;">Link</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:7.1pt">
  <td width="39" rowspan="12" valign="top" style="width:29.5pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL<o:p></o:p></span></p>
  </td>
  <td width="52" rowspan="5" valign="top" style="width:39.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">code classification</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java patches<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[27]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">102041<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/TruX-DTF/DL4PatchCorrectness"><span style="color:windowtext;text-decoration:none;text-underline:none">https://github.com/TruX-DTF/DL4PatchCorrectness</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">POJ104<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[39][38][34][19]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C/C++<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">30815<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeCloneBench<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[39][38][42]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">901028<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2014<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SATD dataset<sup>[26]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2016<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/maldonado/tse.satd.data/tree/master/dataset"><span style="color:windowtext;text-decoration:none;text-underline:none">https://github.com/maldonado/tse.satd.data/tree/master/dataset</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SmartBugs Wild
  Dataset<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[58]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">47398<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/smartbugs/smartbugs-wild"><span style="color:windowtext;
  text-decoration:none;text-underline:none">https://github.com/smartbugs/smartbugs-wild</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:7.1pt">
  <td width="52" rowspan="3" valign="top" style="width:39.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">program repair</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">ManySStuBs4J<sup>[37]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">63923<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://github.com/EhsanMashhadi/MSR2021-ProgramRepair/tree/main/data<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Automatic Bug
  Fixing<sup>[47]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">46680<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">TFix-dataset<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">[23]</span></sup><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">JavaScript<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">104804<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">https://drive.google.com/file/d/1CtfnYaVf-q6FZP5CUM4Wh7ofpp8b9ajW/view<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:7.1pt">
  <td width="52" rowspan="2" valign="top" style="width:39.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">code completion</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java and
  TypeScript datasets<sup>[59]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/TypeScript<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">ETH Py150 corpus<sup>[49]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Python<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">74749<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/google-research-datasets/eth_py150_open"><span style="color:windowtext;text-decoration:none;text-underline:none">https://github.com/google-research-datasets/eth_py150_open</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:7.1pt">
  <td width="52" valign="top" style="width:39.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">API</span><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">recommendation</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Req2Lib-dataset<sup>[57]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">5625<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;height:7.1pt">
  <td width="52" valign="top" style="width:39.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">code translation</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeTrans<sup>[48]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/C#<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">10300<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/microsoft/CodeXGLUE"><span style="color:windowtext;
  text-decoration:none;text-underline:none">https://github.com/microsoft/CodeXGLUE</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13;height:7.1pt">
  <td width="39" rowspan="6" valign="top" style="width:29.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">NL<o:p></o:p></span></p>
  </td>
  <td width="52" rowspan="4" valign="top" style="width:39.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">Text classification</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Herzig's issue
  report datasets<sup>[21][46]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2012<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="http://www.st.cs.uni-saarland.de/softevo/bugclassify/"><span style="color:windowtext;text-decoration:none;text-underline:none">http://www.st.cs.uni-saarland.de/softevo/bugclassify/</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Commit messages<sup>[12][40]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1793<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://zenodo.org/record/4266643#.X6vERuLPxPY"><span style="color:
  windowtext;text-decoration:none;text-underline:none">https://zenodo.org/record/4266643#.X6vERuLPxPY</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:15;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">issue report
  from GitHub<sup>[54]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://bitbucket.org/jstzwj/lms4githubissue/src/master/data_view.7z"><span style="color:windowtext;text-decoration:none;text-underline:none">https://bitbucket.org/jstzwj/lms4githubissue/src/master/data_view.7z</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:16;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SEntiMoji
  dataset<sup>[41]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">10,096<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/SEntiMoji/SEntiMoji"><span style="color:windowtext;
  text-decoration:none;text-underline:none">https://github.com/SEntiMoji/SEntiMoji</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:17;height:7.1pt">
  <td width="52" valign="top" style="width:39.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">review responses automatic generation</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">review-response
  pairs datasets<sup>[43][22]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">570881<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:18;height:7.1pt">
  <td width="52" valign="top" style="width:39.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">link prediction</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">traceability
  dataset<sup>[48]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1834<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://zenodo.org/record/4511291#.YB3tjyj0mbg"><span style="color:
  windowtext;text-decoration:none;text-underline:none">https://zenodo.org/record/4511291#.YB3tjyj0mbg</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:19;height:7.1pt">
  <td width="39" rowspan="5" valign="top" style="width:29.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL+NL<o:p></o:p></span></p>
  </td>
  <td width="52" rowspan="3" valign="top" style="width:39.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">code summarization</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code review
  comments (CR)<sup>[21][46]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1600<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2017<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/senticr/SentiCR/"><span style="color:windowtext;
  text-decoration:none;text-underline:none">https://github.com/senticr/SentiCR/</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:20;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Summarization(CS)<sup>[47]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1953940<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing"><span style="color:windowtext;text-decoration:none;text-underline:none">https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:21;height:7.1pt">
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeSearchNet<sup>[48][53]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Ruby/JavaScript/GO/Python/Java/PHP<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/github/CodeSearchNet"><span style="color:windowtext;
  text-decoration:none;text-underline:none">https://github.com/github/CodeSearchNet</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:22;height:7.1pt">
  <td width="52" valign="top" style="width:39.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">code generation</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Concode data<sup>[28][48][15]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">100,000<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2018<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://drive.google.com/drive/folders/1kC6fe7JgOmEHhVFaXjzOmKeatTJy1I1W"><span style="color:windowtext;text-decoration:none;text-underline:none">https://drive.google.com/drive/folders/1kC6fe7JgOmEHhVFaXjzOmKeatTJy1I1W</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:23;height:7.1pt">
  <td width="52" valign="top" style="width:39.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">synthesis</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeXGLUE<sup>[33]</sup><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><a href="https://github.com/microsoft/CodeXGLUE"><span style="color:windowtext;
  text-decoration:none;text-underline:none">https://github.com/microsoft/CodeXGLUE</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:24;mso-yfti-lastrow:yes;height:7.1pt">
  <td width="39" valign="top" style="width:29.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CV<o:p></o:p></span></p>
  </td>
  <td width="52" valign="top" style="width:39.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">UML</span><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">diagram classification </span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="136" valign="top" style="width:102.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">UML</span><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:宋体;mso-ascii-font-family:
  &quot;Times New Roman&quot;;mso-hansi-font-family:&quot;Times New Roman&quot;">diagram</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="67" valign="top" style="width:50.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="58" valign="top" style="width:43.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">14815<o:p></o:p></span></p>
  </td>
  <td width="45" valign="top" style="width:33.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2016<o:p></o:p></span></p>
  </td>
  <td width="193" valign="top" style="width:144.75pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p class="aff3" align="center" style="text-align:center;text-indent:18.6pt"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
</tbody></table>

## Performance Statistics of PTMs

The powerful learning ability of pre-trained models has led researchers in the field of software engineering to apply pre-trained models to various software engineering tasks. We classify the downstream tasks in the software engineering domain into PL (Program Language) related tasks, NL (Natural Language) related tasks, programming language and natural language interaction tasks, and image related tasks in the software engineering domain according to the input data type. On this basis, we measured the performance of different models on various metrics in various downstream tasks.

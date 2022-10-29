# PTM4SE
Recent years, deep learning has achieved excellent performance in Software Engineering (SE) tasks. However, excellent performance relies on large-scale training sets, which prevents the application of deep learning techniques in practical tasks. With the release of pre-trained models (PTMs) in the field of deep learning, researchers in SE have begun to pay attention to PTMs, and introduced PTMs into SE tasks. PTMs has made a qualitative leap in SE tasks, which makes intelligent software engineering enter a new era. However, none of the studies have refined the success, failure, and opportunities of pre-trained models in SE. To clarify the work in this cross-field (PTM4SE: Pre-trained models for Software Engineering), we systematically review the current studies related to PTM4SE. Specifically, we firstly describe the framework of the intelligent software engineering methods based on pre-trained models. We then analyze and discuss the commonly used pre-trained models in SE. Meanwhile, we introduce the downstream tasks in SE with pre-trained models in detail, and compare and analyze the performance of pre-trained model techniques on these tasks. We then present the datasets used in SE for training and fine-tuning the PTMs. Finally, we discuss the challenges and opportunities for PTM4SE.

## Research Framework
In order to solve the problem that intelligent SE methods based on DL methods require a large amount of labeled data, researchers in SE have proposed many methods with PTMs to solve SE-related tasks (i.e., pre-trained model-based intelligent software engineering methods). These methods apply a small amount of labeled data from SE downstream tasks to train an intelligent model based on the existing PTMs, which could achieve the final PTMs4SE intelligent method to solve SE downstream tasks (e.g., code generation, program repair, and issue report classification).  

The specific construction process mainly includes four parts: SE downstream task data collection and processing, intelligent method construction based on pre-trained model, model training and model evaluation.<br><br>

<div align = center>
<img src="pictures/Research%20framework%20of%20intelligent%20software%20method%20based%20on%20pre-trained%20model.png" width="600px"><br>
</div>

<p align="center">Fig.1 Research framework of intelligent software method based on pre-trained model</p>

## PTMs in SE
Since 2018, researchers in the field of software engineering have begun to study intelligent methods based on PTMs. According to the dataset source of the trained PTMs, the used PTMs can be divided into Off-the-shelf models in DL, Domain-specific models, and source code models.<br><br>

<div align = center>
<img src="pictures/Distribution%20of%20pre-trained%20models%20used%20in%20the%20software%20engineering.png" width="800px"><br>
</div>
 
<p align="center">Fig.2 Distribution of pre-trained models used in the software engineering</p>

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

### PL-related tasks

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" width="581" style="width:435.4pt;border-collapse:collapse;border:none;mso-border-top-alt:
 solid black 1.0pt;mso-border-bottom-alt:solid black 1.0pt;mso-border-insideh:
 1.0pt solid black">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:8.5pt">
  <td width="42" valign="top" style="width:31.45pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL <o:p></o:p></span></p>
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="90" valign="top" style="width:67.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Sub-Tasks<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PTMs<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Accuracy<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Precision<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Recall<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">F1<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">MAP<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BLEU<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">EM<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBLEU<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:8.5pt">
  <td width="42" rowspan="38" valign="top" style="width:31.45pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code
  classification<o:p></o:p></span></p>
  </td>
  <td width="90" rowspan="4" valign="top" style="width:67.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Commit
  classifcation<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.80<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.84<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.75<o:p></o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.79<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">seBERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.87</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.85</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.84</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">BERToverflow</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.84</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.81</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.81</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">BERT-BASE</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.77</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.73</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.75</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:8.5pt">
  <td width="90" rowspan="4" valign="top" style="width:67.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Algorithm
  classification<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.85<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.83<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">RoBERTa</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.83</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.80</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">ResNet18</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">86.4</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">85.8</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">84.7</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">82.2</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">ResNet50<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.90<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.86<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.87<o:p></o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.86<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:8.5pt">
  <td width="90" rowspan="4" valign="top" style="width:67.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Technical Debt
  Detection<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b style="mso-bidi-font-weight:normal"><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.82<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">BERT-SO-1M</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.82<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">StackOBERTflow</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.81<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">BERT-comments</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt">0.81<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13;height:8.5pt">
  <td width="90" rowspan="7" valign="top" style="width:67.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Vulnerability Detection<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.92<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.92<o:p></o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.92<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt">CuBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.72<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:15;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">C-BERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.62<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:16;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.64<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:17;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">PLBART</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.63<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:18;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">ResNet18<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.89<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.89<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.89<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:19;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">ResNet50<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.91<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.91<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.91<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:20;height:8.5pt">
  <td width="90" rowspan="9" valign="top" style="width:67.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Defect Detection<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5-base<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.66<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:21;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeT5-small</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt">0.63<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:22;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PLBART<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.63<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:23;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CuBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.95&nbsp;</span></b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:24;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">RoBERTa
  (code)</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.61<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:25;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">BERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.76<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:26;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeBERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.68<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:27;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeBERTa<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.70<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:28;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.71<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:29;height:8.5pt">
  <td width="90" rowspan="10" valign="top" style="width:67.5pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Clone Detection<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">RoBERTa&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.97<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.96<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.96<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:30;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBERT&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.97<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.96<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.96<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.96<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.10<o:p></o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:31;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:32;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeT5-small</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:33;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeT5-base</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:34;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">RoBERTa
  (code)</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.95<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:35;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">PLBART</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:36;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">code2vec</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.82</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.40</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">0.60</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:37;height:1.0pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">OSCAR</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><b style="mso-bidi-font-weight:normal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.49<o:p></o:p></span></b></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:38;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">InferCode</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.90<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.56<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.75<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:39;height:8.5pt">
  <td width="132" colspan="2" rowspan="12" valign="top" style="width:98.95pt;
  border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Program Repair<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5-base<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.77</span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.22</span></b></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:40;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeT5-small</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.76<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold">0.19<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:41;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">RoBERTa</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.75<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:42;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">RoBERTa (code)<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.16<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:43;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.72<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.16<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:44;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.80</span></b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.17<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:45;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PLBART<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.19<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:46;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt">CuBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.89<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:47;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt">T5<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.60<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:48;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeBERTa</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.82<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.81<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.81<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:49;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CC2Vec</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.74<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.73<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.72<o:p></o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.72<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:50;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">BERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.74<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.74<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.70<o:p></o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.72<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:51;height:8.5pt">
  <td width="132" colspan="2" valign="top" style="width:98.95pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Completion<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CugLM&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.84<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:52;height:8.5pt">
  <td width="132" colspan="2" rowspan="7" valign="top" style="width:98.95pt;border:
  none;border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Translation<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">RoBERTa (code)<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.56<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.83<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:53;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBERT<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.80<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.59<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.85<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:54;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PLBART<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold">0.83<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold">0.65<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.88<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:55;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">GraphCodeBERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.81<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.59<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:56;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeT5-small</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.83<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-weight:bold">0.64<o:p></o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:57;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeT5-base</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.84<o:p></o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt">0.66<o:p></o:p></span></b></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:58;height:8.5pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">IR-BERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><b style="mso-bidi-font-weight:normal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.92<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><b style="mso-bidi-font-weight:normal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.86<o:p></o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><b style="mso-bidi-font-weight:normal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.89<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:59;height:8.5pt">
  <td width="132" colspan="2" valign="top" style="width:98.95pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt;font-family:&quot;Times New Roman&quot;,serif">API</span><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"> </span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:&quot;Times New Roman&quot;,serif">Recommendation</span><span lang="EN-US" style="font-family:&quot;Times New Roman&quot;,serif"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">word2vec<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.23<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.93<o:p></o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:60;height:8.5pt">
  <td width="132" colspan="2" rowspan="2" valign="top" style="width:98.95pt;border:
  none;border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">Software
  Effort Estimation<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeBERTa</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><b style="mso-bidi-font-weight:normal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.78<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:61;mso-yfti-lastrow:yes;height:1.0pt">
  <td width="104" valign="top" style="width:78.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeBERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><b style="mso-bidi-font-weight:normal"><span lang="EN-US" style="font-size:9.0pt;font-family:&quot;Times New Roman&quot;,serif">0.78<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="38" valign="top" style="width:28.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="41" valign="top" style="width:30.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="49" valign="top" style="width:36.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.0pt">
  <p class="MsoNormal" align="left" style="text-align:left;mso-pagination:widow-orphan;
  vertical-align:top"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
</tbody></table>

### Interaction tasks between PL and NL

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" width="578" style="width:433.45pt;border-collapse:collapse;border:none;mso-border-top-alt:
 solid black 1.0pt;mso-border-bottom-alt:solid black 1.0pt;mso-border-insideh:
 1.0pt solid black">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:8.5pt">
  <td width="125" valign="top" style="width:93.7pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">NL+PL<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="112" valign="top" style="width:84.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PTMs<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BLEU-4<o:p></o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BLEU<o:p></o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBLEU<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">EM<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">MRR<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:8.5pt">
  <td width="125" rowspan="6" valign="top" style="width:93.7pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Summarization<o:p></o:p></span></p>
  </td>
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5-base<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.20</span></b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5-small<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold">0.19<o:p></o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PLBART<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.18<o:p></o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">RoBERTa</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.17<o:p></o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeBERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.18<o:p></o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">GraphCodeBERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.19<o:p></o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:8.5pt">
  <td width="125" rowspan="5" valign="top" style="width:93.7pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Generation<o:p></o:p></span></p>
  </td>
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5-base<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.41<o:p></o:p></span></b></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.43<o:p></o:p></span></b></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.22<o:p></o:p></span></b></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5-small<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold">0.38<o:p></o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold">0.41<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-bidi-font-weight:
  bold">0.22<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PLBART<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.37<o:p></o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.39<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.19<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">GPT-2</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.25<o:p></o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.30<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.17<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">CodeGPT-2</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.29<o:p></o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.33<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.18<o:p></o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;height:8.5pt">
  <td width="125" valign="top" style="width:93.7pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Review<o:p></o:p></span></p>
  </td>
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">T5<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.82</span></b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13;height:8.5pt">
  <td width="125" rowspan="5" valign="top" style="width:93.7pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Search<o:p></o:p></span></p>
  </td>
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">RoBERTa(code)<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.62<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">RoBERTa</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.60<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:15;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">InferCode<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.57<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:16;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBERT<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.68<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:17;mso-yfti-lastrow:yes;height:8.5pt">
  <td width="112" valign="top" style="width:84.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td width="68" valign="top" style="width:51.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="91" valign="top" style="width:68.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="88" valign="top" style="width:66.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:36.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="46" valign="top" style="width:34.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.70</span></b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

### CV-related tasks

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" width="578" style="width:433.45pt;border-collapse:collapse;border:none;mso-border-top-alt:
 solid black 1.0pt;mso-border-bottom-alt:solid black 1.0pt;mso-border-insideh:
 1.0pt solid black">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:8.5pt">
  <td width="161" valign="top" style="width:120.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CV<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="95" valign="top" style="width:70.9pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PTMs<o:p></o:p></span></p>
  </td>
  <td width="323" valign="top" style="width:242.05pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">Accuracy</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;mso-yfti-lastrow:yes;height:8.5pt">
  <td width="161" valign="top" style="width:120.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt">UML diagram Classification<o:p></o:p></span></p>
  </td>
  <td width="95" valign="top" style="width:70.9pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:black;background:white">VGG-16</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="323" valign="top" style="width:242.05pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">0.50</span></b><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

### NL-related tasks

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" align="left" width="572" style="width:428.85pt;border-collapse:collapse;border:none;
 mso-border-top-alt:solid black 1.0pt;mso-border-bottom-alt:solid black 1.0pt;
 mso-table-overlap:never;mso-table-lspace:9.0pt;margin-left:6.75pt;mso-table-rspace:
 9.0pt;margin-right:6.75pt;mso-table-anchor-vertical:paragraph;mso-table-anchor-horizontal:
 margin;mso-table-left:left;mso-table-top:6.2pt;mso-border-insideh:1.0pt solid black">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt">
  <td width="95" valign="top" style="width:70.9pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">NL <o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.35pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Sub-Tasks<o:p></o:p></span></p>
  </td>
  <td width="92" valign="top" style="width:69.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">PTMs<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Accuracy&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Precision<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Recall<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">F1<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">MCC&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">AUC<o:p></o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">BLEU&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">MAP<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:7.1pt">
  <td width="95" rowspan="22" valign="top" style="width:70.9pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">SE Related Text classification<o:p></o:p></span></p>
  </td>
  <td width="66" rowspan="5" valign="top" style="width:49.35pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Issue classification<o:p></o:p></span></p>
  </td>
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">BERT-base<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.76<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.85<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">BERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt">0. <span style="color:black;background:white">33</span><o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.46<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.38<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">BERToverflow<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.80<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.86<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.81<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">seBERT<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.79<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.89<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.80<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">RoBERTa<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.82<o:p></o:p></span></b></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.84<o:p></o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.86<o:p></o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.85<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:7.1pt">
  <td width="66" rowspan="8" valign="top" style="width:49.35pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">APP Review classification<o:p></o:p></span></p>
  </td>
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">BERT<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.94<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.61<o:p></o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.79<o:p></o:p></span></b></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">RoBERTa<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.94<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.59<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.78<o:p></o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:10.5pt;color:black;
  background:white">ALBERT</span><span lang="EN-US" style="font-size:10.5pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.93<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.48<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.70<o:p></o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:10.5pt;color:black;
  background:white">BERTOverflow</span><span lang="EN-US" style="font-size:10.5pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.90<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.13<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.59<o:p></o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">XLNet<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.94<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.52<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.75<o:p></o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">BERT-SO-1M</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.90<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">BERT-reviews</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.92<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">StackOBERTflow</span><span lang="EN-US" style="font-size:
  9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.86<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14;height:7.1pt">
  <td width="66" rowspan="9" valign="top" style="width:49.35pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Sentiment classification (positive)<o:p></o:p></span></p>
  </td>
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">DeepMoji<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.95<o:p></o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.95<o:p></o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.95<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:15;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">BERT<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.79<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.78<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:16;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">RoBERTa<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.80<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.79<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:17;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">BERT-SO-1M</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.88<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:18;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">BERT-SO-1M-large</span><span lang="EN-US" style="font-size:
  9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.93<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.94<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:19;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">DistilRoBERTa</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.92<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.92<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:20;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">StackOBERTflow</span><span lang="EN-US" style="font-size:
  9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.93<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.94<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:21;height:1.25pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">ALBERT</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.79<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.74<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.77<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:1.25pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:22;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;color:black;
  background:white">XLNet<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.75<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.81<o:p></o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.78<o:p></o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:23;height:15.3pt">
  <td width="160" colspan="2" rowspan="2" valign="top" style="width:120.25pt;
  border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Review Responses Automatic Generation<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-element:frame;mso-element-frame-hspace:
  9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:paragraph;
  mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;mso-height-rule:
  exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">RoBERTa<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">0.24<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:24;height:7.1pt">
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">BERT<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.57</span></b><span lang="EN-US" style="font-size:
  9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:25;mso-yfti-lastrow:yes;height:7.1pt">
  <td width="160" colspan="2" valign="top" style="width:120.25pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">Link prediction<o:p></o:p></span></p>
  </td>
  <td width="92" valign="top" style="width:69.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt">BERT<o:p></o:p></span></p>
  </td>
  <td width="40" valign="top" style="width:30.0pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="42" valign="top" style="width:31.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.97<o:p></o:p></span></b></p>
  </td>
  <td width="43" valign="top" style="width:32.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="39" valign="top" style="width:29.25pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="37" valign="top" style="width:27.75pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td width="40" valign="top" style="width:30.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan;mso-element:
  frame;mso-element-frame-hspace:9.0pt;mso-element-wrap:around;mso-element-anchor-vertical:
  paragraph;mso-element-anchor-horizontal:margin;mso-element-top:6.2pt;
  mso-height-rule:exactly"><b><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt">0.99<o:p></o:p></span></b></p>
  </td>
 </tr>
</tbody></table>

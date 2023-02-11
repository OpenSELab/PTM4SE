# PTM4SE
Recent years, deep learning has achieved excellent performance in Software Engineering (SE) tasks. However, excellent performance relies on large-scale training sets, which prevents the application of deep learning techniques in practical tasks. With the release of pre-trained models (PTMs) in the field of deep learning, researchers in SE have begun to pay attention to PTMs, and introduced PTMs into SE tasks. PTMs has made a qualitative leap in SE tasks, which makes intelligent software engineering enter a new era. However, none of the studies have refined the success, failure, and opportunities of pre-trained models in SE. To clarify the work in this cross-field (PTM4SE: Pre-trained models for Software Engineering), we systematically review the current studies related to PTM4SE. Specifically, we firstly describe the framework of the intelligent software engineering methods based on pre-trained models. We then analyze and discuss the commonly used pre-trained models in SE. Meanwhile, we introduce the downstream tasks in SE with pre-trained models in detail, and compare and analyze the performance of pre-trained model techniques on these tasks. We then present the datasets used in SE for training and fine-tuning the PTMs. Finally, we discuss the challenges and opportunities for PTM4SE.

## 1. Research Framework
In order to solve the problem that intelligent SE methods based on DL methods require a large amount of labeled data, researchers in SE have proposed many methods with PTMs to solve SE-related tasks (i.e., pre-trained model-based intelligent software engineering methods). These methods apply a small amount of labeled data from SE downstream tasks to train an intelligent model based on the existing PTMs, which could achieve the final PTMs4SE intelligent method to solve SE downstream tasks (e.g., code generation, program repair, and issue report classification).  

The specific construction process mainly includes four parts: SE downstream task data collection and processing, intelligent method construction based on pre-trained model, model training and model evaluation.<br><br>

<div align = center>
<img src="pictures/Research%20framework%20of%20intelligent%20software%20method%20based%20on%20pre-trained%20model.png" width="600px"><br>
</div>

<p align="center">Fig.1 Research framework of intelligent software method based on pre-trained model</p>

## 2. PTMs in SE
Since 2018, researchers in SE have begun to introduce different types of PTMs into the SE-related task. Thus, we collected the intelligent software engineer with the PTMs and divided them into four types:Off-the-shelf models, Domain-specific models, and source code models.<br><br>

<div align = center>
<img src="pictures/Distribution%20of%20pre-trained%20models%20used%20in%20the%20software%20engineering.png" width="800px"><br>
</div>
 
<p align="center">Fig.2 Distribution of pre-trained models used in the software engineering</p>

### 2.1 Off-the-shelf Models

Off-the-shelf Models are the pre-trained models that are trained on general domain datasets in the DL doamin, e.g., BERT (or GPT or XLNet) pre-trained models which are trained on English Wikipedia and general news datasets in Natural language processing (NLP), and ResNet and VGG models which are pretrained on ImageNet datasets in computer vision (CV). Thus, we divide the off-the-shelf models into two categories:  off-the-shelf models in the NLP and  off-the-shelf models in the CV.

### 2.2 Domain-specific Models

Domain-specific models are the pre-trained models that are trained on the SE-specific datasets (e.g., GitHub, Stack Overflow, and JIRA). In recent years, researchers in SE have collected a large number of SE-specific datasets to re-train the DL models, such as SeBERT, Text-To-Text Transfer Transformer(T5) model, Word2Vec-SO, BERT-reviews, BERT-SO-1M, BERT-SO-1M-Large, and RoBERTa-SO in Fig. 2.

### 2.3 Source Code Models

Source code models are the pre-trained models that are trained on source codes to understand the syntax and semantic information included in the source data. For now, researchers in SE have collected different language of source code to retrain the DL models, such as Code2Vec,CodeT5, CodeBERT, GraphCodeBERT, C-BERT, CuBERT, CodeBERT, and CodeBERT. PLBART, OSCAR, InferCode, and DOBF in Fig. 2.

## 3. Common Available SE Datasets
Datasets as one of important components in PTMs affect the performance of PTMs for the SE-related tasks. To get the higher performance of intelligent software engineering methods, researchers in SE have collected different types of SE datasets to train or fine-tune the models. To present and understand the current SE datasets, we summarized and analyzed these datasets in SE, and divided them into PTMs datasets and SE-related downstream Task Dataset.

### 3.1 PTMs Datasets

PTMs datasets are datasets that are used for Trained a DL model from scratch. The PTMs datasets frequently used in SE are listed in the table, which are also collected in our datasets files in this repository. 

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0 width=501
 style='width:375.65pt;border-collapse:collapse;border:none;mso-border-alt:
 solid windowtext .5pt;mso-padding-alt:0cm 5.4pt 0cm 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt'>
  <td width=33 valign=top style='width:25.0pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Type</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=90 valign=top style='width:67.15pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Dataset</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Programming
  Language</span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Source</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Scale</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Open Time</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>PTMs</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;height:7.1pt'>
  <td width=33 rowspan=10 valign=top style='width:25.0pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PL<o:p></o:p></span></p>
  </td>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/salesforce/CodeT5"><span
  style='font-size:6.5pt'>CodeSearchNet+C/C# datasets</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Ruby/ JavaScript/ GO/ Python/ Java/ PHP/ C/
  C#<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>GitHub+BigQuery</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>8.35G<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub C language repositories<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>5.8 G<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C-BERT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java and TypeScript datasets<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/ TypeScript<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CugLM</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java <span class=SpellE>datases</span>&nbsp;<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>SynFix</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/Kawser-nerd/CLCDSA/"><span
  style='font-size:6.5pt'>CLCDSA dataset</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/ C/ C++<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>AtCoder+CodeJam</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>17.6M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>IR-BERT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://s3.amazonaws.com/code2vec/data/java14m_data.tar.gz"><span
  style='font-size:6.5pt'>Java datasets</span></a></span><span lang=EN-US
  style='font-size:6.5pt'>&nbsp;<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>32G<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>InferCode</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code2vec<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/google-research-datasets/eth_py150_open">ETH Py150
  Open corpus</a><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>190M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeTrek</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>unique Python files<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>159GB<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeX</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/tech-srl/code2seq/tree/master/JavaExtractor%20and%20https:/github.com/tech-srl/code2vec/tree/master/JavaExtractor">JavaSmall
  and JavaMed datasets</a><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>4.7M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Coder<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python and Java pre-training corpus<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/ Python<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>21.3M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CuBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'>/</span><span lang=EN-US> </span><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>TreeBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11;height:7.1pt'>
  <td width=33 rowspan=2 valign=top style='width:25.0pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>NL<o:p></o:p></span></p>
  </td>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/smartshark/seBERT/tree/main/data"><span
  style='font-size:6.5pt'>SE textual data</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>English<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Stack Overflow<o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Jira<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>119.7G<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>seBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://aclanthology.org/attachments/2020.acl-main.443.Dataset.zip"><span
  style='font-size:6.5pt'>CoNLL-2003</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>English<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Stack Overflow<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>3.16M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>BERTOverflow</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CosSensBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13;height:7.1pt'>
  <td width=33 rowspan=7 valign=top style='width:25.0pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>NL+<o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PL<o:p></o:p></span></p>
  </td>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://zenodo.org/record/5387856#.Y1TB2nZByUl"><span
  style='font-size:6.5pt'>Java datasets from CodeSearchNet+SO posts</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/ English<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>GitHub+SO</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>52.5M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2022<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>T5<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing"><span
  style='font-size:6.5pt'>Java datasets from CodeSearchNet+SO posts</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/ English<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1.5M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>T5<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:15;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/wasiahmad/PLBART"><span
  style='font-size:6.5pt'>Java and Python from BigQuery+SO posts</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/ Python/ English<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>BigQuery+GitHub</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>655G<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:16;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/github/CodeSearchNet"><span
  style='font-size:6.5pt'>CodeSearchNet</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Ruby/ JavaScript/ GO/ Python/ Java/ PHP/ English<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>3.5 G<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>T-BERT<o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>Graphcodebert</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:17;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python corpus of <span class=SpellE>CodeSearchNet</span>
  dataset<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1.6M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CLAWSAT/ CODE-MVP<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:18;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java corpus of <span class=SpellE>CodeSearchNet</span>
  dataset<o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2.0M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CLAWSAT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:19;mso-yfti-lastrow:yes;height:7.1pt'>
  <td width=90 valign=top style='width:67.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>AnghaBench</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td width=104 valign=top style='width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C<o:p></o:p></span></p>
  </td>
  <td width=85 valign=top style='width:63.8pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GitHub<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.53M<o:p></o:p></span></p>
  </td>
  <td width=47 valign=top style='width:35.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
  <td width=94 valign=top style='width:70.85pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>COMBO<o:p></o:p></span></p>
  </td>
 </tr>
</table>

### 3.2 SE-related Downstream Task Dataset

SE-related downstream task datasets are the datasets used to fine tune the intellignet DL models for the se-related downstream tasks. Common SE-related downstream datasets frequently used are listed in the followed table.

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-padding-alt:0cm 5.4pt 0cm 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt'>
  <td valign=top style='border:solid windowtext 1.0pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Type</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Tasks</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Dataset</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Programming
  Language</span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Scale</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:#24292F;background:white'>Open Time</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;height:7.1pt'>
  <td rowspan=28 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PL<o:p></o:p></span></p>
  </td>
  <td rowspan=16 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Classification<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/TruX-DTF/DL4PatchCorrectness"><span
  style='font-size:6.5pt'>Java patches</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>102041<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>POJ104<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>30815<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeCloneBench</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>901028<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2014<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://github.com/maldonado/tse.satd.data/tree/master/dataset"><span
  style='font-size:6.5pt'>SATD dataset</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2016<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/smartbugs/smartbugs-wild"><span
  style='font-size:6.5pt'>SmartBugs Wild Dataset</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>47398<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://sites.google.com/view/du-commits/home">SPI</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>298917<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a href="https://www.qemu.org/index.html">QEMU</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>13600<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2005<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://www.linuxjournal.com/article/8517">FFmpeg</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>4919<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2006<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/microsoft/CodeXGLUE/tree/main/Code-Code/Defect-detection">Devign</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>27318</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Merge <span class=SpellE>Conflcts</span>
  Dataset<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C#/JavaScript/TypeScript/Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>219934<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2022<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://anonymous.4open.science/r/CommitMessageEmpirical/README.mdd">Multi-language
  Commit Message Dataset (MCMD)</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/C#/C++/Python/JavaScript<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2250000</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2022<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/CGCL-codes/VulDeePecker">Vuldeepecker</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>61638</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2018<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a href="https://osf.io/d45bw/">Draper</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1274366<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2018<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/VulDetProject/ReVeal/tree/master/data">REVEAL</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>18169<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:15;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/muVulDeePecker/muVulDeePecker">muVuldeepecker (MVD)</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>181641<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:16;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a href="https://github.com/ibm/D2A">D2A</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C/C++<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1295623</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:17;height:7.1pt'>
  <td rowspan=7 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Program Repair<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://github.com/EhsanMashhadi/MSR2021-ProgramRepair/tree/main/data"><span
  style='font-size:6.5pt'>ManySStuBs4J</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>63923<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:18;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing"><span
  style='font-size:6.5pt'>Automatic Bug Fixing</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>46680<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:19;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://drive.google.com/file/d/1CtfnYaVf-q6FZP5CUM4Wh7ofpp8b9ajW/view"><span
  style='font-size:6.5pt'>TFix-dataset</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>JavaScript<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>104804<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:20;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/jkoppel/QuixBugs">QuixBugs</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python/Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2017<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:21;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/lin-tan/CoCoNut-Artifact/releases">CoCoNut</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/Python/C/JavaScript<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>9675342<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:22;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="http://salt.ece.ubc.ca/software/bugaid/">BugAID</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>JavaScript<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2016<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:23;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://repairbenchmarks.cs.umass.edu/ManyBugs/">ManyBugs</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>10468<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2015<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:24;height:7.1pt'>
  <td rowspan=2 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Completion<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java and TypeScript datasets<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/TypeScript<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:25;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://github.com/google-research-datasets/eth_py150_open"><span
  style='font-size:6.5pt'>ETH Py150 corpus</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>74749<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:26;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>API Recommendation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Req2Lib-dataset<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>5625<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:27;height:7.1pt'>
  <td rowspan=2 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Translation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/microsoft/CodeXGLUE">Coode-code (CodeTrans</a><span
  class=MsoHyperlink>)</span><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java/C#<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>10300<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:28;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/IBM/Project_CodeNet">Python800 dataset</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>240000<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:29;height:7.1pt'>
  <td rowspan=6 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>NL<o:p></o:p></span></p>
  </td>
  <td rowspan=4 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Text Classification<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="http://www.st.cs.uni-saarland.de/softevo/bugclassify/"><span
  style='font-size:6.5pt'>Herzig's issue report datasets</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>English<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2012<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:30;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://zenodo.org/record/4266643#.X6vERuLPxPY"><span
  style='font-size:6.5pt'>Commit messages</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>English<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1793<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:31;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://bitbucket.org/jstzwj/lms4githubissue/src/master/data_view.7z"><span
  style='font-size:6.5pt'>issue report from GitHub</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>English<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:32;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/SEntiMoji/SEntiMoji"><span
  style='font-size:6.5pt'>SEntiMoji dataset</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>10096<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:33;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Review Responses Automatic Generation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>review-response pairs datasets<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>English<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>570881<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:34;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Link Prediction<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://zenodo.org/record/4511291#.YB3tjyj0mbg"><span
  style='font-size:6.5pt'>traceability dataset</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>English<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1834<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:35;height:7.1pt'>
  <td rowspan=20 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PL+NL<o:p></o:p></span></p>
  </td>
  <td rowspan=8 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt'><span lang=EN-US style='font-size:6.5pt'>Code
  Generation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://drive.google.com/drive/folders/1kC6fe7JgOmEHhVFaXjzOmKeatTJy1I1W"><span
  style='font-size:6.5pt'>Concode data</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>100,000<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2018<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:36;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>DJANGO<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>18805<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2015<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:37;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/rajasagashe/juice">JUICE-10K</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>13946</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:38;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/google-research/google-research/tree/master/mbpp">MBPP</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>974<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:39;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://yale-lily.github.io/spider">Spider</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SQL<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>5693<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2018<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:40;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a href="https://github.com/hendrycks/apps">APPS</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>232421<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:41;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/deepmind/code_contests">CodeContests</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>C++/Python/Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>13610</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2022<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:42;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/openai/human-eval">HumanEval</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:43;height:7.1pt'>
  <td rowspan=5 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Summarization<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/senticr/SentiCR/"><span
  style='font-size:6.5pt'>Code review comments (CR)</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1600<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2017<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:44;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a
  href="https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing"><span
  style='font-size:6.5pt'>Code <span class=GramE>Summarization(</span>CS)</span></a></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>1953940<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:45;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/github/CodeSearchNet"><span
  style='font-size:6.5pt'>CodeSearchNet</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Ruby/JavaScript/GO/Python/Java/PHP<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:46;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java projects from GitHub<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>134239<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:47;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a href="http://www.srl.inf.ethz.ch/py150">PY150</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>30 000<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2016<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:48;height:7.1pt'>
  <td rowspan=5 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Search<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/microsoft/CodeXGLUE/tree/main/Text-Code/NL-code-search-Adv">AdvTest
  dataset</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>280634</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:49;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a href="https://conala-corpus.github.io/">CoNaLa</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python/Java<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>79809<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2018<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:50;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/nokia/codesearch">SO-DS</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>13250<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:51;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/LittleYUYU/StackOverflow-Question-Code-Dataset">StaQC</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>147546<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2018<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:52;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/Jun-jie-Huang/CoCLR/tree/main/data">CoSQA</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>20604<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:53;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Review<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><a
  href="https://github.com/microsoft/CodeBERT/tree/master/CodeReviewer">CodeReview
  data</a><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Python/Java/Go/C++/JavaScript/C/C#/<span
  class=SpellE>Php</span>/Ruby<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2022<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:54;height:7.1pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Synthesis<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US><a href="https://github.com/microsoft/CodeXGLUE"><span
  style='font-size:6.5pt'>CodeXGLUE</span></a></span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:55;mso-yfti-lastrow:yes;height:7.1pt'>
  <td valign=top style='border:solid windowtext 1.0pt;border-top:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CV<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>UML Diagram Classification<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>UML Diagram<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>14815<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>2016<o:p></o:p></span></p>
  </td>
 </tr>
</table>

## 4. SE-related tasks that used the PTMs and their performance

 Researchers in SE have applied many PTMs into various SE-related tasks because of the powerful learning ability of PTMs. We summarized and analyzed these SE-related tasks with the PTMs. Meanwhile, based on the types of input datasets, we divided them into four types: programming language (PL) related tasks, natural language (NL) related tasks in the SE domain, the interaction task among PL and NL, and image related tasks in the SE domain.

<div align = center>
<img src="pictures/Distribution%20of%20downstream%20tasks%20with%20pre-trained%20models%20in%20software%20engineering.jpg" width="900px"><br>
</div>

<p align="center">Fig.3 Distribution of downstream tasks with pre-trained models in software engineering</p>

### 4.1 PL-related tasks

PL-related tasks are the tasks to solve the problems through studying the syntactic and semantic feature representations of source code. The current main tasks and performance are listed in the followed table.

<div align=center>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-padding-alt:0cm 5.4pt 0cm 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes;height:8.5pt'>
  <td valign=top style='border:solid windowtext 1.0pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p align=center style='text-align:center;mso-line-height-alt:.9pt;mso-pagination:
  widow-orphan'><span lang=EN-US style='font-size:6.5pt'>PL<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Sub-Tasks<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PTMs<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Accuracy<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Precision<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Recall<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>F1<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>MAP<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BLEU<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>EM<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeBLEU<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>MCC<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>EditSIM<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Number of fixed bugs<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;height:8.5pt'>
  <td rowspan=48 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code classification<o:p></o:p></span></p>
  </td>
  <td rowspan=4 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Commit classifcation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.80<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.84<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.75<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.79<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>seBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.87</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.85</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.84</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERToverflow</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.84</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.81</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.81</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT-BASE</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.77</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.73</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.75</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5;height:8.5pt'>
  <td rowspan=5 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Algorithm classification<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.85<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.83<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>RoBERTa</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.83</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.80</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>COMBO<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.74<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>ResNet18</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>86.4</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>85.8</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>84.7</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>82.2</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>ResNet50<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.90<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.86<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.87<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.86<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10;height:8.5pt'>
  <td rowspan=4 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Technical Debt Detection<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b
  style='mso-bidi-font-weight:normal'><span lang=EN-US style='font-size:6.5pt'>0.82<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT-SO-1M</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.82<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>StackOBERTflow</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.81<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT-comments</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.81<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14;height:8.5pt'>
  <td rowspan=8 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Vulnerability Detection<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.92<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.92<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.92<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:15;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CuBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.72<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:16;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>COMBO<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.67<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:17;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>C-BERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.62<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:18;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.64<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.54<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:19;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>PLBART</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.63<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:20;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>ResNet18<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.89<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.89<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.89<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:21;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>ResNet50<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.91<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.91<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.91<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:22;height:8.5pt'>
  <td rowspan=12 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Defect Detection<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5-base<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.66<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:23;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5-small</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.63<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:24;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.64<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.60<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.27<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:25;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.63<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:26;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CuBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.95&nbsp;</span></b><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:27;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>RoBERTa
  (code)</span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.61<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:28;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.76<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:29;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.68<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.54<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.27<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:30;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeBERTa<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.70<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.59<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.27<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:31;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.71<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:32;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CODE-MVP<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.89<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:33;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SynCoBERT<span style='color:black;
  background:white'><o:p></o:p></span></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.65<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:34;height:8.5pt'>
  <td rowspan=15 valign=top style='border-top:none;border-left:none;border-bottom:
  solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Clone Detection<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.96<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.96<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:35;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeBERT&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.96<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.96<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.96<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.10<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:36;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:37;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5-small</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:38;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5-base</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.95<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:39;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>RoBERTa
  (code)</span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.95<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:40;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>PLBART</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.95<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:41;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>code2vec</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.82</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.40</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'>0.60</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:42;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>T5<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p><span lang=EN-US style='font-size:6.5pt;color:black;background:white'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.70<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:43;height:1.0pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>OSCAR</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif;
  mso-bidi-font-weight:bold'>0.49<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:44;height:1.0pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>COMBO<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.64<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif;
  mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:45;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>InferCode</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.90<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.56<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.75<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:46;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SynCoBERT<span style='color:black;
  background:white'><o:p></o:p></span></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.97<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.98<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.97<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.88<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:47;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SCodeR<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.95<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.96<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.95<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.92<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:48;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>UniXcoder<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.98<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.93<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.95<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.91<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:49;height:8.5pt'>
  <td colspan=2 rowspan=12 valign=top style='border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Program Repair<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5-base<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.22</span></b><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:50;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5-small</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.76<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.19<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:51;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>RoBERTa</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.75<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:52;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa (code)<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.16<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:53;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.72<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.16<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:54;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.80</span></b><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.17<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:55;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.19<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:56;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CuBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.89<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:57;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>T5<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.60<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>64/182<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:58;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeBERTa</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.82<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.81<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.81<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:59;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CC2Vec</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.74<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.73<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.72<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.72<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:60;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.74<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.74<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.70<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.72<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:61;height:8.5pt'>
  <td colspan=2 rowspan=7 valign=top style='border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Completion<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CugLM&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.84<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:62;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>UniXcoder<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.43<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'>0.72<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b><span lang=EN-US style='font-size:6.5pt;font-family:
  "Times New Roman",serif'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:63;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.38<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.68<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:64;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.37<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.67<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:65;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SPT-Code<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.27<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:66;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>TreeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.25<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:67;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>GraphCodeBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.25<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:68;height:8.5pt'>
  <td colspan=2 rowspan=12 valign=top style='border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Translation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa (code)<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.56<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.83<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:69;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.80<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.59<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.85<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:70;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.83<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.65<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.88<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:71;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SynCoBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.61<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.82<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:72;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>StructCoder<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.85<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b
  style='mso-bidi-font-weight:normal'><span lang=EN-US style='font-size:6.5pt'>0.67<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.88<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:73;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SPT-Code<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b
  style='mso-bidi-font-weight:normal'><span lang=EN-US style='font-size:6.5pt'>0.90<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.64<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:74;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>TreeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.81<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.60<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:75;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CugLM<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.83<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.62<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:76;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>GraphCodeBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.81<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.59<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:77;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5-small</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.83<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.64<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:78;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeT5-base</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.84<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.66<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:79;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>IR-BERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b style='mso-bidi-font-weight:normal'><span lang=EN-US
  style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.92<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b style='mso-bidi-font-weight:normal'><span lang=EN-US
  style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.86<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b style='mso-bidi-font-weight:normal'><span lang=EN-US
  style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.89<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:80;height:8.5pt'>
  <td colspan=2 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>API
  Recommendation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>word2vec<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.23<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.93<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:81;height:8.5pt'>
  <td colspan=2 rowspan=2 valign=top style='border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'>Software
  Effort Estimation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeBERTa</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b style='mso-bidi-font-weight:normal'><span lang=EN-US
  style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.78<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:82;mso-yfti-lastrow:yes;height:1.0pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><b style='mso-bidi-font-weight:normal'><span lang=EN-US
  style='font-size:6.5pt;font-family:"Times New Roman",serif'>0.78<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:1.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
</table>

</div>

### 4.2 NL-related tasks

NL-related tasks are the tasks to solve the problems through studying the feature represents included in the text information (e.g., issue report, commit message
) in SE, such as the classification of issue reports, the classfication of APP review, and the sentiment classification. The current NL-related tasks with the PTMs and their performance are presented in the followed table to help developers better understand textual information in the field of software engineering.

<div align=center>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-top-alt:solid black 1.0pt;
 mso-border-bottom-alt:solid black 1.0pt;mso-border-insideh:1.0pt solid black'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt'>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>NL <o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Sub-Tasks<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PTMs<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Accuracy&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Precision<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Recall<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>F1<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>MCC&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>AUC<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BLEU&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>MAP<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;height:7.1pt'>
  <td rowspan=22 valign=top style='border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SE Related Text classification<o:p></o:p></span></p>
  </td>
  <td rowspan=5 valign=top style='border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Issue classification<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERT-base<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.76<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.85<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0. <span style='color:black;background:
  white'>33</span><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.46<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.38<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERToverflow<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.80<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.86<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.81<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>seBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.79<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.89<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.80<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.82<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.84<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.86<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.85<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6;height:7.1pt'>
  <td rowspan=8 valign=top style='border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>APP Review classification<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.94<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.61<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.79<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.94<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.59<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.78<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>ALBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.93<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.48<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.70<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERTOverflow</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.90<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.13<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.59<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>XLNet<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.94<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.52<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.75<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT-SO-1M</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.90<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT-reviews</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.92<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>StackOBERTflow</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.86<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14;height:7.1pt'>
  <td rowspan=9 valign=top style='border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Sentiment classification (positive)<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>DeepMoji<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.95<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.95<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.95<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:15;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.79<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.78<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:16;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.80<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.79<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:17;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT-SO-1M</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.88<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:18;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>BERT-SO-1M-large</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.93<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.94<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:19;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>DistilRoBERTa</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.92<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.92<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:20;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>StackOBERTflow</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.93<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.94<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:21;height:1.25pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>ALBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.79<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.74<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:1.25pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:22;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>XLNet<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.75<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.81<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.78<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:23;height:15.3pt'>
  <td colspan=2 rowspan=2 valign=top style='border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Review Responses Automatic Generation<o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt'><span lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.24<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:15.3pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:24;height:7.1pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.57</span></b><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:25;mso-yfti-lastrow:yes;height:7.1pt'>
  <td colspan=2 valign=top style='border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Link prediction<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.97<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.99<o:p></o:p></span></b></p>
  </td>
 </tr>
</table>

</div>

### 4.3 Interaction tasks among PL and NL

Interaction tasks among PL and NL are the tasks to process the pairs of PL and NL datasets in SE, such as code summarization, code generation, code review, and code search tasks. We present the these tasks and their current performance in the followed table. 

<div align=center>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-padding-alt:0cm 5.4pt 0cm 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes;height:8.5pt'>
  <td valign=top style='border:solid windowtext 1.0pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>NL+PL<o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PTMs<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Accuracy<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Precision<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Recall<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>F1<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>BLEU<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeBLEU<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>EM<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Pass@k<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>MRR<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>ROUGE<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:solid windowtext 1.0pt;border-left:none;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>METEOR<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;height:8.5pt'>
  <td rowspan=11 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Summarization<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5-base<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.20<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5-small<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.19</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>UniXcoder<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.19<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.18<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>RoBERTa</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.17<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>Codex<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.20<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>TreeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.46<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.34<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.39<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.48<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.57<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.27<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>SPT-Code<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.49<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.58<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.32<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CugLM<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.46<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.56<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.26<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.36<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.25<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.30<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.45<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.55<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.26<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>GraphCodeBERT</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.46<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.57<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.27<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12;height:8.5pt'>
  <td rowspan=9 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Generation<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5-base<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.41<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.43<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.22<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5-small<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.38<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.41<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;mso-bidi-font-weight:bold'>0.22<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.37<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.39<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.19<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:15;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>GPT-2</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.25<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.30<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.17<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:16;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>CodeGPT-2</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.29<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.33<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.18<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:17;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>StructCoder<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.41<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.45<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.22<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:18;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>UniXcoder<span style='color:black;
  background:white'><o:p></o:p></span></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.38<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.23<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:19;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CommitBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.59<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.30<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:20;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>Codex<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.29,<o:p></o:p></span></b></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.47,<o:p></o:p></span></b></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.72</span></b><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:21;height:8.5pt'>
  <td rowspan=2 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Review<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>T5<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.74<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.79<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.66<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.72<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.82</span></b><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:22;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeT5<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.67<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.70<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.59<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.64<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:23;height:8.5pt'>
  <td rowspan=12 valign=top style='border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>Code Search<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>RoBERTa(code)<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.62<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:24;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>RoBERTa</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.60<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:25;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>InferCode<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.57<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:26;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.69<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:27;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>GraphCodeBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.71<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:28;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PLBART<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.69<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:29;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CodeRetriever<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.42<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:30;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CODE-MVP<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.54<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:31;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>SPT-Code</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.70<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:32;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SynCoBERT<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.74<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:33;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>SCodeR<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.77<o:p></o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:34;mso-yfti-lastrow:yes;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>UniXcoder<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>0.74<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
</table>

</div>

### 4.4 CV-related tasks

CV-related tasks are the tasks to process the software artifacts with the image as input in SE. At present, researchers in SE have applied the PTMs into the classification of UML diagrams. 

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-top-alt:solid black 1.0pt;
 mso-border-bottom-alt:solid black 1.0pt;mso-border-insideh:1.0pt solid black'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes;height:8.5pt'>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>CV<o:p></o:p></span></p>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>PTMs<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:solid black 1.0pt;border-left:none;
  border-bottom:solid black 1.0pt;border-right:none;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>Accuracy</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;mso-yfti-lastrow:yes;height:8.5pt'>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt'>UML diagram Classification<o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'>VGG-16</span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border:none;border-bottom:solid black 1.0pt;mso-border-top-alt:
  solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><b><span
  lang=EN-US style='font-size:6.5pt'>0.50</span></b><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
 </tr>
</table>

## Notes:
Check out our paper for more information: Research Progress of Pre-trained models in Software Engineering.

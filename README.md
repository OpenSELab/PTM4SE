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

<table class="MsoNormalTable" border="0" cellspacing="0" cellpadding="0" width="501" style="width:375.65pt;border-collapse:collapse">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt">
  <td width="33" valign="top" style="width:25.0pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Type</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="90" valign="top" style="width:67.15pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Dataset</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Programming
  Language</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Source</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Scale</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Open Time</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">PTMs</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:7.1pt">
  <td width="33" rowspan="6" valign="top" style="width:25.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL<o:p></o:p></span></p>
  </td>
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/salesforce/CodeT5"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeSearchNet+C/C# datasets</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Ruby<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">JavaScript<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GO<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Python<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PHP<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C#<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub+BigQuery<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">8.35G<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeT5<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub C
  language repositories<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">5.8 G<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C-BERT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java and
  TypeScript datasets<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">TypeScript<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CugLM<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java
  datases&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SynFix<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/Kawser-nerd/CLCDSA/"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CLCDSA dataset</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C/C++<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">AtCoder+CodeJam<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">17.6M<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">IR-BERT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://s3.amazonaws.com/code2vec/data/java14m_data.tar.gz"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java datasets</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">&nbsp;<o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">32G<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">InferCode<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code2vec<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:7.1pt">
  <td width="33" rowspan="2" valign="top" style="width:25.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">NL<o:p></o:p></span></p>
  </td>
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/smartshark/seBERT/tree/main/data"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SE textual data</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Stack Overflow<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Jira<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">119.7G<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">seBERT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://aclanthology.org/attachments/2020.acl-main.443.Dataset.zip"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CoNLL-2003</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Stack Overflow<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">3.16M<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BERTOverflow<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CosSensBERT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:7.1pt">
  <td width="33" rowspan="4" valign="top" style="width:25.0pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">NL+<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL<o:p></o:p></span></p>
  </td>
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://zenodo.org/record/5387856#.Y1TB2nZByUl"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java datasets from
  CodeSearchNet+SO posts</span></a></span><span lang="EN-US" style="font-size:
  9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub+SO<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">52.5M<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2022<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">T5<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java datasets from
  CodeSearchNet+SO posts</span></a></span><span lang="EN-US" style="font-size:
  9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1.5M<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">T5<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/wasiahmad/PLBART"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java and Python from
  BigQuery+SO posts</span></a></span><span lang="EN-US" style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Python<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">BigQuery+GitHub<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">655G<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PLBART<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;mso-yfti-lastrow:yes;height:7.1pt">
  <td width="90" valign="top" style="width:67.15pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/github/CodeSearchNet"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeSearchNet</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="104" valign="top" style="width:77.95pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Ruby<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">JavaScript<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GO<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Python<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PHP<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="85" valign="top" style="width:63.8pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">GitHub<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">3.5 G<o:p></o:p></span></p>
  </td>
  <td width="47" valign="top" style="width:35.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">T-BERT<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Graphcodebert<o:p></o:p></span></p>
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeBERT<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

### 3.2 SE-related Downstream Task Dataset

SE-related downstream task datasets are the datasets used to fine tune the intellignet DL models for the se-related downstream tasks. Common SE-related downstream datasets frequently used are listed in the followed table.

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" width="581" style="width:435.4pt;border-collapse:collapse;border:none;mso-border-top-alt:
 solid black 1.0pt;mso-border-bottom-alt:solid black 1.0pt;mso-border-insideh:
 1.0pt solid black">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:7.1pt">
  <td width="39" valign="top" style="width:29.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Type</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="65" valign="top" style="width:48.5pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Tasks</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Dataset</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Programming
  Language</span><span lang="EN-US" style="font-size:9.0pt"><o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Scale</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border-top:solid black 1.0pt;
  border-left:none;border-bottom:solid black 1.0pt;border-right:none;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;color:#24292F;background:white">Open Time</span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:7.1pt">
  <td width="39" rowspan="12" valign="top" style="width:29.5pt;border:none;
  border-bottom:solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;
  padding:5.0pt 5.0pt 5.0pt 5.0pt;height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL<o:p></o:p></span></p>
  </td>
  <td width="65" rowspan="5" valign="top" style="width:48.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Classification<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/TruX-DTF/DL4PatchCorrectness"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java patches</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">102041<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">POJ104<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">C/C++<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">30815<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeCloneBench<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">901028<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2014<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/maldonado/tse.satd.data/tree/master/dataset"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SATD dataset</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2016<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/smartbugs/smartbugs-wild"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SmartBugs Wild Dataset</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">47398<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:7.1pt">
  <td width="65" rowspan="3" valign="top" style="width:48.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Program Repair<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/EhsanMashhadi/MSR2021-ProgramRepair/tree/main/data"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">ManySStuBs4J</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">63923<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Automatic Bug Fixing</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">46680<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://drive.google.com/file/d/1CtfnYaVf-q6FZP5CUM4Wh7ofpp8b9ajW/view"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">TFix-dataset</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">JavaScript<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">104804<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:7.1pt">
  <td width="65" rowspan="2" valign="top" style="width:48.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Completion<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java and
  TypeScript datasets<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/TypeScript<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/google-research-datasets/eth_py150_open"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">ETH Py150 corpus</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Python<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">74749<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:7.1pt">
  <td width="65" valign="top" style="width:48.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">API Recommendation<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Req2Lib-dataset<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">5625<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;height:7.1pt">
  <td width="65" valign="top" style="width:48.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Translation<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/microsoft/CodeXGLUE"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeTrans</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java/C#<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">10300<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13;height:7.1pt">
  <td width="39" rowspan="6" valign="top" style="width:29.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">NL<o:p></o:p></span></p>
  </td>
  <td width="65" rowspan="4" valign="top" style="width:48.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Text Classification<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="http://www.st.cs.uni-saarland.de/softevo/bugclassify/"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Herzig's issue report
  datasets</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2012<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://zenodo.org/record/4266643#.X6vERuLPxPY"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Commit messages</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1793<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:15;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://bitbucket.org/jstzwj/lms4githubissue/src/master/data_view.7z"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">issue report from GitHub</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:16;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/SEntiMoji/SEntiMoji"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">SEntiMoji dataset</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">10,096<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:17;height:7.1pt">
  <td width="65" valign="top" style="width:48.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Review Responses
  Automatic Generation<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">review-response
  pairs datasets<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">570881<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:18;height:7.1pt">
  <td width="65" valign="top" style="width:48.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Link Prediction<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://zenodo.org/record/4511291#.YB3tjyj0mbg"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">traceability dataset</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">English<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1834<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:19;height:7.1pt">
  <td width="39" rowspan="5" valign="top" style="width:29.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">PL+NL<o:p></o:p></span></p>
  </td>
  <td width="65" rowspan="3" valign="top" style="width:48.5pt;border:none;border-bottom:
  solid black 1.0pt;mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Summarization<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/senticr/SentiCR/"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code review comments (CR)</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1600<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2017<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:20;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://drive.google.com/drive/folders/1uJv-kljY1Q59fa-TdkpXOOd9QEG5OZDa?usp=sharing"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Summarization(CS)</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">1953940<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2020<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:21;height:7.1pt">
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/github/CodeSearchNet"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeSearchNet</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Ruby/JavaScript/GO/Python/Java/PHP<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2019<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:22;height:7.1pt">
  <td width="65" valign="top" style="width:48.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Code Generation<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://drive.google.com/drive/folders/1kC6fe7JgOmEHhVFaXjzOmKeatTJy1I1W"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Concode data</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Java<o:p></o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">100,000<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2018<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:23;height:7.1pt">
  <td width="65" valign="top" style="width:48.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">Synthesis<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US"><a href="https://github.com/microsoft/CodeXGLUE"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CodeXGLUE</span></a></span><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2021<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:24;mso-yfti-lastrow:yes;height:7.1pt">
  <td width="39" valign="top" style="width:29.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">CV<o:p></o:p></span></p>
  </td>
  <td width="65" valign="top" style="width:48.5pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">UML Diagram Classification<o:p></o:p></span></p>
  </td>
  <td width="151" valign="top" style="width:4.0cm;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">UML Diagram<o:p></o:p></span></p>
  </td>
  <td width="94" valign="top" style="width:70.85pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="57" valign="top" style="width:42.55pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">14815<o:p></o:p></span></p>
  </td>
  <td width="66" valign="top" style="width:49.6pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-top-alt:solid black 1.0pt;padding:5.0pt 5.0pt 5.0pt 5.0pt;
  height:7.1pt">
  <p style="mso-line-height-alt:.9pt;mso-pagination:widow-orphan"><span lang="EN-US" style="font-size:9.0pt;mso-bidi-font-size:10.0pt">2016<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeBLEU</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>EditSIM</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  lang=EN-US style='font-size:6.5pt'>Commit <span class=SpellE>classifcation</span><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>seBERT</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>BERToverflow</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeBERT</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>RoBERTa</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>StackOBERTflow</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>GraphCodeBERT</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CuBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>CodeBERT</span></span><span lang=EN-US style='font-size:6.5pt;
  color:black;background:white'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CuBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>RoBERTa</span></span><span lang=EN-US style='font-size:6.5pt;
  color:black;background:white'> (code)</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>CodeBERT</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>CodeBERTa</span></span><span lang=EN-US style='font-size:6.5pt;
  color:black;background:white'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>GraphCodeBERT</span></span><span lang=EN-US style='font-size:6.5pt;
  color:black;background:white'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>SynCoBERT</span></span><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>RoBERTa</span></span><span
  lang=EN-US style='font-size:6.5pt'>&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'>&nbsp;<o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>GraphCodeBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>RoBERTa</span></span><span lang=EN-US style='font-size:6.5pt;
  color:black;background:white'> (code)</span><span lang=EN-US
  style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>InferCode</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>SynCoBERT</span></span><span
  lang=EN-US style='font-size:6.5pt;color:black;background:white'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>SCodeR</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>UniXcoder</span></span><span lang=EN-US style='font-size:6.5pt;
  color:black;background:white'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>RoBERTa</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>RoBERTa</span></span><span
  lang=EN-US style='font-size:6.5pt'> (code)<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>GraphCodeBERT</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CuBERT</span></span><span
  lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>CodeBERTa</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CugLM</span></span><span
  lang=EN-US style='font-size:6.5pt'>&nbsp;<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>UniXcoder</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>TreeBERT</span></span><span
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
 <tr style='mso-yfti-irow:67;height:8.5pt'>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p style='mso-line-height-alt:.9pt;mso-pagination:widow-orphan'><span
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>GraphCodeBERT</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>RoBERTa</span></span><span
  lang=EN-US style='font-size:6.5pt'> (code)<o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CodeBERT</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>SynCoBERT</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>StructCoder</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>TreeBERT</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt'>CugLM</span></span><span
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>GraphCodeBERT</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:8.5pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan;
  vertical-align:top'><span lang=EN-US style='font-size:6.5pt;font-family:"Times New Roman",serif'><o:p>&nbsp;</o:p></span></p>
  </td>
  <td valign=top style='border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .5pt;
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>CodeBERTa</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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
  class=SpellE><span lang=EN-US style='font-size:6.5pt;color:black;background:
  white'>CodeBERT</span></span><span lang=EN-US style='font-size:6.5pt'><o:p></o:p></span></p>
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

<div  align=center>
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
</div>

### 4.3 Interaction tasks among PL and NL

Interaction tasks among PL and NL are the tasks to process the pairs of PL and NL datasets in SE, such as code summarization, code generation, code review, and code search tasks. We present the these tasks and their current performance in the followed table. 

<div align=center>
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
</div>

### 4.4 CV-related tasks

CV-related tasks are the tasks to process the software artifacts with the image as input in SE. At present, researchers in SE have applied the PTMs into the classification of UML diagrams. 

<div align=center>
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
</div>

## Notes:
Check out our paper for more information: Research Progress of Pre-trained models in Software Engineering.

https://arxiv.org/pdf/1805.05236.pdf

## existing industrial and open-source tools:
QiHoo360 [17], AndroBugs [2], MobSF [13], and QARK [16].

## SOTA limitations

* current studies lack a baseline of sensitive datarelated security weaknesses specific to the core functionality of banking apps to ensure an overall assessment of these apps; 

* the current off-the-shelf services (e.g., Qihoo360 [17]) and open-source tools (e.g., AndroBugs [2]) use syntax-based scanning to perform a security check during app development, which would incur a large number of false positives (e.g., non-sensitive data printed in the log file). 

* Besides, these tools focus on generic categories of apps, not specific to banking apps. 

Even when the weaknesses, such as cryptographic misuses [42] and inappropriate SSL/TLS implementations [40, 45, 51, 65], have been reported for years, it still appears unknown why so many security weaknesses in banking apps are not yet patched [63].


## steps
1. we first collect 693 banking apps across 83 countries from various markets, to our knowledge, this is the largest banking app dataset taken into study to date; 

2. to collect the weaknesses exhibited in banking apps and complement the capability of existing tools in data-related weakness detection, we first summarize a weakness baseline and propose an automated security risk assessment system (Ausera). Ausera combines static program analysis techniques and sensitive keyword identification, to identify such weaknesses (cf. Section 2). 

3. By applying Ausera, we collected 2,157 security weaknesses in the 693 banking apps, and further conduct a comprehensive empirical study (cf. Section 3) to investigate the ecosystem of banking apps in terms of security weaknesses, aiming to answer the following research questions:

## RQ
* RQ1: What is the current status of existing tools towards
collecting reliable data-related weaknesses in banking apps
compared with Ausera?

* RQ2: What is the overall security status of banking apps in
terms of data-related weaknesses?

* RQ3: What is the weakness status of banking apps globally
w.r.t. economies and regulations?

* RQ4: How are weaknesses introduced during app evolution
and fragmentation?

* RQ5: What is the gap between academic researchers and
banks in understanding and fixing weaknesses?

## Take away

* Note that, to avoid missing variants of the keywords, we
further employ Word2vec [57] to supplement the corpus of the
keyword database.

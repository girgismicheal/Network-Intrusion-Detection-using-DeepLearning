# Network-Intrusion-Detection-using-DeepLearning
## Problem’s overview
With the expanded applications of modern-day networking, network infrastructures are at risk from cyber-attacks and intrusions. Multiple datasets have been proposed in the literature that can be used to create Machine Learning (ML) based Network Intrusion Detection Systems (NIDS). However, many of these datasets suffer from sub-optimal performance and do not adequately and effectively represent all types of intrusions.  Another problem with these datasets is the low accuracy of tail classes. To address these issues,  we propose the University of Nevada - Reno Intrusion Detection Dataset (UNR-IDD) that provides researchers with a wider range of samples and scenarios.
![image](https://drive.google.com/uc?export=view&id=12F5nT5UPD-PQWMy23u6iVmP36EEF2gqC)
<br>
**Note: This is a real world problem you can check link from more information and how the University of Nevada, Reno collect the data**
https://www.tapadhirdas.com/unr-idd-dataset

### Multi-class Classification
The goal of multi-class classification is to differentiate the intrusions not only from normal working conditions but also from each other. Multi-class classification helps us to learn about the root causes of network intrusions. The labels for multi-class classification in UNR-IDD are illustrated in the accompanying table.

| Label	      | Description                   |
| ----------- | -----------                   |
|Normal       |	Network Functionality.|
|TCP-SYN      |	TCP-SYN Flood.                |
|PortScan     |	Port Scanning.                |
|Overflow     |	Flow Table Overflow.          |
|Blackhole    |	Blackhole Attack.             |
|Diversion    |	Traffic Diversion Attack.     |

## The Project Methodology
The figure below shows our project pipeline.
![image](https://drive.google.com/uc?export=view&id=1mMgQzvgfCqGYUnkptkJ_Ahh3fRBPgMde)
## Results:
**BaseLine Model Accurancy

### Batch size

|                 | Min\_train\_acc | Max\_train\_acc | AVG\_train\_acc | Min\_test\_acc | Max\_test\_acc | AVG\_test\_acc        | Min\_valid\_acc | Max\_valid\_acc | AVG\_valid\_acc |
|-----------------| --------------- | --------------- | --------------- | -------------- | -------------- |-----------------------| --------------- | --------------- | --------------- |
| 32              | 0.758687        | 0.788087        | 0.769378        | 0.755793       | 0.778966       | 0.770053              | 0.755793        | 0.782531        | 0.765419        |
| <mark>64</mark> | 0.756014        | 0.76785         | 0.762047        | 0.755793       | 0.784314       | <mark>0.773262</mark> | 0.721925        | 0.754011        | 0.745098        |
| 128             | 0.757159        | 0.781214        | 0.769454        | 0.757576       | 0.780749       | 0.768627              | 0.748663        | 0.795009        | 0.77041         |


### Activation Functions Vs Neurons

**1 Hidden Layer**

| Neurons  | Min\_train\_acc | Max\_train\_acc | AVG\_train\_acc | Min\_test\_acc | Max\_test\_acc | AVG\_test\_acc | Min\_valid\_acc | Max\_valid\_acc | AVG\_valid\_acc |
|----------| --------------- | --------------- | --------------- | -------------- | -------------- | -------------- | --------------- | --------------- | --------------- |
| 10       | 0.752577        | 0.772432        | 0.763727        | 0.754011       | 0.777184       | 0.768984       | 0.730838        | 0.775401        | 0.752941        |
| 20       | 0.769378        | 0.78236         | 0.775105        | 0.768271       | 0.789661       | 0.781105       | 0.759358        | 0.791444        | 0.773975        |
| 30       | 0.775105        | 0.796105        | 0.784422        | 0.778966       | 0.818182       | 0.802139       | 0.773619        | 0.798574        | 0.785383        |
| 40       | 0.777396        | 0.802215        | 0.788698        | 0.775401       | 0.807487       | 0.793583       | 0.770053        | 0.798574        | 0.788235        |

**2 Hidden Layer**

| Neurons  | Min\_train\_acc | Max\_train\_acc | AVG\_train\_acc | Min\_test\_acc | Max\_test\_acc | AVG\_test\_acc | Min\_valid\_acc | Max\_valid\_acc | AVG\_valid\_acc |
|----------| --------------- | --------------- | --------------- | -------------- | -------------- | -------------- | --------------- | --------------- | --------------- |
| 10       | 0.766705        | 0.783123        | 0.777854        | 0.775401       | 0.800357       | 0.78574        | 0.746881        | 0.777184        | 0.768627        |
| 20       | 0.780069        | 0.786942        | 0.784422        | 0.782531       | 0.802139       | 0.7918         | 0.770053        | 0.793226        | 0.780036        |
| 30       | 0.783887        | 0.79496         | 0.79076         | 0.793226       | 0.816399       | 0.802852       | 0.780749        | 0.793226        | 0.78574         |
| 40       | 0.789996        | 0.809851        | 0.799771        | 0.798574       | 0.827094       | 0.810695       | 0.782531        | 0.809269        | 0.795722        |

**4 Hidden Layer**

| Neurons  | Min\_train\_acc | Max\_train\_acc | AVG\_train\_acc | Min\_test\_acc | Max\_test\_acc | AVG\_test\_acc | Min\_valid\_acc | Max\_valid\_acc | AVG\_valid\_acc |
|----------| --------------- | --------------- | --------------- | -------------- | -------------- | -------------- | --------------- | --------------- | --------------- |
| 10       | 0.765559        | 0.791905        | 0.779305        | 0.764706       | 0.800357       | 0.783957       | 0.775401        | 0.787879        | 0.783957        |
| 20       | 0.779305        | 0.807178        | 0.793127        | 0.784314       | 0.821747       | 0.804635       | 0.770053        | 0.809269        | 0.792513        |
| 30       | 0.803742        | 0.832761        | 0.815426        | 0.803922       | 0.825312       | 0.814617       | 0.787879        | 0.83779         | 0.812478        |
| 40       | 0.800305        | 0.831233        | 0.818175        | 0.805704       | 0.83779        | 0.823173       | 0.800357        | 0.818182        | 0.808913        |

<mark>**8 Hidden Layer**</mark>

| Neurons         | Min\_train\_acc | Max\_train\_acc | AVG\_train\_acc | Min\_test\_acc | Max\_test\_acc | AVG\_test\_acc        | Min\_valid\_acc | Max\_valid\_acc | AVG\_valid\_acc |
|-----------------| --------------- | --------------- | --------------- | -------------- | -------------- |-----------------------| --------------- | --------------- | --------------- |
| 10              | 0.680794        | 0.76365         | 0.734555        | 0.7041         | 0.777184       | 0.748307              | 0.68984         | 0.762923        | 0.739394        |
| 20              | 0.771287        | 0.835815        | 0.804811        | 0.762923       | 0.819964       | 0.748307              | 0.780749        | 0.816399        | 0.804991        |
| 30              | 0.799542        | 0.818633        | 0.811531        | 0.798574       | 0.836007       | 0.818538              | 0.802139        | 0.821747        | 0.810695        |
| <mark>40</mark> | 0.806796        | 0.827797        | 0.817717        | 0.800357       | 0.84492        | <mark>0.824599</mark> | 0.807487        | 0.825312        | 0.814617        |


### Optimizer

| Optimizer                     | Min\_train\_acc | Max\_train\_acc | AVG\_train\_acc       | Min\_test\_acc | Max\_test\_acc | AVG\_test\_acc        | Min\_valid\_acc | Max\_valid\_acc | AVG\_valid\_acc |
|-------------------------------| -------- | -------- |-----------------------| -------- | -------- |-----------------------| -------- | -------- | -------- |
| AdamW\_lr\_0.1                | 0.254296 | 0.369225 | 0.277281              | 0.226381 | 0.397504 | 0.260606              | 0.251337 | 0.331551 | 0.26738  |
| AdamW\_lr\_0.01               | 0.669721 | 0.791142 | 0.758381              | 0.688057 | 0.803922 | 0.77148               | 0.684492 | 0.805704 | 0.76934  |
| <mark>AdamW\_lr\_0.001</mark> | 0.797633 | 0.818251 | <mark>0.809927</mark> | 0.791444 | 0.828877 | <mark>0.810695</mark> | 0.802139 | 0.823529 | 0.814973 |
| SGD\_m\_0.1\_lr\_0.1          | 0.747614 | 0.783123 | 0.759832              | 0.764706 | 0.789661 | 0.77148               | 0.754011 | 0.782531 | 0.766845 |
| SGD\_m\_0.1\_lr\_0.01         | 0.731195 | 0.758687 | 0.744635              | 0.723708 | 0.762923 | 0.753298              | 0.73262  | 0.766488 | 0.749376 |
| SGD\_m\_0.1\_lr\_0.001        | 0.693394 | 0.746468 | 0.716991              | 0.698752 | 0.773619 | 0.735116              | 0.686275 | 0.759358 | 0.718004 |
| SGD\_m\_0.5\_lr\_0.1          | 0.691867 | 0.789614 | 0.759756              | 0.7041   | 0.807487 | 0.768627              | 0.695187 | 0.795009 | 0.766132 |
| SGD\_m\_0.5\_lr\_0.01         | 0.775487 | 0.804124 | 0.789309              | 0.773619 | 0.802139 | 0.790374              | 0.766488 | 0.809269 | 0.792513 |
| SGD\_m\_0.5\_lr\_0.001        | 0.745323 | 0.761741 | 0.752348              | 0.752228 | 0.770053 | 0.759002              | 0.752228 | 0.768271 | 0.756506 |
| SGD\_m\_0.9\_lr\_0.1          | 0.620084 | 0.744177 | 0.703475              | 0.631016 | 0.762923 | 0.716221              | 0.631016 | 0.759358 | 0.713725 |
| SGD\_m\_0.9\_lr\_0.01         | 0.768614 | 0.80756  | 0.795036              | 0.768271 | 0.814617 | 0.801426              | 0.778966 | 0.816399 | 0.802496 |
| SGD\_m\_0.9\_lr\_0.001        | 0.768996 | 0.793051 | 0.785185              | 0.775401 | 0.802139 | 0.790018              | 0.768271 | 0.800357 | 0.788235 |
| RMSprop\_lr\_0.1              | 0.247805 | 0.468118 | 0.332264              | 0.226381 | 0.508021 | 0.347237              | 0.251337 | 0.449198 | 0.330838 |
| RMSprop\_lr\_0.01             | 0.723177 | 0.771287 | 0.741733              | 0.736185 | 0.786096 | 0.757932              | 0.743316 | 0.786096 | 0.760428 |
| RMSprop\_lr\_0.001            | 0.771287 | 0.808706 | 0.787247              | 0.773619 | 0.812834 | 0.790731              | 0.768271 | 0.812834 | 0.787166 |

### Activation Function

|                          | Min\_train\_acc | Max\_train\_acc | AVG\_train\_acc | Min\_test\_acc | Max\_test\_acc | AVG\_test\_acc       | Min\_valid\_acc | Max\_valid\_acc | AVG\_valid\_acc |
|--------------------------| --------------- | --------------- | --------------- | -------------- | -------------- |----------------------| --------------- | --------------- | --------------- |
| Relu                     | 0.80718         | 0.82818         | 0.8155          | 0.80927        | 0.83066        | 0.8164               | 0.79679         | 0.81996         | 0.8107          |
| <mark>Leaky\_relu</mark> | 0.804124        | 0.82054         | 0.81191         | 0.80392        | 0.84136        | <mark>0.81854</mark> | 0.80392         | 0.823529        | 0.81177         |
| Sigmoid                  | 0.2543          | 0.57427         | 0.44162         | 0.22638        | 0.61497        | 0.44385              | 0.25134         | 0.61141         | 0.46631         |
| Tanh                     | 0.79572         | 0.80298         | 0.80046         | 0.79857        | 0.81283        | 0.80535              | 0.80927         | 0.827094        | 0.8189          |


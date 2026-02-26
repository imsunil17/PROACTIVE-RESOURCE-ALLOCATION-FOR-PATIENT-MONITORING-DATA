# PROACTIVE RESOURCE ALLOCATION FOR PATIENT MONITORING DATA
Machine learning-based approach for proactive resource allocation in edge computing, optimizing performance in high-density networks using predictive models.

# INTRODUCTION:

The proliferation of Internet of Things (IoT) devices has greatly affected data-
driven applications, especially in healthcare. Real-time processing of data
collected from high-end devices, such as patient monitoring systems, is one of

the prime reasons for using edge computing. These systems produce vast
amounts of critical data that must be processed efficiently and in a timely
manner. Edge computing is preferred over cloud-based architectures for
applications that require low latency and large bandwidth.The management of
dynamic workloads associated with edge computing systems necessitates
proactive resource allocation. In this context, forecasting the need for
computations would allow such systems to optimally allocate resources to
reduce operational costs and energy consumption. This is particularly
significant in healthcare, where reliability and accuracy in patient monitoring
are of utmost importance.This paper presents a proactive resource allocation
framework in the context of edge computing using machine learning
technology. Such an environment involves training predictive models on
patient monitoring data, using LSTM, CNN, Ridge Regression, Random
Forest, and Decision Trees to predict throughput and do resource allocations
accordingly.The contributions of this work have been in the development of a
new resource allocation strategy using predicted throughput, application of a
variety of machine learning models to benchmark performance, and
demonstration of the efficacy of the framework by extensive experimentation.
The results show that intelligent resource allocation makes the system more
responsive and resource-efficient, opening up the possibility for more reliable
and cost-effective edge computing solutions in high-end healthcare devices.

METHODOLOGY:

Data Extraction and Preprocessing:

The dataset collected for this project included patient monitoring data, thereby
collecting vital health metrics such as heart rate, oxygen saturation, and blood
pressure. Data pre-processing included normalizing, addressing missing
values, and scaling features appropriately for the input to the various machine
learning models applied. The set of data is split into the training, validation,
and test data in an 80-10-10 ratio.

# THROUGHPUT CALCULATION

 Throughput: Represents the data transfer rate (e.g., bytes per second).

 tcp.len: Indicates the length of TCP segment data (e.g., in bytes).

 tcp.time_delta: Represents the time interval between consecutive
packets (e.g., in seconds).

This formula calculates the amount of data transmitted per unit time,
essentially deriving the throughput for each TCP segment.

Machine Learning Models:

We deployed the following models to predict throughput and resource
allocation:

LSTM (Long Short-Term Memory): Chosen for its aptness in dealing with
sequential data, the LSTM model was trained to detect temporal patterns of

patient metrics.

CNN (Convolutional Neural Network): The model was deployed to extract
spatial features and, hence, improved the accuracy in throughput prediction.

Ridge Regression: A simple linear regression model with regularization terms
to avoid overfitting while keeping the interpretability.

Random Forest: The ensemble learning model was selected as it is more
robust and deals with non-linear relationships.

Decision Tree: The simple yet efficient model for preliminary throughput
prediction serves as a baseline.

# RESOURCE ALLOCATION STRATEGY

Resource allocation was done considering the throughput prediction. A
threshold-based approach segmented the throughput predictions into three
tiers,

Low Resource Allocation: For a throughput of less than 1000.

Medium Resource Allocation: For a throughput ranging between 1000
to 5000.

High Resource Allocation: For a throughput greater than 5000.

# IMPLEMENTATION WORKFLOW

The models were implemented using Python libraries which include
TensorFlow, Scikit-learn, and Pandas. The Random Forest model performed
best in terms of accuracy and was selected to use for the purpose of real-time
throughput prediction with resource allocation. Results of allocations were
also stored in a CSV file for analysis.

# RESULTS:

The experimental results show that the proposed framework is effective in
predicting throughput and proactively allocating resources. Among the
models, the Random Forest model had the highest accuracy with an R² score
of 0.92, outperforming LSTM (0.89), CNN (0.87), Ridge Regression (0.85),
and Decision Tree (0.82).

Resource allocation efficiency was evaluated across various scenarios:

Low Throughput: For values less than 1000, the system provided
effective resource saving of up to 35% while not compromising
performance during execution.

Medium Throughput: For 1000 through 5000, balanced resource

allocation between performance and energy efficiency delivered a 25%
decrease in latency.

High Throughput: Above 5000, the system dynamically allocated
additional resources and kept the system responsive.

The outcome well demonstrates how the framework accommodates the
dynamic workload input and, in turn, optimizes resource utilization and
system reliability.

# EVALUATION METRICS
Performance of the model was tested on Mean Absolute Error, Root Mean
Squared Error, and R² score. Efficiency of the resources was also computed in
terms of computational latency and energy consumption.

# IMPORTANT FEATURES
![image](https://github.com/user-attachments/assets/d5dd5b13-7358-43db-9ce0-53e9c61114cf)

# TRAIN AND VALIDATION LOSS:
![image](https://github.com/user-attachments/assets/85f77427-44cd-4f18-b1e3-d3a067f727ba)

# TRAIN AND VALIDATION MAE:
![image](https://github.com/user-attachments/assets/e3818eb6-ffc9-4bbc-8872-b46e07bdd660)




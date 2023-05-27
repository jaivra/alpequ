# Alpequ - Algorithms Performance Quantifier

Alpequ is a tool designed to quantify the performance of algorithms in terms of time. It provides a useful means to compare the efficiency of algorithms implemented in different programming languages and evaluate which one performs better with specific problem instances.

## Architecture

<p align="center">
 <img src="https://github.com/jaivra/alpequ/blob/main/images/alpequ_architecture.png" alt>
</p>


The core component of Alpequ is AlgorithmManager, which forms the foundation of the architecture. It is responsible for executing different algorithms, checking their results, and estimating their execution time.

For each problem X, AlgorithmManager is aware of a correct algorithm that can solve it. Various applications can declare their ability to solve the problem, and AlgorithmManager will call each one, validate the results, and calculate the execution time.

Communication between AlgorithManager and different applications is facilitated through gRPC.
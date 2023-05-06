MSSP Evaluator

PLEASE DOWNLOAD AND OPEN THE ZIP 

INTRODUCTION
The MSSP Evaluator is a tool created for helping to assess solutions for the movie scene scheduling problem (MSSP).

This tool is capable of evaluating multiple solutions paired with multiple instances at a given time.  

There are three input files that the evaluator takes: config, inputs and sols. The config file should contain four lines of text as follows:

inputs.txt
sols.txt
verbose:true
record:true

The first line is the name of the file containing all the instances that you want to evaluate. The second contains the solutions that you want to evaluate. Each instance is directly paired to its corresponding solution. That is, instance 0 will receive solution 0.

The third line is the verbose option. Set this to true if you wish to see a component breakdown of the costs of the provided solution. By default, this is set to false.

The final line is the record option. Set this to true if you want the program to create a text file record of the results of the evaluations. By default it is set to false.


FILE FORMATS
The input files must confirm to the file format as provided in the readme located in the benchmark dataset. 

The solutions in the solution file must be comma delimited. Remember that the scenes are numerically named, with the first scene being 0, and the last being n-1, where n is the number of scenes. NB! This numbering is just the label associated with the scene. It is not actually indicative of the scene's order. The order is given by the index of the scene in the actual solution. For example:

3,2,0,1 

The first scene in this order is scene 3. Scene 0 is located at index 2, making it the third scene in the production schedule.


USING THE EVALUATOR
To run the evaluator from the command line, type the following:

java -jar "msspEvaluator.jar" 

This will run the evaluator and provide you with the results of your solutions.


REQUIREMENTS
This program was created using Java version 1.8.0. It should work with later versions of Java as well.

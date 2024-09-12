# Brief code explanation for the project GastroFLOW

All codes are written in Python, and the project is mainly divided into the following parts: `Color normalization`, `Data process`, `Machine learning` and `MLP learning`. You can find the corresponding code in the `working` folder.

## Color normalization
  
`ChromaCalculate`: calculate the color transform matrix between two doamains (different scanners).

`ColorNormalize`: use calculated transform matrix to carry out transformation on `WSI` file

## Data process
  
`DataAggreation`: convert feature data of Qupath program into an integrated `.csv` file 

## Machine learning
  
`MLTrainNEval`: train ML models over chosen dataset

`MLTest`: evaluate ML model on target dataset, calculate and record scores

## MLP learning
  
`MLPTrain`: train a simple MLP over chosen dataset

`MLPTest`: evaluate MLP model on target dataset, using `Case model` (case level celluar features), `Patch model` (patch level cellular features) and `GFLOW` (a blend model using both level features) to get predict results. Calculate scores and generate figures.

## P.S. 

I do not filter extra packages in the `requirements.txt`. You can create a virtual environment and install all packages in the file by running the following command:

```bash
conda create --name <envname> --file requirements.txt
```

To fluently run the ColorNormalize function, a `WSI` file is needed. But, this kind of file is too big ... so please contact me when necessary. 

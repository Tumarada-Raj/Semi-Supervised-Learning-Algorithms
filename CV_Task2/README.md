Instructions to reproduce reported results.

* Given below are the commands to reproduce the results for each specific dataset with corresponing labels:
* The code base for this task is by default set to give the respective error rate in %
* You need to run the repective commands sequentially and uncomment the respective test_error() functionality in the main.py file
* The pre-trained models are stored in ./models

NOTE: If you want to check the train functionality please uncomment the train() in the main.py. The models after training will be stored in ./models/obs(This path is different from the pre-trained models to avoid the overriding of models)


# CIFAR 10
## 4000 labels
best_model_cifar10_4000_0.6_8.pt - error rate 21.77%
-----------------------------------------------------

python "./main.py" --dataset cifar10 --num-labeled 4000 --num-validation 1000 --lr 0.03 --momentum 0.9 --wd 0.001 --train-batch 64 --total-iter 102400 --iter-per-epoch 1024 --max-grad-norm 1 --vat-xi 0.6 --vat-eps 8 --vat-iter 1 --modelpath "./models/obs/"

## 250 labels
best_model_cifar10_250_0.6_8.pt - error rate 52.75%
----------------------------------------------------

python "./main.py" --dataset cifar10 --num-labeled 250 --num-validation 1000 --lr 0.03 --momentum 0.9 --wd 0.001 --train-batch 64 --total-iter 102400 --iter-per-epoch 1024 --max-grad-norm 1 --vat-xi 0.6 --vat-eps 8 --vat-iter 1 --modelpath "./models/obs/"

# CIFAR 100
## 10000 labels
best_model_cifar100_10000_0.6_8.pt - error rate 51.23%
------------------------------------------------------

python "./main.py" --dataset cifar100 --num-labeled 10000 --num-validation 1000 --lr 0.03 --momentum 0.9 --wd 0.001 --train-batch 64 --total-iter 102400 --iter-per-epoch 1024 --max-grad-norm 1 --vat-xi 0.6 --vat-eps 8 --vat-iter 1 --modelpath "./models/obs/"

## 2500 labels
best_model_cifar100_2500_0.6_8.pt - error rate 66.81%
------------------------------------------------------

python "./main.py" --dataset cifar100 --num-labeled 4000 --num-validation 1000 --lr 0.03 --momentum 0.9 --wd 0.001 --train-batch 64 --total-iter 102400 --iter-per-epoch 1024 --max-grad-norm 1 --vat-xi 0.6 --vat-eps 8 --vat-iter 1 --modelpath "./models/obs/"
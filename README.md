Wasserstein GAN
===============

[[forked from]](https://github.com/martinarjovsky/WassersteinGAN)   [[Paper]](https://arxiv.org/abs/1701.07875)



### 训练

	nohup python main.py --dataset cifar --dataroot /data/tf/torch_data/cifar --cuda --ngpu 2&
	nohup python main.py --dataset lsun --dataroot /data/tf/torch_data/LSUN/data --cuda --ngpu 2&



#### WGAN的改进

* 判别器最后一层去掉 sigmoid
* 判别器与生成器的 loss 都不不取 log
* 权重截断到绝对值不超过一个小常数 c
* 训练时不用动量(包括momentum和Adam)，推荐RMSProp、SGD





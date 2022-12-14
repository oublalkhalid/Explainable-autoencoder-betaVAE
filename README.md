# Explainable-autoencoder-betaVAE

![latent space](doc/network.png)

Recently, there has been an explosion of literature related to Non-Intrusive Load Monitoring (NILM) for Grid Smart approaches based on neural networks and other advanced machine learning methods. However, while these methods offer competitive accuracy, the inner workings of these models are less clear. Understanding the output of the networks allows for improved designs, highlights relevant features and aspects of the data used to make the decision, provides better model accuracy (as a single measure of accuracy is often insufficient), and also provides an inherent level of confidence in the value of the consumption feedback provided to the NILM end user. Explainable Artificial Intelligence (XAI) aims to solve this problem by explaining these <<black boxes>>. XAI methods, developed for image and text-based methods, can in many cases interpret the outputs of complex models well, making them interpretive. However, explaining the inference of time series data remains a challenge. In this research internship, we investigate the explainability of a generative autoencoder used to disaggregate the power source of each individual device. This is indeed a blind separation, and many attempts have been made to improve such models, and they are often supervised, making these models not very tractable. Our investigation shows how the explicability of an autoencoder can contribute to solving the NILM problem. Although based on the disentanglement of the latent space, which is for a standard Variational Autoencoder (VAE) organized in an unsupervised manner. Adding constraints to this space will allow us to effectively learn the model characteristics of each machine. Furthermore, we demonstrate that if the components of this space are unorganized or correlated such as for a standard VAE (the attributes are mixed), the model becomes weak and less explainable. Moreover, the addition of contrasts in this space, notably the $D_{KL}$ regularization term with the $\beta$ factor of disentanglement, will lead us to have results competitive with the literature, and more importantly, the navigation in the latent space allows us to understand the learned attributes and consequently a high performance and confidence of the predictions. Our research work confirms that the disentanglement process is a natural requirement for explaining an autoencoder, unlike other methods that rely solely on model weight analysis.

![latent space](doc/beta_effect.png)
![latent space](doc/latent_space.gif)

## Results
![latent space](doc/related_work_vs_betaVAE.png)

## Results on UK-DALE Dataset
![latent space](doc/related_work_vs_betaVAE_ukdale.png)


## Interpolation between $z_d$ and $z_{d} + sing(z_{d})$

![latent space](doc/move_1.png)

![latent space](doc/Move_2.png)

![latent space](doc/Move_3.png)

![latent space](doc/Move_4.png)


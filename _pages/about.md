---
permalink: /
title: "Vahid Jebraeeli"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

In an era of exponentially growing AI, my work asks a critical question: **How do we achieve intelligent scale sustainably?**

I am a Machine Learning and Computer Vision researcher, and a final-year Ph.D. candidate at North Carolina State University, where I architect the next generation of generative models and foundational vision systems. My research, summarized by the title of my thesis, *"Balanced Scalability for Sustainable ML"*, is focused on building AI that is not only powerful but also profoundly efficient. I move beyond brute-force computation to create systems with elegance, precision, and a deep understanding of the data they learn from.

## My Approach: A Duality of Data Synthesis and Architectural Innovation

Today's AI demands immense datasets and computational power. My research confronts this challenge head-on by reimagining how machines learn from and generate information, focusing on two core areas:

* **Mastering the Data Lifecycle**: I build frameworks that fundamentally control the data itself. My work explores the full spectrum of data synthesis, from distillation to creation. My **"Koopcon"** model (ICIP 2024) utilizes Koopman Operator Theory and Optimal Transport to distill massive datasets into compact, potent essences, proving that smaller can be smarter. Conversely, its conceptual dual, my **"Expansive Synthesis"** framework (ICASSP 2025), can grow a rich, large-scale dataset from just a handful of samples, enabling powerful learning even when data is scarce.

* **Re-engineering Core AI Architectures**: I don't just use existing models; I redesign them from the inside out for greater control and efficiency. I am developing **ViTCAE**, a new class of Vision Transformer that repurposes the model's global `Class` token into a generative linchpin for controllable image synthesis. This work introduces a novel, dynamic attention mechanism inspired by opinion dynamics to significantly reduce computational overhead through a principled head-freezing technique. My ongoing research also explores the fusion of classical Volterra Filters with modern attention mechanisms, creating models with a far richer, multi-scale understanding of both local detail and global context.

## From Theory to Practice

My path has been one of consistent academic excellence, beginning with ranking in the top 0.3% in Iran's national university entrance exam and culminating in an M.Sc. with Distinction from the prestigious Sharif University of Technology. This rigorous theoretical grounding is balanced by hands-on industry experience, where I’ve engineered generative AI solutions for a German tech firm and deployed deep learning models for agricultural analysis with the USDA. This blend of deep theory and practical application fuels my pursuit of AI systems that are not just academically novel, but also robust, deployable, and impactful.

I believe the future of AI lies not in its size, but in its intelligence. If you share this vision, I'd love to connect.

---
* [**Email me!**](mailto:vjebrae@ncsu.edu)
* [**My LinkedIn**](https://www.linkedin.com/in/vahid-jebraeeli-2a1406102/)
---

## Featured Publications

### VITCAE: ViT-based Class-conditioned Autoencoder
![VITCAE Architecture](/images/vitcae_architecture.png)
Standard Vision Transformer (ViT) autoencoders often fail to leverage the global `Class` token for generation and use static attention mechanisms, which is inefficient. VITCAE addresses this by transforming the `Class` token into a generative controller. In this framework, the encoder maps the `Class` token to a global latent variable that sets the prior distribution for all local patch-level latents, creating a strong hierarchy where global semantics guide the synthesis of local details. Inspired by opinion dynamics, we introduce a convergence-aware temperature scheduler that adaptively anneals each attention head's influence, allowing us to freeze converged heads during training. This dynamic head-pruning mechanism significantly improves computational efficiency without sacrificing model fidelity.

### Generative Expansion of Small Datasets: An Expansive Graph Approach
![Expansive Synthesis Architecture](/images/expansive_synthesis.png)
Data scarcity is a major bottleneck in machine learning. This work introduces an "Expansive Synthesis" model designed to generate large-scale, information-rich datasets from minimal initial samples. The framework leverages the non-linear latent space of a neural network, interpreted through Koopman operator theory, to create a linearized space suitable for principled expansion. Using expander graph mappings and feature interpolation, the model generates new, diverse data points while preserving the statistical distribution and feature relationships of the original data. The distributional consistency of the newly synthesized data is refined using an autoencoder with self-attention and regularized by an optimal transport loss.

### Koopcon: A new approach towards smarter and less complex learning
![Koopcon Architecture](/images/koopcon_architecture.png)
Training deep learning models on massive datasets is computationally expensive. Koopcon introduces an autoencoder-based dataset condensation model that packs large datasets into compact, information-rich representations. The model is backed by Koopman operator theory, which allows us to systematically handle the non-linear features of the data in a linear latent space. To ensure the condensed dataset faithfully represents the original, the model minimizes the distributional discrepancy using Optimal Transport theory and the Wasserstein distance. Experimental results show that classifiers trained on the small, condensed dataset generated by Koopcon exhibit performance comparable to those trained on the original large dataset, affirming the model's efficacy in creating data-efficient learning pipelines.

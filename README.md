# 🚀 My Journey into RNA 3D Structure Prediction | Stanford RNA Folding Challenge 🧬

Over the past few weeks, I’ve been diving deep into the **Stanford RNA 3D Folding Kaggle Competition**, one of the most exciting and technically rich challenges I’ve participated in. This competition involves predicting the 3D coordinates of atoms in RNA molecules based on their nucleotide sequences. The problem sits at the intersection of biology, geometry, and deep learning, and has pushed my modeling, data engineering, and scientific visualization skills to new heights.

**🔬 Challenge Overview**
	
 	The dataset includes thousands of **RNA sequences** alongside their corresponding **3D atomic coordinates** for training. The task is to predict the 3D spatial configuration of 	nucleotides in unseen test sequences. Due to the biological complexity and geometric nature of RNA structures, this is far from a trivial problem.

**🛠️ My Workflow & Modeling Path**

	1.	EDA + Preprocessing
		I started with a comprehensive exploratory data analysis (EDA) — evaluating sequence lengths, nucleotide distributions, coordinate distributions, and label density. 			This gave me insight into the scale and variability of RNA structures across samples.
	2.	Baseline Models
		My first approach used a simple MLP Regressor on one-hot encoded sequences. Though the results weren’t perfect, it provided a valuable baseline for evaluating progress.
	3.	Embedding Models
		I replaced one-hot encodings with trainable embedding layers, allowing the model to learn richer representations of nucleotide identities. Combined with positional 			embeddings, this significantly improved performance and model generalization.
	4.	Advanced Architectures
		I implemented:
				• [Bidirectional GRUs] for sequential modeling
				• Transformer-based architectures with attention mechanisms
				• Delta prediction models that predict relative positions instead of absolute 3D coordinates
	5.	Normalization + Clipping


To improve training stability, I experimented with z-score and MinMax normalization, and applied clipping before inverse transformation to avoid out-of-bound predictions.

**📈 Evaluation & Visualizations**

	I used mean squared error (MSE) and mean absolute error (MAE) for evaluation. But more importantly, I visualized the predictions in 3D to observe how well the model captured 		molecular geometry. These visualizations—color-coded structures, progression plots, and error distribution charts—helped interpret model behavior and refine architectures.

**📤 Submission Pipeline**

	After identifying the best model, I built a clean inference pipeline:
		
  		• K-mer encoding + position IDs
		• Masking + padding handling
		• Coordinate prediction + inverse scaling
		• Output formatting for Kaggle submission

**🔥 Results**
		
  	My best **Transformer + Delta model** achieved an impressive Validation **MSE ~2945**, with substantial visual alignment between predicted and ground truth structures.

-----

**💡 Takeaways**

	This project wasn’t just about model tuning—it was about understanding structure, representation, and precision in 3D space. I learned how to combine biological domain logic 		with modern deep learning methods, and how to build a full research-grade pipeline from raw sequences to submission-ready outputs.

-----

Feel free to check out my full notebook on Kaggle or reach out if you’re exploring anything at the edge of AI & Biology. This has been one of the most rewarding challenges I’ve worked on!

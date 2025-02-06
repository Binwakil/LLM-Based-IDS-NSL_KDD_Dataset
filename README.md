
# NSL-KDD Binary Classification with Transformer

This project focuses on binary classification of the NSL-KDD dataset to detect network intrusions. A Transformer-based architecture has been implemented to analyze tabular data, demonstrating the flexibility of deep learning models in handling non-sequential datasets.

---

## Features
- **Data Preprocessing**:
  - Encoding of categorical features.
  - Normalization and scaling of numerical data.
  - Splitting into training, validation, and test sets.
- **Transformer Model**:
  - Custom multi-head self-attention and Transformer block layers.
  - Binary classification output with `sigmoid` activation.
- **Training and Evaluation**:
  - Training over multiple epochs with performance tracking.
  - Validation and test set evaluations.
  - Visualization of training history (accuracy and loss).

---

## Prerequisites
Ensure the following packages are installed:
- Python 3.8+
- TensorFlow 2.x
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

Install dependencies:
```bash
pip install tensorflow numpy pandas scikit-learn matplotlib
```

---

## Dataset
The project uses the [NSL-KDD dataset](https://www.unb.ca/cic/datasets/nsl.html) for network intrusion detection. 
- Training file: `KDDTrain+.txt`
- Test file: `KDDTest+.txt`

Preprocessing includes:
- Conversion of categorical features to numerical values.
- Binarization of labels (`1` for normal, `0` for attack).
- Scaling and normalization of numerical features.

---

## Model Architecture
The model uses a Transformer-based architecture, consisting of:
1. **Embedding Layer**: Projects features into a higher-dimensional space.
2. **Transformer Block**: Captures feature relationships using multi-head self-attention.
3. **Global Pooling Layer**: Aggregates outputs from the Transformer block.
4. **Dense Layers**: Adds fully connected layers with `ReLU` activation.
5. **Output Layer**: A single neuron with `sigmoid` activation for binary classification.

---

## Usage

### Data Preprocessing
Ensure the dataset is placed in a folder named `data/` with the following structure:
```
data/
├── KDDTrain+.txt
├── KDDTest+.txt
```
Run the notebook or script to preprocess the dataset, including feature encoding and splitting.

### Training the Model
Train the Transformer model using the provided notebook:
```bash
python train_transformer.py
```

### Evaluate the Model
After training, evaluate the model on the test set:
```python
test_loss, test_accuracy = model.evaluate(X_test, y_test)
print(f"Test Accuracy: {test_accuracy}")
```

---

## Visualizations
The training history is plotted to monitor performance over epochs:
- Training and validation accuracy.
- Training and validation loss.

Sample plots:
- **Accuracy**: Shows the improvement in prediction performance.
- **Loss**: Tracks model optimization during training.

---

## Results
- **Baseline Accuracy**: 53% 
- **Validation Accuracy**: 99% 
- **Test Accuracy**: 99% 

---

## Future Work
- Fine-tune hyperparameters (e.g., number of heads, embedding dimension, learning rate).
- Experiment with other architectures such as TabTransformer or XGBoost for comparison.
- Extend the model to multi-class classification for more granular analysis of attack types.

---

## License
This project is open-source and available under the [MIT License](LICENSE).

---

## Author
**Almustapha Wakili**  
PhD Candidate, Towson University  
Email: [awakili@towson.edu](mailto:awakili@towson.edu)

---

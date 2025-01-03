

  <h1>Character Translation Using Transformers</h1>
    <p>This project implements a character-level translation model using PyTorch Lightning and Transformer architecture. It aims to perform language translation tasks at the character level, leveraging the Transformer model's ability to handle sequence-to-sequence problems effectively.</p>

  <h2>Features</h2>
    <ul>
        <li><b>Custom Data Module:</b> Includes a PyTorch Lightning <code>CharacterTranslationDataModule</code> for handling and preprocessing the data, encoding sequences, and splitting data into training and validation sets.</li>
        <li><b>Transformer-based Model:</b> Implements a character-level Transformer with embedding, positional encoding, and multiple encoder-decoder layers.</li>
        <li><b>Accuracy Evaluation:</b> Evaluates the model across 10 independent runs and logs accuracy metrics.</li>
        <li><b>Results Visualization:</b> Plots the accuracy achieved across different runs for performance tracking.</li>
    </ul>

  <h2>Workflow</h2>
    <ol>
        <li><b>Data Loading:</b> Downloads the English-Portuguese dataset if not already present locally.</li>
        <li><b>Data Preprocessing:</b> Encodes input and output sequences with start and stop tokens and pads them to a uniform length.</li>
        <li><b>Model Training:</b> Trains the Transformer-based model for up to 200 epochs using the GPU (if available).</li>
        <li><b>Evaluation:</b> Evaluates model accuracy on the test set and logs metrics.</li>
        <li><b>Results Saving and Plotting:</b> Saves the test accuracy of all 10 runs to a text file (<code>translation-results.txt</code>) and visualizes them in a plot.</li>
    </ol>

  <h2>Requirements</h2>
    <ul>
        <li>Python 3.8+</li>
        <li>PyTorch and PyTorch Lightning</li>
        <li>NumPy</li>
        <li>Matplotlib</li>
        <li>TorchMetrics</li>
    </ul>

  <h2>Installation</h2>
    <ol>
        <li>Clone the repository:
            <pre><code>git clone &lt;repository-url&gt;
cd &lt;repository-name&gt;</code></pre>
        </li>
        <li>Install dependencies:
            <pre><code>pip install -r requirements.txt</code></pre>
        </li>
        <li>Run the training and evaluation script:
            <pre><code>python train_translation_model.py</code></pre>
        </li>
    </ol>

   <h2>Results</h2>
  <p>The model achieves an average accuracy of approximately <b>91.5%</b> across 10 independent runs, demonstrating the robustness and reliability of the Transformer architecture for character-level translation tasks. A plot visualizing accuracy across runs is included in the repository.</p>

  <h2>File Structure</h2>
    <ul>
        <li><code>train_translation_model.py</code>: Main script for training and evaluating the model.</li>
        <li><code>CharacterTranslationDataModule</code>: Data module for preprocessing and batching data.</li>
        <li><code>TransformerTranslationModel</code>: Transformer-based model implementation.</li>
        <li><code>translation-results.txt</code>: Contains the accuracy results for 10 runs.</li>
        <li><code>results_plot.png</code>: Visualization of accuracy across runs.</li>
    </ul>

  <h2>Future Improvements</h2>
  <ul>
        <li>Extend to word-level translation for more practical use cases.</li>
        <li>Explore additional Transformer configurations for improved accuracy.</li>
        <li>Incorporate attention visualization to interpret the model’s behavior.</li>
    </ul>

  <h2>Acknowledgments</h2>
  <p>The dataset is sourced from Luis Roque's repository. The implementation leverages PyTorch Lightning for modular and scalable deep learning.</p>


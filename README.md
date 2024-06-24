# NONAME-Tool
## Using Our Tool for Metabolic Modeling

This guide walks you through preparing your data and model for use with our tool.

**File Formats**
| File Type             | Description                                                   | Supported Formats                                  |
|------------------------|--------------------------------------------------------------|----------------------------------------------------|
| Expression Data       | Contains gene expression values for your samples.             | `.xlsx`, `.csv`                                       |
| Organism Model        | Represents the metabolic network of your organism.           | `.xml (SBML)`, `.mat`                               |

**Part 1: Modifying Expression Data**

1. **Column Renaming:**
    - In your expression file (`.xlsx` or `.csv`), identify the column containing gene data. This column might be named "Gene symbols," "Gene names," "Probe_ids," or something similar.
    - Rename this column to simply "Gene."
    - Ensure that the gene names in this column match exactly with the gene names used in your chosen model. You can usually find this information on the model's website or database.

2. **Column Selection:**
    - Keep only the "Gene" column and the columns containing expression values for each sample.
    - Remove any unnecessary columns with information unrelated to gene expression.

**Part 2: Organism Model**

1. **GPR Rules Requirement:**
    - Your chosen model must contain GPR (Gene-Protein-Reaction) rules to be compatible with our tool.
    - We support models in both `.xml` (SBML format) and `.mat` formats.

2. **Model Selection:**
    - You can find suitable models from publicly available repositories like BiGG Models and BioModels (as mentioned in our article).

3. **Example Model:**
    - Here's an example of an E. coli model available at http://bigg.ucsd.edu/models/iAF1260.

**Part 3: Running the Code**

- **Sequential Execution:**
    - Execute the code cells within your chosen environment (Jupyter Notebook or Google Colab) in the exact order they appear.
    - Make sure each code cell runs successfully before proceeding to the next one. This ensures proper data processing.

**Additional Tips:**

- Consider including screenshots (`.png` or `.jpg`) of Figures 1.1 and 1.2 (if applicable) in your Markdown file to provide visual examples.
- You can use code blocks to display code snippets within your Markdown document. For example:

```python
# Sample Python code
import pandas as pd

data = pd.read_csv("expression_data.csv")
data = data[["Gene", "Sample1", "Sample2"]]

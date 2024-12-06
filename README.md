# FluxReal-Toolbox

--> [Easy-to-Use Version](https://colab.research.google.com/drive/1wag8YWG-5yFAnSAbnUYl9ilQGObNYBwM?usp=sharing) in Google Colab

Cosider citing us if you use this tool in your research:
 
```
Citatation buraya gelecek
But let's throw in a <b>tag</b>.
```

## Using Our Tool for Metabolic Modeling

This guide walks you through preparing your data and model for use with our tool.

**File Formats**
| File Type             | Description                                                   | Supported Formats                                  |
|------------------------|--------------------------------------------------------------|----------------------------------------------------|
| Expression Data       | Contains gene expression values for your samples.             | `.xlsx`, `.csv`                                       |
| Organism Model        | Represents the metabolic network of your organism.           | `.xml (SBML)`, `.mat`                               |

### Part 1: Modifying Expression Data 

1. **Column Renaming:**
    - In your expression file (`.xlsx` or `.csv`), identify the column containing gene data. This column might be named "Gene symbols," "Gene names," "Probe_ids," or something similar.
    - Rename this column to simply "Gene."
    - Ensure that the gene names in this column match exactly with the gene names used in your chosen model. You can usually find this information on the model's website or database.

2. **Column Selection:**
    - Keep only the "Gene" column and the columns containing expression values for each sample.
    - Remove any unnecessary columns with information unrelated to gene expression.

Example Modified Expression Data for Recon3 : ![Alt text](Figure1.png?raw=true "Example Modified Expression Data for Recon3D")

Example Modified Expression Data for  iAF1260 (Escherichia Coli) : ![Alt text](Figure2.png?raw=true "Example Modified Expression Data for  iAF1260 (Escherichia Coli)")

### Part 2: Organism Model

1. **GPR Rules Requirement:**
    - Your chosen model must contain GPR (Gene-Protein-Reaction) rules to be compatible with our tool.
    - We support models in both `.xml` (SBML format) and `.mat` formats.

2. **Model Selection:**
    - You can find suitable models from publicly available repositories like [BiGG Models](http://bigg.ucsd.edu/) and [BioModels](https://www.ebi.ac.uk/biomodels/) (as mentioned in our article).
    - Here's an example of an E. coli model [iAF1260](http://bigg.ucsd.edu/models/iAF1260).

### Part 3: Running the Code

- **Sequential Execution:**
    - Execute the code cells within your chosen environment (Jupyter Notebook or Google Colab) in the exact order they appear.
    - Make sure each code cell runs successfully before proceeding to the next one. This ensures proper data processing.

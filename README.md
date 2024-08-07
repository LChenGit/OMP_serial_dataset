
# OMP_Serial Dataset

This dataset, named **omp_serial**, consists of code snippets annotated with various OpenMP pragma labels and other relevant metadata. The dataset is provided in a JSON file format.

## Data Description

The JSON file contains entries with the following fields:

- **ID**: A unique identifier for each entry.
- **realId**: The original identifier from the source data.
- **code**: The code snippet associated with the entry.
- **pragma**: The OpenMP pragma directive used in the code snippet.
- **label_para**: Label indicating the presence of parallelization.
- **label_function_call**: Label indicating the presence of function calls.
- **label_nested_loop**: Label indicating the presence of nested loops.
- **label_reduction**: Label indicating the presence of reduction operations.
- **label_task**: Label indicating the presence of tasks.
- **label_simd**: Label indicating the presence of SIMD directives.
- **label_target**: Label indicating the presence of target directives.

## File Format

The dataset is provided in a JSON file named `OMP_Serial.json`. Each line in the file represents a single code snippet along with its annotations as a JSON object.

## How to Use

### Loading Data with Pandas

To load and use the data with Python, you can use the `pandas` library:

```python
import pandas as pd

# Load the JSON file
df = pd.read_json('omp_serial.json', lines=True)

# Display the first few rows of the DataFrame
print(df.head())
```

### Example Usage

Here is an example of how you can access and manipulate the data:

```python
import pandas as pd

# Load the JSON file
df = pd.read_json('OMP_Serial.json', lines=True)

# Filter code snippets with parallelization
parallel_snippets = df[df['label_para'] == 1]

# Display the filtered code snippets
print(parallel_snippets)
```

## Citation

If you use this dataset in your research, please cite our work:

```bibtex
@article{chen2023learning,
  title={Learning to parallelize with openmp by augmented heterogeneous ast representation},
  author={Chen, Le and Mahmud, Quazi Ishtiaque and Phan, Hung and Ahmed, Nesreen and Jannesari, Ali},
  journal={Proceedings of Machine Learning and Systems},
  volume={5},
  year={2023}
}
```

## Contact

For any questions or issues, please contact:

- **Name**: Le Chen
- **Email**: lechen AT iastate.edu

## License

This dataset is licensed under the MIT License. Please see the LICENSE file for more information.


# TLU-IS330-BigData-1

## Installation Guide

### Step 1: Download and Set Up Apache Spark

1. **Download Apache Spark:**
   - Visit the [Apache Spark download page](https://spark.apache.org/downloads.html).
   - Choose the latest version of Spark and a pre-built package for Hadoop.

2. **Extract the downloaded package:**
   ```bash
   tar -xvf spark-<version>-bin-hadoop<version>.tgz```
   ```

3.  **Set up the SPARK_HOME environment variable:**

Add the following lines to your .bashrc, .zshrc, or equivalent shell configuration file:
```bash
export SPARK_HOME=/path/to/spark-<version>-bin-hadoop<version>
export PATH=$SPARK_HOME/bin:$PATH```
```
- Reload the shell configuration:

```bash
source ~/.bashrc  # or source ~/.zshrc
```

## Step 2: Download and Set Up JDK 17
Download JDK 17:

4. **Visit the Oracle JDK download page or use the OpenJDK from AdoptOpenJDK.**
Install JDK 17:

Follow the instructions for your operating system.
Set up the JAVA_HOME environment variable:

Add the following lines to your .bashrc, .zshrc, or equivalent shell configuration file:
```bash
export JAVA_HOME=/path/to/jdk-17
export PATH=$JAVA_HOME/bin:$PATH
```
Reload the shell configuration:
```bash
source ~/.bashrc  # or source ~/.zshrc
```

## Step 3: Install PySpark
Install PySpark using pip:
```bash
pip install pyspark
```

## Step 4: Verify the Installation
Create a simple script to verify the installation:

```python
from pyspark import SparkConf, SparkContext
```

### Example Spark configuration
```python
conf = SparkConf().setAppName("exampleApp").setMaster("local[*]")
```

### Initialize SparkContext
```python
sc = SparkContext(conf=conf)
```
### Check SparkContext
```python
print(sc)
```
Run the script to ensure everything is set up correctly:

```bash
python verify_spark.py
```
If the setup is correct, you should see output indicating that the SparkContext has been successfully initialized.

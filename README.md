# FlexSum: Document Summarization with Controllable Parameters

FlexSum is an advanced NLP system that provides customizable document summarization with fine-grained control over various parameters including length, focus areas, and abstraction level.

## 🌟 Features

- **Controllable Parameters:**
  - Summary length (percentage or word count)
  - Focus areas (topics/entities emphasis)
  - Abstraction level (extractive to abstractive)
  - Domain adaptation (specialized vocabulary handling)

- **Multi-format Support:**
  - PDF documents
  - DOCX files
  - Plain text
  - HTML content

- **Comprehensive Evaluation:**
  - ROUGE metrics
  - BERTScore
  - Human evaluation interface
  - Comparison with reference summaries

- **User-friendly Interface:**
  - Interactive parameter controls
  - Real-time summary generation
  - Source-summary highlighting

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- PyTorch 1.10+

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/FlexSum.git
cd FlexSum

# Create and activate virtual environment
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate

# Install dependencies
pip install -r requirements.txt

from src.models.summarizer import FlexSummarizer
from src.data.document_loader import DocumentLoader

# Load document
loader = DocumentLoader()
document = loader.load("path/to/document.pdf")

# Initialize summarizer with parameters
summarizer = FlexSummarizer(
    length_control=0.3,  # 30% of original length
    focus_areas=["main topic"],
    abstraction_level=0.5  # balanced between extractive and abstractive
)

# Generate summary
summary = summarizer.summarize(document)
print(summary)

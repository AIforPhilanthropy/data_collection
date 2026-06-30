# Educational Web Scraping for Swiss Solidarity Campaign Data

This repository provides an educational, end-to-end notebook that demonstrates multiple web scraping strategies on Swiss Solidarity campaign pages.

Primary target listing:
- https://www.swiss-solidarity.org/our-work/our-past-campaigns

The notebook is designed for teaching and reproducibility. It includes setup, data extraction, pagination handling, and output persistence in structured files.

## Open in Google Colab

You can run the notebook directly in Google Colab with this link:

[Open in Colab](https://colab.research.google.com/github/AIforPhilanthropy/data_collection/blob/main/notebooks/web_scraping_swiss_solidarity_tutorial.ipynb)

In Colab, use File > Save a copy in Drive to place it in your Google Drive.

## No-Code Web Scraper Interface (Hugging Face Space)

For non-coders, you can also use this user-friendly web app:

[Hugging Face Space: Web Scraper UI](https://huggingface.co/spaces/luciagomez/web_scraper)

This interface is designed to let you scrape websites without writing code. It supports:
- Recursive web scraping with BeautifulSoup
- Sitemap exploration to discover website structure
- Retrieval of specific elements identified through the sitemap
- Download and preservation of PDF files as PDF documents

<img width="725" height="505" alt="image" src="https://github.com/user-attachments/assets/8b7e882e-8c68-4b12-92fc-43d12081abac" />


## What This Notebook Teaches

The notebook compares and documents several scraping approaches:

1. HTTP requests only
2. Requests + BeautifulSoup
3. Selenium browser automation
4. Agentic extraction with Gemini API (minimal section, optional)
5. Agentic extraction with MolmoWeb endpoint (minimal section, optional)

It also includes:
- Pagination handling for button-based pagination across multiple pages
- Polite scraping behavior through delays and explicit headers
- Structured output generation for downstream analysis

## Repository Structure

- notebooks/web_scraping_swiss_solidarity_tutorial.ipynb: Main educational notebook

When executed, the notebook writes data to:
- outputs/swiss_solidarity_scraping/

Typical output files include:
- 00_config.json
- 01_helper_definition.json
- 02_method_a_seed_meta.json
- 03_method_a_regex_links.json
- 04_method_a_shallow_crawl.json
- 05_method_b_bs4_links.json
- 06_method_b_pagination_and_records.json
- 07_method_c_selenium.json
- 08_method_d_gemini.json
- 09_method_e_molmoweb.json

## Educational Goals

This material is intended for students and practitioners who want to understand:
- Trade-offs between static scraping and browser-based scraping
- How to detect and traverse pagination
- How to build reusable extraction helpers
- How to produce clean, machine-readable outputs
- How to combine deterministic extraction with agentic methods

## Running Locally

Recommended Python packages:
- requests
- beautifulsoup4
- selenium

Optional for advanced sections:
- google-genai (Gemini section)
- a running MolmoWeb-compatible endpoint (MolmoWeb section)

If Selenium is installed but browser driver execution fails, the notebook handles that gracefully and reports the reason.

## Notes on Responsible Scraping

Please review website terms and robots rules before collecting data at scale.
The notebook is configured for educational use with low request volume and lightweight pacing.

## License

See LICENSE.

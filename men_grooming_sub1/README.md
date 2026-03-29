# Men's Grooming Products Scraper - Group 1 (Face Care)

This module scrapes men's grooming products from Boutiqaat.com, specifically focusing on face care subcategories.

## Covered Subcategories

- Face Moisturizers
- Day & Night Creams
- Face Serums & Treatments
- Face Oils
- Face Masks
- Sheet Masks
- Face Wash & Cleansers
- Face Scrubs & Exfoliators
- Toners
- Eye Serum & Treatments
- Eye Masks
- Lip Balm & Treatments

## Features

- **Async Processing**: Uses asyncio with semaphore (max 3 concurrent) for efficient scraping
- **Playwright Integration**: Handles JavaScript-rendered content and infinite scroll
- **S3 Integration**: Uploads product images and Excel files to AWS S3
- **Excel Generation**: Creates formatted Excel workbooks with product data
- **Date Partitioning**: Stores data in S3 with year/month/day structure

## S3 Storage Path

```
boutiqaat-data/year=YYYY/month=MM/day=DD/men/grooming/
```

## Usage

```bash
python -m men_grooming_sub1.main
```

## Dependencies

- Python 3.11+
- playwright
- beautifulsoup4
- boto3
- openpyxl

## Part of GitHub Actions Workflow

This module runs as part of the automated daily workflow at 3:00 AM UTC.

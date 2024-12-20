
## How Does This Project Work?

### Web Scraping:
- Python scripts (e.g., `jobscraper_indeed.py`) utilize libraries like **Selenium** or **BeautifulSoup** to scrape job data from various websites.
- Scraped data is saved in a **JSON** file (`jobs.json`).

### Backend with Flask:
- **Flask** serves the scraped job data via a REST API (`/api/jobs`).
- The main route (`/`) dynamically renders the job data into an **HTML** table.

### Frontend with HTML:
- The web interface uses **Bootstrap**-enhanced HTML templates to display job listings in a clean and responsive layout.

### Containerization with Docker:
- The entire application (scraper, Flask app, frontend) is containerized into a **Docker** image for easy deployment.
- **Docker Compose** is used to manage volumes, ports, and dependencies, simplifying setup and execution.

### Running on Raspberry Pi:
- This project is designed to run on a **Raspberry Pi** using **Docker** for seamless deployment.
- The containerized app ensures portability and consistent operation across different environments.

### Handling Resource Constraints:
- The app is optimized for efficiency, running lightweight processes in Docker containers.
- A **headless** scraping approach (e.g., Chromium in headless mode) minimizes system resource usage.
- Where applicable, Python’s **async features** are used to optimize performance and handle multiple tasks concurrently.


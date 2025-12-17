# Data Engineering Curriculum - Week by Week

## Phase 1: Foundations (Weeks 1-6)

### Week 1: SQL Basics & Environment Setup
**Goal:** Get comfortable with SQL fundamentals

**Daily Tasks:**
- **Day 1-2:** SQL basics review
  - SELECT, WHERE, ORDER BY, LIMIT
  - Data types and basic operators
  - Setup: Install PostgreSQL or use online SQL editors
  - Practice: 10 basic SELECT queries

- **Day 3-4:** Filtering and sorting
  - DISTINCT, IN, BETWEEN, LIKE
  - AND, OR, NOT operators
  - NULL handling
  - Practice: 10 filtering problems

- **Day 5-6:** Aggregate functions
  - COUNT, SUM, AVG, MIN, MAX
  - GROUP BY and HAVING
  - Practice: 10 aggregation problems

- **Day 7:** Review & mini-project
  - Complete 20 easy SQL problems on LeetCode
  - Write queries analyzing sample e-commerce data

**Resources:**
- SQLBolt (interactive tutorial)
- Mode Analytics SQL Tutorial
- LeetCode SQL (Easy problems)

---

### Week 2: Advanced SQL - Part 1
**Goal:** Master JOINs and subqueries

**Daily Tasks:**
- **Day 1-2:** JOINs deep dive
  - INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN
  - CROSS JOIN
  - Self joins
  - Practice: 15 JOIN problems

- **Day 3-4:** Subqueries
  - Subqueries in WHERE clause
  - Subqueries in FROM clause (derived tables)
  - Subqueries in SELECT clause
  - Correlated subqueries
  - Practice: 15 subquery problems

- **Day 5-6:** Set operations
  - UNION, UNION ALL
  - INTERSECT, EXCEPT
  - Combining multiple queries
  - Practice: 10 problems

- **Day 7:** Review & practice
  - 25 medium-level SQL problems
  - Focus on real-world scenarios

**Milestone:** Complete 50 SQL problems total

---

### Week 3: Advanced SQL - Part 2
**Goal:** Master window functions and CTEs

**Daily Tasks:**
- **Day 1-2:** Window functions basics
  - ROW_NUMBER(), RANK(), DENSE_RANK()
  - OVER() clause and PARTITION BY
  - Practice: 10 ranking problems

- **Day 3-4:** Advanced window functions
  - LAG(), LEAD()
  - SUM/AVG/COUNT as window functions
  - Running totals and moving averages
  - Practice: 15 window function problems

- **Day 5-6:** CTEs (Common Table Expressions)
  - Basic CTEs (WITH clause)
  - Multiple CTEs
  - Recursive CTEs
  - Practice: 10 CTE problems

- **Day 7:** Integration & practice
  - Complex queries combining JOINs, CTEs, and window functions
  - 20 medium/hard problems

**Milestone:** 100+ SQL problems completed

---

### Week 4: Python Fundamentals
**Goal:** Build solid Python foundation

**Daily Tasks:**
- **Day 1:** Python setup & basics
  - Install Python 3.11+, VS Code, Jupyter
  - Variables, data types, operators
  - Input/output
  - Practice: 10 basic programs

- **Day 2:** Control flow
  - if/elif/else statements
  - for and while loops
  - break, continue, pass
  - Practice: 15 control flow exercises

- **Day 3:** Data structures
  - Lists, tuples, sets
  - List comprehensions
  - Practice: 20 list manipulation problems

- **Day 4:** Dictionaries
  - Dictionary operations
  - Dictionary comprehensions
  - Nested dictionaries
  - Practice: 15 dictionary problems

- **Day 5:** Functions
  - Function definition and calling
  - Arguments (positional, keyword, default, *args, **kwargs)
  - Lambda functions
  - Practice: 15 function exercises

- **Day 6:** File I/O
  - Reading/writing text files
  - CSV file handling
  - JSON file operations
  - Practice: 10 file handling programs

- **Day 7:** Mini project
  - Build: CSV data analyzer
  - Read CSV, calculate statistics, generate report

**Milestone:** 50+ Python programs written

---

### Week 5: Python - Intermediate Concepts
**Goal:** OOP and error handling

**Daily Tasks:**
- **Day 1-2:** Object-Oriented Programming
  - Classes and objects
  - Attributes and methods
  - __init__ constructor
  - Practice: Create 5 classes

- **Day 3:** OOP advanced
  - Inheritance
  - Encapsulation
  - Polymorphism
  - Practice: Build class hierarchy

- **Day 4:** Error handling
  - try/except/finally
  - Common exceptions
  - Custom exceptions
  - Practice: Add error handling to previous programs

- **Day 5:** Modules and packages
  - Importing modules
  - Creating your own modules
  - Virtual environments (venv)
  - pip and package management

- **Day 6:** Working with dates and times
  - datetime module
  - Date arithmetic
  - Timezone handling
  - Practice: Date manipulation exercises

- **Day 7:** Project
  - Build: Data ETL script v1.0
  - Read multiple CSVs, merge, clean, output JSON

**Milestone:** Comfortable with Python syntax and structure

---

### Week 6: Git & Version Control
**Goal:** Master Git workflow for professional development

**Daily Tasks:**
- **Day 1:** Git basics
  - Install Git
  - git init, clone, status
  - git add, commit
  - .gitignore
  - Practice: Create local repository

- **Day 2:** GitHub & remote repositories
  - Create GitHub account
  - git push, pull, fetch
  - SSH keys setup
  - Practice: Push your Python projects to GitHub

- **Day 3:** Branching
  - git branch, checkout, switch
  - Merge basics
  - Resolving conflicts
  - Practice: Create feature branches

- **Day 4:** Advanced Git
  - git log, diff
  - git stash
  - git rebase (basic)
  - Commit message best practices

- **Day 5:** GitHub workflow
  - README.md best practices
  - Markdown syntax
  - Repository structure
  - Practice: Clean up your repositories

- **Day 6-7:** Portfolio setup
  - Organize your learning repositories
  - Create professional README files
  - Add project descriptions
  - Start documenting your journey

**Milestone:** Active GitHub with organized learning history

---

## Phase 2: Core Data Engineering Skills (Weeks 7-14)

### Week 7: Python for Data - pandas Basics
**Goal:** Start working with DataFrames

**Daily Tasks:**
- **Day 1:** pandas introduction
  - Install pandas, NumPy
  - Series and DataFrames
  - Reading CSV, Excel files
  - Practice: Load and explore datasets

- **Day 2:** DataFrame operations
  - Selecting columns and rows
  - iloc and loc
  - Filtering data
  - Practice: 10 selection exercises

- **Day 3:** Data manipulation
  - Adding/removing columns
  - Sorting data
  - Handling duplicates
  - Practice: Data cleaning exercises

- **Day 4:** Missing data
  - Detecting missing values
  - fillna(), dropna()
  - Interpolation
  - Practice: Clean messy datasets

- **Day 5:** Aggregations
  - groupby()
  - agg() and apply()
  - Multiple aggregations
  - Practice: Group and summarize data

- **Day 6:** Merging data
  - merge() - like SQL joins
  - concat()
  - join()
  - Practice: Combine multiple datasets

- **Day 7:** Project
  - Analyze e-commerce dataset
  - Sales trends, customer analysis
  - Generate insights and visualizations

---

### Week 8: Python for Data - Advanced pandas & NumPy
**Goal:** Advanced data manipulation

**Daily Tasks:**
- **Day 1-2:** Advanced pandas
  - pivot_table() and pivot()
  - stack() and unstack()
  - MultiIndex DataFrames
  - Practice: Reshape complex datasets

- **Day 3:** Time series
  - DateTime index
  - Resampling
  - Rolling windows
  - Practice: Time series analysis

- **Day 4:** NumPy basics
  - Arrays and operations
  - Broadcasting
  - Array manipulations
  - Practice: NumPy exercises

- **Day 5:** String operations
  - str accessor methods
  - Regular expressions
  - Text cleaning
  - Practice: Clean text data

- **Day 6:** Performance optimization
  - Vectorization
  - apply() vs vectorized operations
  - Memory optimization
  - Practice: Optimize slow code

- **Day 7:** Project
  - Build: Data cleaning pipeline
  - Process messy real-world dataset
  - Output clean, analysis-ready data

---

### Week 9: Database Connections & SQL from Python
**Goal:** Connect Python to databases

**Daily Tasks:**
- **Day 1:** PostgreSQL setup
  - Install PostgreSQL
  - Create database and tables
  - psql command line basics

- **Day 2:** Python DB API
  - psycopg2 library
  - Connection handling
  - Executing queries
  - Practice: CRUD operations

- **Day 3:** SQLAlchemy introduction
  - Engine and connections
  - Executing raw SQL
  - Parameterized queries
  - Practice: Query databases from Python

- **Day 4:** pandas + SQL
  - read_sql() and to_sql()
  - Query results to DataFrames
  - Bulk inserts
  - Practice: ETL workflows

- **Day 5:** ORM basics
  - SQLAlchemy ORM
  - Models and tables
  - Querying with ORM
  - Practice: Build simple ORM models

- **Day 6:** Connection pooling
  - Managing connections efficiently
  - Context managers
  - Error handling

- **Day 7:** Project
  - Build: Database ETL script
  - Extract from CSV → Transform with pandas → Load to PostgreSQL

**Milestone:** Can build end-to-end ETL scripts

---

### Week 10: Data Warehousing Concepts
**Goal:** Understand DW architecture and design

**Daily Tasks:**
- **Day 1:** Data warehouse fundamentals
  - OLTP vs OLAP
  - Data warehouse architecture
  - ETL vs ELT
  - Read: Kimball methodology basics

- **Day 2:** Dimensional modeling
  - Facts and dimensions
  - Star schema
  - Snowflake schema
  - Practice: Design simple star schema

- **Day 3:** Dimension types
  - Slowly Changing Dimensions (SCD Type 1, 2, 3)
  - Conformed dimensions
  - Junk dimensions
  - Practice: Design SCD Type 2

- **Day 4:** Fact tables
  - Transaction facts
  - Snapshot facts
  - Accumulating facts
  - Factless facts
  - Practice: Design fact tables

- **Day 5:** Data modeling practice
  - Design e-commerce data warehouse
  - Identify facts and dimensions
  - Create ERD diagram

- **Day 6:** Data quality
  - Data validation
  - Data profiling
  - Data lineage
  - Study: Great Expectations library

- **Day 7:** Review & project planning
  - Plan your data warehouse project
  - Design schema for retail analytics

---

### Week 11: Introduction to Apache Airflow
**Goal:** Start orchestrating data pipelines

**Daily Tasks:**
- **Day 1:** Airflow introduction
  - What is workflow orchestration?
  - Airflow architecture (scheduler, executor, web server)
  - Install Airflow locally
  - Start web UI

- **Day 2:** DAGs (Directed Acyclic Graphs)
  - DAG definition
  - Task dependencies
  - Create first simple DAG
  - Practice: Hello World DAG

- **Day 3:** Operators
  - PythonOperator
  - BashOperator
  - EmailOperator
  - Practice: Build multi-task DAG

- **Day 4:** Task dependencies
  - set_upstream() and set_downstream()
  - >> and << operators
  - Branching
  - Practice: Complex dependencies

- **Day 5:** Scheduling
  - cron expressions
  - Schedule intervals
  - start_date and end_date
  - Catchup and backfilling

- **Day 6:** XCom and task communication
  - Passing data between tasks
  - XCom push and pull
  - Best practices

- **Day 7:** Project
  - Build: Daily ETL pipeline DAG
  - Extract from API → Transform → Load to database
  - Schedule to run daily

---

### Week 12: Advanced Airflow
**Goal:** Production-ready pipelines

**Daily Tasks:**
- **Day 1:** Sensors
  - FileSensor
  - HttpSensor
  - TimeSensor
  - Practice: Wait for external events

- **Day 2:** Hooks and connections
  - PostgresHook
  - HttpHook
  - Managing connections in Airflow UI
  - Practice: Database operations

- **Day 3:** Variables and templates
  - Airflow Variables
  - Jinja templating
  - Macros
  - Practice: Dynamic pipelines

- **Day 4:** Error handling
  - Retries and timeouts
  - on_failure_callback
  - Email alerts
  - Practice: Robust error handling

- **Day 5:** Testing DAGs
  - Unit testing
  - DAG validation
  - Testing tasks locally
  - Practice: Write tests

- **Day 6:** Best practices
  - DAG design patterns
  - Idempotency
  - Task sizing
  - Documentation

- **Day 7:** Project
  - Build: Complex multi-stage ETL pipeline
  - Multiple data sources
  - Data quality checks
  - Error notifications

---

### Week 13: APIs & Web Scraping
**Goal:** Extract data from web sources

**Daily Tasks:**
- **Day 1:** REST APIs basics
  - HTTP methods (GET, POST)
  - Status codes
  - JSON responses
  - Practice: Call public APIs

- **Day 2:** requests library
  - Making API calls
  - Query parameters
  - Headers and authentication
  - Practice: 10 API integrations

- **Day 3:** API pagination
  - Offset-based pagination
  - Cursor-based pagination
  - Handling large datasets
  - Practice: Paginate through API results

- **Day 4:** Rate limiting
  - API rate limits
  - Retry logic with backoff
  - Throttling requests
  - Practice: Respectful API consumption

- **Day 5:** Web scraping basics
  - BeautifulSoup
  - HTML parsing
  - Extracting data
  - Practice: Scrape 5 websites

- **Day 6:** Ethics & legality
  - robots.txt
  - Terms of service
  - Legal considerations
  - Best practices

- **Day 7:** Project
  - Build: API data collector
  - Extract from 3+ APIs
  - Transform and standardize
  - Load to database
  - Schedule with Airflow

---

### Week 14: Data Formats & Storage
**Goal:** Work with various data formats

**Daily Tasks:**
- **Day 1:** CSV and Excel
  - Advanced CSV handling
  - Excel with openpyxl
  - Large file processing
  - Practice: Process large CSV files

- **Day 2:** JSON
  - Complex JSON structures
  - Nested JSON
  - JSON Lines (JSONL)
  - Practice: Parse complex JSON

- **Day 3:** Parquet
  - Columnar format benefits
  - PyArrow and fastparquet
  - Reading/writing Parquet
  - Practice: CSV to Parquet conversion

- **Day 4:** XML
  - XML parsing
  - ElementTree
  - XML to DataFrame
  - Practice: Parse XML feeds

- **Day 5:** Avro
  - Schema evolution
  - Reading/writing Avro
  - Use cases

- **Day 6:** Data compression
  - gzip, bzip2
  - Compression strategies
  - Performance considerations

- **Day 7:** Review & project
  - Build: Universal data converter
  - Convert between formats
  - Optimize for size and speed

**Milestone:** Core DE skills established

---

## Phase 3: Cloud & Modern Tools (Weeks 15-20)

### Week 15: AWS Fundamentals
**Goal:** Understand cloud basics

**Daily Tasks:**
- **Day 1:** AWS account setup
  - Create AWS account
  - Set up billing alerts
  - IAM basics
  - MFA setup

- **Day 2:** IAM deep dive
  - Users, groups, roles
  - Policies and permissions
  - Least privilege principle
  - Practice: Create IAM users

- **Day 3:** S3 (Simple Storage Service)
  - Buckets and objects
  - Storage classes
  - Versioning
  - Practice: Upload/download files

- **Day 4:** S3 advanced
  - Lifecycle policies
  - Event notifications
  - S3 + Python (boto3)
  - Practice: Automate S3 operations

- **Day 5:** EC2 basics
  - Launch an instance
  - Security groups
  - SSH connection
  - Practice: Deploy Python script on EC2

- **Day 6:** AWS CLI
  - Install and configure
  - Common commands
  - Scripting with AWS CLI

- **Day 7:** Project
  - Build: S3 data pipeline
  - Upload data to S3
  - Trigger Lambda on upload
  - Process and store results

---

### Week 16: AWS Data Services
**Goal:** Master AWS data tools

**Daily Tasks:**
- **Day 1:** RDS (Relational Database Service)
  - Create PostgreSQL RDS instance
  - Connect from Python
  - Backup and restore
  - Practice: Migrate local DB to RDS

- **Day 2:** AWS Lambda
  - Serverless concepts
  - Create Lambda functions
  - Triggers and events
  - Practice: S3 trigger → Lambda processing

- **Day 3:** Lambda for data processing
  - Lambda layers
  - Environment variables
  - Error handling
  - Practice: Data transformation Lambda

- **Day 4:** AWS Glue introduction
  - Glue Data Catalog
  - Crawlers
  - ETL jobs
  - Practice: Catalog S3 data

- **Day 5:** Glue ETL jobs
  - PySpark basics
  - Glue Studio
  - Create ETL job
  - Practice: S3 to S3 transformation

- **Day 6:** Amazon Redshift
  - Data warehouse service
  - Create cluster
  - Load data from S3
  - Query with SQL
  - Practice: Build simple data warehouse

- **Day 7:** Project
  - Build: End-to-end AWS pipeline
  - S3 → Glue → Redshift
  - Query and analyze

---

### Week 17: More AWS Services
**Goal:** Expand AWS toolkit

**Daily Tasks:**
- **Day 1:** CloudWatch
  - Logs and monitoring
  - Metrics and dashboards
  - Alarms
  - Practice: Monitor your pipelines

- **Day 2:** SQS (Simple Queue Service)
  - Queue concepts
  - Creating queues
  - Producing and consuming messages
  - Practice: Decouple pipeline stages

- **Day 3:** SNS (Simple Notification Service)
  - Topics and subscriptions
  - Email/SMS notifications
  - Integration with Lambda
  - Practice: Pipeline alerts

- **Day 4:** Kinesis
  - Streaming data concepts
  - Kinesis Data Streams
  - Producers and consumers
  - Practice: Real-time data ingestion

- **Day 5:** EventBridge
  - Event-driven architecture
  - Rules and targets
  - Scheduling
  - Practice: Orchestrate services

- **Day 6:** Cost optimization
  - Understanding AWS billing
  - Cost allocation tags
  - Reserved instances
  - Spot instances

- **Day 7:** Review
  - AWS services comparison
  - When to use what
  - Architecture patterns

---

### Week 18: Docker & Containerization
**Goal:** Container essentials

**Daily Tasks:**
- **Day 1:** Docker introduction
  - What are containers?
  - Install Docker Desktop
  - docker run basics
  - Practice: Run containers

- **Day 2:** Docker images
  - Images vs containers
  - docker pull, build
  - Docker Hub
  - Practice: Run different images

- **Day 3:** Dockerfile
  - Writing Dockerfiles
  - FROM, COPY, RUN, CMD
  - Multi-stage builds
  - Practice: Create Python app image

- **Day 4:** Docker Compose
  - Multi-container applications
  - docker-compose.yml
  - Services and networks
  - Practice: Python app + PostgreSQL

- **Day 5:** Volumes and networking
  - Data persistence
  - Volume mounts
  - Container networking
  - Practice: Database with persistent storage

- **Day 6:** Docker best practices
  - Image optimization
  - Security considerations
  - .dockerignore

- **Day 7:** Project
  - Containerize your ETL pipeline
  - Docker Compose with Airflow
  - Multi-service setup

---

### Week 19: Streaming Data & Real-time Processing
**Goal:** Handle real-time data

**Daily Tasks:**
- **Day 1:** Streaming concepts
  - Batch vs streaming
  - Event-driven architecture
  - Message brokers
  - Use cases

- **Day 2:** Apache Kafka basics
  - Install Kafka locally
  - Topics, partitions, brokers
  - Producers and consumers
  - Practice: Hello World Kafka

- **Day 3:** Kafka with Python
  - confluent-kafka-python
  - Producing messages
  - Consuming messages
  - Practice: Stream processing

- **Day 4:** Stream processing patterns
  - Windowing
  - Aggregations
  - Joins
  - Practice: Real-time analytics

- **Day 5:** AWS Kinesis hands-on
  - Kinesis Data Streams
  - Kinesis Data Firehose
  - Lambda consumer
  - Practice: Stream to S3/Redshift

- **Day 6:** Change Data Capture (CDC)
  - Database replication
  - Debezium concepts
  - Event sourcing

- **Day 7:** Project
  - Build: Real-time pipeline
  - Generate streaming data
  - Process and aggregate
  - Store results

---

### Week 20: Testing & Data Quality
**Goal:** Build reliable pipelines

**Daily Tasks:**
- **Day 1:** Unit testing Python
  - pytest basics
  - Writing test cases
  - Test coverage
  - Practice: Test your functions

- **Day 2:** Testing data pipelines
  - Testing ETL logic
  - Mocking data sources
  - Integration tests
  - Practice: Test your pipelines

- **Day 3:** Great Expectations
  - Data validation library
  - Expectations and suites
  - Data quality checks
  - Practice: Validate datasets

- **Day 4:** Data quality framework
  - Schema validation
  - Completeness checks
  - Accuracy checks
  - Practice: Build quality checks

- **Day 5:** Logging and monitoring
  - Python logging module
  - Structured logging
  - Log aggregation
  - Practice: Add comprehensive logging

- **Day 6:** CI/CD basics
  - GitHub Actions
  - Automated testing
  - Deployment pipelines
  - Practice: Set up CI for your projects

- **Day 7:** Review & refactor
  - Code review your projects
  - Add tests and documentation
  - Implement quality checks

**Milestone:** Production-ready skills

---

## Phase 4: Portfolio Projects & Job Prep (Weeks 21-26)

### Week 21-22: Project 1 - E-commerce Analytics Pipeline
**Goal:** Build end-to-end batch processing pipeline

**Project Scope:**
- **Data sources:** 
  - E-commerce transaction data (CSV files)
  - Product catalog API
  - Customer data from PostgreSQL
  
- **Requirements:**
  - Extract data from multiple sources
  - Clean and transform data
  - Implement SCD Type 2 for customers
  - Load into dimensional data warehouse
  - Schedule daily with Airflow
  - Data quality checks
  - Generate daily reports

- **Tech Stack:**
  - Python (pandas, SQLAlchemy)
  - PostgreSQL / AWS Redshift
  - Apache Airflow
  - Docker
  - AWS S3
  - Great Expectations

- **Week 21:** Build core pipeline
- **Week 22:** Add monitoring, testing, documentation

**Deliverables:**
- GitHub repository with clean code
- Comprehensive README
- Architecture diagram
- Sample dashboard/report

---

### Week 23-24: Project 2 - Real-time Data Streaming
**Goal:** Build streaming data pipeline

**Project Scope:**
- **Data source:**
  - Simulate real-time events (e-commerce clicks, IoT sensors, etc.)
  - Twitter/social media API (alternative)
  
- **Requirements:**
  - Stream ingestion (Kafka or Kinesis)
  - Real-time processing and aggregation
  - Windowed analytics
  - Store in time-series database
  - Real-time dashboard
  - Handle late data and reprocessing

- **Tech Stack:**
  - Apache Kafka or AWS Kinesis
  - Python streaming processors
  - AWS Lambda
  - DynamoDB or TimescaleDB
  - CloudWatch dashboards

- **Week 23:** Build streaming infrastructure
- **Week 24:** Add analytics, visualization, optimization

**Deliverables:**
- End-to-end streaming system
- Performance metrics
- Detailed documentation

---

### Week 25: Project 3 - API Data Integration Platform
**Goal:** Multi-source data integration

**Project Scope:**
- **Data sources:**
  - 3-5 public APIs (weather, finance, social media, etc.)
  - Web scraping (news sites, etc.)
  
- **Requirements:**
  - API client library/framework
  - Rate limiting and retry logic
  - Incremental loading
  - Data normalization
  - Historical data storage (Data Lake)
  - Query interface
  - Automated scheduling

- **Tech Stack:**
  - Python (requests, BeautifulSoup)
  - AWS S3 (Data Lake)
  - AWS Glue (cataloging)
  - Athena (querying)
  - Airflow (orchestration)

**Deliverables:**
- Reusable API integration framework
- Multiple working integrations
- Query interface

---

### Week 26: Portfolio Polish & Job Applications

**Day 1-2: GitHub Portfolio Optimization**
- Clean up all repositories
- Professional README files
- Add screenshots/diagrams
- Ensure code quality
- Add comprehensive documentation

**Day 3: Resume & LinkedIn**
- Update resume with DE projects
- Highlight transferable skills from Magento
- Optimize LinkedIn profile
- Add certifications/courses completed
- Get 2-3 recommendations

**Day 4-5: Interview Preparation**
- Review SQL interview questions
- Python coding challenges
- System design basics
- Behavioral questions (STAR method)
- Mock interviews

**Day 6-7: Job Applications**
- Identify 20+ target companies
- Customize resume for each
- Write cover letters emphasizing transition
- Apply to positions
- Network on LinkedIn

---

## Bonus Topics (As Needed)

### Data Visualization
- Matplotlib, Seaborn basics
- Plotly for interactive viz
- Tableau/Power BI (if required by jobs)

### Spark & Big Data
- PySpark fundamentals
- DataFrames and SQL
- Spark on AWS EMR

### Advanced SQL
- Query optimization
- Explain plans
- Indexes and performance tuning

### dbt (Data Build Tool)
- Analytics engineering
- Transformation in warehouse
- Testing and documentation

### Infrastructure as Code
- Terraform basics
- AWS CloudFormation
- Version-controlled infrastructure

---

## Success Metrics Tracking

### Technical Skills Checklist
- [ ] 150+ SQL problems solved
- [ ] 100+ Python programs written
- [ ] 10+ Airflow DAGs created
- [ ] 5+ AWS services hands-on
- [ ] 3 complete portfolio projects
- [ ] CI/CD pipeline implemented
- [ ] Data quality framework built

### Professional Development
- [ ] GitHub: 26+ weeks of consistent activity
- [ ] LinkedIn: Profile complete and optimized
- [ ] Network: 20+ DE connections
- [ ] Resume: Updated with projects
- [ ] Interview: Practiced 50+ questions
- [ ] Applications: 20+ submitted

---

## Weekly Review Template

**End of each week, reflect on:**

1. **What did I learn?** (Key concepts)
2. **What did I build?** (Projects/code)
3. **What challenges did I face?** (Blockers)
4. **What's my confidence level?** (1-10)
5. **What's next week's focus?**
6. **Hours spent:** (Track actual time)

---

**Remember:** This is a marathon, not a sprint. Consistency beats intensity. Even 1-2 hours daily adds up to massive progress!

**Good luck on your Data Engineering journey! 🚀**

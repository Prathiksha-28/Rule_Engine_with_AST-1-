# Rule_Engine_with_AST-1-

## Description
This is a 3-tier rule engine application designed to determine user eligibility based on attributes such as age, department, income, and experience. The system utilizes an Abstract Syntax Tree (AST) to represent and evaluate conditional rules dynamically. 

## Design Choices
- **AST Representation**: Each rule is represented as a Node in an AST, enabling flexible rule creation, modification, and evaluation.
- **Database**: PostgreSQL is used for storing rules and metadata, providing robust querying capabilities.
- **API Layer**: A RESTful API exposes endpoints for rule creation, combination, and evaluation, ensuring a clear separation of concerns.

## Build Instructions
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/rule-engine.git
   cd rule-engine
   
## Build and run the Docker Containers
   docker-compose up --build
   
## Access API at: http://localhost:5000

## Docker Setup
``markdown
- **Dockerfile**: Defines the application container build process.
- **docker-compose.yml**: Sets up services, including the API and PostgreSQL database.

#### API Endpoints
- `POST /create_rule`: Create a new rule from a rule string.
- `POST /combine_rules`: Combine multiple rules into a single AST.
- `POST /evaluate_rule`: Evaluate an AST against provided user data.

#### Dependencies
```markdown
- Python 3.x
- Flask
- SQLAlchemy
- psycopg2
- Docker (for containerization)
- PostgreSQL

To install Python dependencies, run:
````
pip install -r requirements.txt

#### Testing
To run tests, ensure you have `pytest` installed. Execute:
```bash
pytest tests/
#### Sample JSON Data for Testing
```json
{
    "age": 35,
    "department": "Sales",
    "salary": 60000,
    "experience": 3
}





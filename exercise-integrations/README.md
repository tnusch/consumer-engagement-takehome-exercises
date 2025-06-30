### 3. Senior Engineer – Marketing Integrations & APIs  
#### Exercise: Develop an API that syncs user profile data to a mock third-party marketing platform with basic validation and transformation logic.

#### 1. Build the Profile Sync API  
Develop a simple REST API that accepts a **batch of user profiles** (e.g., JSON array) via a POST request. Each profile should contain fields such as:
- Email address  
- First name and last name  
- Optional metadata (e.g., tags, preferences)

#### 2. Implement Basic Logic  
Your API should include the following features:
- ✅ **Email validation**: Filter out invalid email addresses (e.g., missing `@` or domain)  
- ✅ **Name normalization**: Ensure first and last names are capitalized correctly (e.g., `john doe` → `John Doe`)  
- ✅ **Logging as mock integration**: Simulate a third-party API call by logging the outgoing transformed data (no real API call required)

#### 3. Document Your Work  
Provide documentation that is understandable by both:
- **Technical stakeholders**: Describe API design, structure, data flow, and any edge-case handling  
- **Non-technical stakeholders**: Explain the purpose of the API, the types of data it processes, and how it fits into a marketing use case

You can include this documentation as:
- A `README.md` section
- A separate `docs/` folder (if preferred)
- Diagrams or flowcharts (optional but welcome)

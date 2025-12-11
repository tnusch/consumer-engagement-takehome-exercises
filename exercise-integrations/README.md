### 3. Senior Engineer – Marketing Integrations & APIs  
#### Exercise: Develop an API that syncs user profile data to a mock third-party marketing platform with basic validation and transformation logic.

#### 1. Build a Minimal Profile Sync API
Create a small service that exposes a POST endpoint accepting a batch of user profiles (JSON array).
Each profile must contain:
- Email address  
- First name and last name  
- Optional metadata (e.g., tags, preferences)

Requirements:
- Validate email format
- Normalize names (capitalize properly)
- Log the final payload as a stand-in for a third-party marketing API call

#### 2. Error handling & retry strategy (conceptual & light implementation)
A. Retry Strategy (Conceptual)
Define a practical retry strategy for when the third-party platform fails.
You do not need to implement retries in code - instead:
- Describe when to retry, when not to retry, and why
- Define backoff behavior
- Identify risks of retry storms and how you'd prevent them
- Explain how retries would interact with batch processing

B. Error Classification & Handling (Light Implementation + Reasoning)
Implement a simple mechanism to classify errors into:
- Client errors (invalid input)
- Server errors (temporary failure, retryable)
- Unexpected faults
And provide a short explanation of how your classification supports observability, debugging, and reliability.

#### 3. Telemetry & Quality Signals (Design Only)
Instead of implementing full logging/metrics/tracing, provide a brief plan (max 10 bullet points) describing:
- Which logs would be emitted at each stage
- Which metrics you would track (e.g., invalid email ratio, batch size, integration failures)
- One example of what you would trace and why
- How the above signals help detect issues before they impact downstream users

#### 4. Document Your Work
Provide a concise, readable explanation for two audiences:
**Technical Audience**
Explain:
- Your API structure
- How you handle validation & transformation
- Your retry and error-handling reasoning
- Your telemetry plan
**Non-Technical Audience**
Explain (3–5 sentences):
- What this service does
- Why validating and transforming user data matters
- Why stable integrations are important for our digital consumer experience

### 3. Senior Engineer – Marketing Integrations & APIs  
**Exercise: Build a small service that accepts user profile submissions, performs basic validation, and forwards them synchronously to a downstream system that is rate-limited. The focus is on API design, batching strategy, and handling throughput pressure without external queue technologies.**

#### 1. Profile Submission API

Expose a POST endpoint accepting a JSON object containing:
- email
- firstName
- lastName
Optional metadata (e.g., tags, preferences, or other free-form fields)

Requirements:

- Validate the submitted data. (Validation rules are intentionally ambiguous—use your judgment and document your reasoning.)
- Return 400 for invalid submissions.
- Log the final payload (simulating a call to an upstream marketing platform).

#### 1b. Downstream Submission Logic
For each incoming profile, the service must forward the data to a downstream API synchronously. The downstream API has the following constraints:
- At most 5 requests per second
- Profiles may be batched together in a single request (feel free to decide a convenient payload format)

Additional Requirements:

- Incoming submissions may arrive at ~500 requests per second
- You may NOT use any external queueing technology (e.g., no Redis/Kafka/Pub/Sub/SQS)
- You may use in-memory data structures to implement batching or rate limiting
- The client calling your POST endpoint must wait for the downstream submission to complete before receiving a response
  
Response Behavior:

Your endpoint should return a JSON response indicating whether the profile:
- was successfully forwarded to the downstream service, or
- could not be forwarded (include an error message)

#### 2. Error handling & retry strategy (conceptual & light implementation)

A. Retry Strategy (Conceptual)

Define a practical retry strategy for when the third-party platform fails.

B. Error Classification & Handling (Light Implementation + Reasoning)

Implement a simple mechanism to classify errors.
Provide a short explanation of how your classification supports observability, debugging, and reliability.

#### 3. Document Your Work
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

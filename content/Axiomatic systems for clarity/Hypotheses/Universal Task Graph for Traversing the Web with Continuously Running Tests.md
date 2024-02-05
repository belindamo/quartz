
**Problem**:
- Ensuring the reliability of AI-powered browser automation responses, regardless of the method used.
- Current reliance on human monitoring for successful task completion, even for AI assistant tools.

**Proposed Flip**:
- Transitioning responsibility from human monitoring of an AI instance to no monitoring of an AI instance for task verification, by continuously running tests and updating task script based on changes. 

**Solution**:
- Implement AI-driven automation for web traversal, adaptable for various applications, with continuous testing to ensure functionality.

**Methodology**:
1. Utilize a large language model for AI-generated automation in website traversal. The generated automation code is suitable for both cloud and local deployment, and can also be used to generate validation tests.
2. Catch errors before users run into them by conducting 24/7 validation tests that detect diffs, (Github Actions? VM?) to ensure task consistency and functionality. 
3. Automate AI regeneration of browser automation upon test failures. (Probably need some manual revision)
4. Future: enable crowdsourced task generation and submission.

**Evaluation Metrics**:
- Ability to detect diffs in continuous testing.
- Ability to filter trivial diffs from ones that indicate that a task automation has broken 
- Success rate of AI script regeneration *after the first automation for that task works* (initial target ≥ 90%).
- Effectiveness on sites with sensitive information or bot detection.

**Implications**:
- Scalability from single to thousands of tasks, with potential for crowdsourcing tasks and community maintenance. 

**Related Works**:
- MultiON: An assistant platform.
- Selenium and Puppeteer: Tools for browser automation.

**Evaluation Plan**:
- **Independent Variable (IV)**: AI in browser automation creation and continuous testing setup.
- **Dependent Variable (DV)**: Task effectiveness without user intervention.
- **Potential Threats**: 
	- Inability to capture all errors in tests and AI-generated tree.
	- What happens when specific user information is needed, while doing automation? like login info.


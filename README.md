# UiPath Eugene -- AI-Powered Email Customer Support Agent

**UiPath Eugene** is an AI-powered email support agent built with
UiPath. It answers technical questions about UiPath by searching and
retrieving relevant information from the UiPath Forum, then replying to
incoming emails automatically.

The solution uses an event-based Gmail trigger and an agentic process
designed in **UiPath Maestro**. When Eugene cannot confidently answer a
question, or when the sender requests a human, it escalates the
conversation to a human support person.

## Demo

> **Demo video:** Add your demo video link here.

The demonstration shows an email arriving with **"Hi Eugene"** in the
message body. The Gmail event trigger starts the process, and Eugene
responds to the email within seconds.

## Screenshots

### Project deployed in Orchestrator
![Project in Orchestrator](Output%20Screenshots/project_in_orchestrator.png)

### BPMN design view (UiPath Maestro)
![BPMN design view](Output%20Screenshots/bpmn_design_view.png)

### AI Agent design view (Studio Web)
![Agent design view](Output%20Screenshots/agent_design_view.png)

### Email examples

<table>
  <tr>
    <td align="center"><a href="Output%20Screenshots/sent_mail_na.jpg"><img src="Output%20Screenshots/sent_mail_na.jpg" width="240" alt="Sent mail NA"></a>
    <td align="center"><a href="Output%20Screenshots/sent_mail_maestro.jpg"><img src="Output%20Screenshots/sent_mail_maestro.jpg" width="240" alt="Sent mail Maestro"></a>
    <td align="center"><a href="Output%20Screenshots/sent_mail_agentic.jpg"><img src="Output%20Screenshots/sent_mail_agentic.jpg" width="240" alt="Sent mail Agentic"></a>
    <td align="center"><a href="Output%20Screenshots/fwd_mail_fred.jpg"><img src="Output%20Screenshots/fwd_mail_fred.jpg" width="240" alt="Forwarded mail"></a>
  </tr>
</table>

_Click any thumbnail to view it full size._

## Key Features

-   **Event-based email trigger:** Starts the workflow when a new email
    is received in the connected Gmail inbox.
-   **AI-powered responses:** Uses an AI Agent powered by an OpenAI LLM
    to answer technical UiPath questions.
-   **UiPath Forum research:** Searches and scrapes relevant UiPath
    Forum content through the agent's tools.
-   **Context grounding:** Uses relevant UiPath documentation and Forum
    content to help keep answers focused and reliable.
-   **Automatic email handling:** Reads incoming emails and sends
    personalized replies.
-   **Human escalation:** Forwards a request to a human when Eugene is
    not confident or when the sender asks for human assistance.
-   **Clear escalation communication:** Informs the sender that a human
    will respond within 24 hours.
-   **HTML email responses:** Formats generated replies as HTML using
    dynamic placeholders.
-   **Monitoring and evaluation:** Uses agent instances, fault
    debugging, Evaluation Sets, and Agent Score to assess and improve
    response quality.

## How It Works

1.  A user sends an email to the connected Gmail inbox.
2.  The Gmail webhook/event trigger detects the incoming message.
3.  The UiPath Maestro process starts and passes the email details to
    the AI Agent.
4.  **UiPath Eugene** interprets the question and uses its available
    tools to search and retrieve relevant UiPath Forum information.
5.  The agent prepares a response grounded in the retrieved context.
6.  The process follows the appropriate route:
    -   **Automatic response:** Eugene sends an HTML-formatted email
        when it can provide a suitable answer.
    -   **Human escalation:** If Eugene is not confident, or the sender
        requests assistance by including **"Speak to human"**, the email
        is forwarded to a human. The sender is informed that a human
        will respond within 24 hours.

## Technology and UiPath Components

-   UiPath Studio Web -- AI Agent creation and configuration
-   UiPath Maestro -- Agentic process and BPMN workflow orchestration
-   UiPath Orchestrator -- Deployment, versioning, and process/agent
    management
-   Gmail integration -- Email trigger, reading, replying, and
    forwarding
-   OpenAI LLM -- Language model powering the AI Agent
-   UiPath Forum -- Knowledge source for technical support answers

## Skills Demonstrated

-   Designed an agentic BPMN process in UiPath Maestro for email
    customer support.
-   Created and configured an AI Agent in UiPath Studio Web, including
    its tasks and tools.
-   Developed system and user prompts to define the agent's tone,
    behavior, and domain focus.
-   Applied context grounding using UiPath documentation and Forum
    content.
-   Integrated Gmail to read, reply to, and forward emails.
-   Implemented decision logic for automated replies and human
    escalation.
-   Generated HTML email responses with dynamic placeholders.
-   Deployed, versioned, and updated the agentic process and AI Agent
    through Orchestrator and Maestro.
-   Tested and debugged agent instances and faults.
-   Explored Evaluation Sets and Agent Score to evaluate response
    quality and improve the agent.

## Project Structure

``` text
Robot-6-Email-Customer-Support-Agentic-AI/
├── Output Screenshots/
├── My_Agent_Prompt.txt
├── UiPath Email Support.uis
└── README.md
```

## Setup and Configuration

This project depends on UiPath services and connected accounts. To run
or adapt it:

1.  Clone or download this repository.
2.  Open the UiPath project in the appropriate UiPath Studio Web
    environment.
3.  Configure the required AI Agent and its tools.
4.  Connect the Gmail account and configure the email event trigger.
5.  Configure access to the UiPath Forum and any documentation sources
    used for grounding.
6.  Configure the OpenAI LLM connection using the credentials and
    settings required by your environment.
7.  Publish and deploy the agentic process through UiPath
    Orchestrator/Maestro.
8.  Test both the automatic-reply and human-escalation paths before
    using it with real support emails.

**Important:** Do not commit passwords, API keys, OAuth tokens, or other
secrets to this repository. Store credentials using the approved secure
credential or connection mechanisms in your UiPath environment.

## Example Trigger and Escalation

-   **Example trigger phrase:** `Hi Eugene`
-   **Human escalation phrase:** `Speak to human`
-   **Human response expectation communicated to the sender:** Within 24
    hours

These phrases describe the behavior demonstrated in this project; update
the prompts and workflow conditions if you change the trigger or
escalation rules.

## Notes

-   AI-generated answers should be reviewed and tested for accuracy
    before the agent is used in a production support environment.
-   The quality of responses depends on the agent instructions,
    retrieved source content, tool configuration, and LLM behavior.
-   Ensure that Gmail permissions and any connected service permissions
    follow your organization's security policies.

## Author

**Mustaq Shaik**

GitHub: [Shaik-Mustaq](https://github.com/Shaik-Mustaq)

## Repository

[Robot-6-Email-Customer-Support-Agentic-AI](https://github.com/Shaik-Mustaq/Robot-6-Email-Customer-Support-Agentic-AI)

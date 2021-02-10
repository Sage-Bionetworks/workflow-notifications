# workflow notifications

Rough plan (via Tess):

> 1. Create a Cloudwatch metric filter: this allows one to match patterns in logs. I think I already know what text patterns to look for.
> 2. Create a Cloudwatch alarm for the metric.
> 3. Create an SNS topic to associate with the alarm. The SNS topic can send the email notification.

Examples of strings that need to be matched:
```
WorkflowManagerActor Successfully started WorkflowActor-9fe6be70-e9da-4118-a5f6-19e5e9034f10

WorkflowManagerActor WorkflowActor-f7a73cc0-facd-4b13-b388-9e4134a14ada is in a terminal state: WorkflowSucceededState

WorkflowManagerActor WorkflowActor-dfcc9038-dd6d-4862-9494-30ff1fcfc24f is in a terminal state: WorkflowFailedState

WorkflowManagerActor WorkflowActor-f9c2e596-63c2-45f4-9087-4c803add1b56 is in a terminal state: WorkflowAbortedState
```

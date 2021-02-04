# workflow notifications

Rough plan (via Tess):

> 1. Create a Cloudwatch metric filter: this allows one to match patterns in logs. I think I already know what text patterns to look for.
> 2. Create a Cloudwatch alarm for the metric.
> 3. Create an SNS topic to associate with the alarm. The SNS topic can send the email notification.


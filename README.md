# Sumologic Orb
https://circleci.com/orbs/registry/orb/circleci/sumologic

Easily capture analytics from your CircleCI jobs in your Sumologic dashboard!

## job-collector
Add this command to your job with environment, team or service custom-data values as parameters. This command will run with the rest of the commands of the job for sending job log. This command has been introduced so as to send environment, team and service information at job level. If this command is not included at job level in one of it's steps, then the workflow-collector job will send the job log. Avoiding this command or using it without the parameters will result in empty custom-data values being sent to Sumo.

## workflow-collector
Add this job to your workflow with no require statements. This job will run in parallel with the rest of your workflow for monitoring and will exit when all other jobs have completed. Custom data can be supplied via the custom-data parameter in the form of valid JSON. Keys and values can be supplied literally or as environment variables, though supplying values as additional, nested JSON is not supported. Passing the custom-data parameter as a folded-style (>) block scalar is recommended (see examples).


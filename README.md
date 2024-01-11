remove-aws-resources
aws-nuke is a powerful open-source tool used for cleaning up and deleting AWS resources in an AWS account. It's designed to be a safety-first resource nuker, meaning it requires explicit configuration to delete resources and is not intended for casual use.

install aws-nuke: apt-get -y install aws-nuke

write the config file in yaml ( already in the repo with name nuke-config-yml)

create aws account alias by following steps: Open the AWS Management Console: Log in to the AWS Management Console using the credentials associated with your AWS account. Navigate to IAM (Identity and Access Management): Go to the IAM dashboard. Choose "Dashboard" in IAM: On the IAM dashboard, there should be a section called "Account settings." Edit the Account Alias: Look for an option to "Change the account alias." Enter an alias that includes the term 'prod' (e.g., mycompany-prod). Save Changes: Save the changes.

run the config file with the command: aws-nuke -c nuke-config.yml --access-key-id PassAccessKeyHere --secret-access-key PassSecretKeyHere --no-dry-run

give the alias at confimation
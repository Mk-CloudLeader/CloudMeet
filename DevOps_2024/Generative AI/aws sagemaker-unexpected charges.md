
### Problem statement : Unexpected charges were incurred from the SageMaker service. You can view this by signing into the AWS Management Console and open the Billing console here: https://console.aws.amazon.com/billing/ 

- Choose Bills to see details about your current charges.

- To avoid incurring unnecessary charges, use the AWS Management Console to delete the **endpoints and resources** that you created while running the exercises.
  SageMaker --Under Inference, choose Endpoint--Action -Delete
            -- Under Notebook, choose Notebook instances --Actions-- --choose Stop--delete

- Delete an Amazon SageMaker Domain
    A Domain consists of a list of authorized users, configuration settings, and an  EFS volume
  SageMaker --Admin configurations---choose Domains --User profiles list--From the dropdown list, choose Delete.

  aws --region Region sagemaker list-domains
  aws --region Region sagemaker delete-app \
    --domain-id DomainId \
    --app-name AppName \
    --app-type AppType \
    --user-profile-name UserProfileName
  
  
| Link | https://docs.aws.amazon.com/sagemaker/latest/dg/ex1-cleanup.html|
| Link | https://docs.aws.amazon.com/sagemaker/latest/dg/gs-studio-delete-domain.html#gs-studio-delete-domain-studio|

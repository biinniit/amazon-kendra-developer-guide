--------

--------

# UpdateExperience<a name="API_UpdateExperience"></a>

Updates your Amazon Kendra experience such as a search application\. For more information on creating a search application experience, see [Building a search experience with no code](https://docs.aws.amazon.com/kendra/latest/dg/deploying-search-experience-no-code.html)\.

## Request Syntax<a name="API_UpdateExperience_RequestSyntax"></a>

```
{
   "Configuration": { 
      "ContentSourceConfiguration": { 
         "DataSourceIds": [ "string" ],
         "DirectPutContent": boolean,
         "FaqIds": [ "string" ]
      },
      "UserIdentityConfiguration": { 
         "IdentityAttributeName": "string"
      }
   },
   "Description": "string",
   "Id": "string",
   "IndexId": "string",
   "Name": "string",
   "RoleArn": "string"
}
```

## Request Parameters<a name="API_UpdateExperience_RequestParameters"></a>

For information about the parameters that are common to all actions, see [Common Parameters](CommonParameters.md)\.

The request accepts the following data in JSON format\.

 ** [Configuration](#API_UpdateExperience_RequestSyntax) **   <a name="Kendra-UpdateExperience-request-Configuration"></a>
Configuration information for your Amazon Kendra you want to update\.  
Type: [ExperienceConfiguration](API_ExperienceConfiguration.md) object  
Required: No

 ** [Description](#API_UpdateExperience_RequestSyntax) **   <a name="Kendra-UpdateExperience-request-Description"></a>
The description of your Amazon Kendra experience you want to update\.  
Type: String  
Length Constraints: Minimum length of 0\. Maximum length of 1000\.  
Pattern: `^\P{C}*$`   
Required: No

 ** [Id](#API_UpdateExperience_RequestSyntax) **   <a name="Kendra-UpdateExperience-request-Id"></a>
The identifier of your Amazon Kendra experience you want to update\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*`   
Required: Yes

 ** [IndexId](#API_UpdateExperience_RequestSyntax) **   <a name="Kendra-UpdateExperience-request-IndexId"></a>
The identifier of the index for your Amazon Kendra experience you want to update\.  
Type: String  
Length Constraints: Fixed length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9-]*`   
Required: Yes

 ** [Name](#API_UpdateExperience_RequestSyntax) **   <a name="Kendra-UpdateExperience-request-Name"></a>
The name of your Amazon Kendra experience you want to update\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 1000\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*`   
Required: No

 ** [RoleArn](#API_UpdateExperience_RequestSyntax) **   <a name="Kendra-UpdateExperience-request-RoleArn"></a>
The Amazon Resource Name \(ARN\) of a role with permission to access `Query` API, `QuerySuggestions` API, `SubmitFeedback` API, and AWS SSO that stores your user and group information\. For more information, see [IAM roles for Amazon Kendra](https://docs.aws.amazon.com/kendra/latest/dg/iam-roles.html)\.  
Type: String  
Length Constraints: Minimum length of 0\. Maximum length of 1284\.  
Pattern: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`   
Required: No

## Response Elements<a name="API_UpdateExperience_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response with an empty HTTP body\.

## Errors<a name="API_UpdateExperience_Errors"></a>

For information about the errors that are common to all actions, see [Common Errors](CommonErrors.md)\.

 ** AccessDeniedException **   
  
HTTP Status Code: 400

 ** ConflictException **   
  
HTTP Status Code: 400

 ** InternalServerException **   
  
HTTP Status Code: 500

 ** ResourceNotFoundException **   
  
HTTP Status Code: 400

 ** ThrottlingException **   
  
HTTP Status Code: 400

 ** ValidationException **   
  
HTTP Status Code: 400

## See Also<a name="API_UpdateExperience_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS Command Line Interface](https://docs.aws.amazon.com/goto/aws-cli/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for \.NET](https://docs.aws.amazon.com/goto/DotNetSDKV3/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for JavaScript](https://docs.aws.amazon.com/goto/AWSJavaScriptSDK/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for PHP V3](https://docs.aws.amazon.com/goto/SdkForPHPV3/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for Python](https://docs.aws.amazon.com/goto/boto3/kendra-2019-02-03/UpdateExperience) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/UpdateExperience) 
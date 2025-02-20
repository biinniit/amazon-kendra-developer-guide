--------

--------

# ListExperienceEntities<a name="API_ListExperienceEntities"></a>

Lists users or groups in your AWS SSO identity source that are granted access to your Amazon Kendra experience\. You can create an Amazon Kendra experience such as a search application\. For more information on creating a search application experience, see [Building a search experience with no code](https://docs.aws.amazon.com/kendra/latest/dg/deploying-search-experience-no-code.html)\.

## Request Syntax<a name="API_ListExperienceEntities_RequestSyntax"></a>

```
{
   "Id": "string",
   "IndexId": "string",
   "NextToken": "string"
}
```

## Request Parameters<a name="API_ListExperienceEntities_RequestParameters"></a>

For information about the parameters that are common to all actions, see [Common Parameters](CommonParameters.md)\.

The request accepts the following data in JSON format\.

 ** [Id](#API_ListExperienceEntities_RequestSyntax) **   <a name="Kendra-ListExperienceEntities-request-Id"></a>
The identifier of your Amazon Kendra experience\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*`   
Required: Yes

 ** [IndexId](#API_ListExperienceEntities_RequestSyntax) **   <a name="Kendra-ListExperienceEntities-request-IndexId"></a>
The identifier of the index for your Amazon Kendra experience\.  
Type: String  
Length Constraints: Fixed length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9-]*`   
Required: Yes

 ** [NextToken](#API_ListExperienceEntities_RequestSyntax) **   <a name="Kendra-ListExperienceEntities-request-NextToken"></a>
If the previous response was incomplete \(because there is more data to retrieve\), Amazon Kendra returns a pagination token in the response\. You can use this pagination token to retrieve the next set of users or groups\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 800\.  
Required: No

## Response Syntax<a name="API_ListExperienceEntities_ResponseSyntax"></a>

```
{
   "NextToken": "string",
   "SummaryItems": [ 
      { 
         "DisplayData": { 
            "FirstName": "string",
            "GroupName": "string",
            "IdentifiedUserName": "string",
            "LastName": "string",
            "UserName": "string"
         },
         "EntityId": "string",
         "EntityType": "string"
      }
   ]
}
```

## Response Elements<a name="API_ListExperienceEntities_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response\.

The following data is returned in JSON format by the service\.

 ** [NextToken](#API_ListExperienceEntities_ResponseSyntax) **   <a name="Kendra-ListExperienceEntities-response-NextToken"></a>
If the response is truncated, Amazon Kendra returns this token, which you can use in a later request to retrieve the next set of users or groups\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 800\.

 ** [SummaryItems](#API_ListExperienceEntities_ResponseSyntax) **   <a name="Kendra-ListExperienceEntities-response-SummaryItems"></a>
An array of summary information for one or more users or groups\.  
Type: Array of [ExperienceEntitiesSummary](API_ExperienceEntitiesSummary.md) objects

## Errors<a name="API_ListExperienceEntities_Errors"></a>

For information about the errors that are common to all actions, see [Common Errors](CommonErrors.md)\.

 ** AccessDeniedException **   
  
HTTP Status Code: 400

 ** InternalServerException **   
  
HTTP Status Code: 500

 ** ResourceNotFoundException **   
  
HTTP Status Code: 400

 ** ThrottlingException **   
  
HTTP Status Code: 400

 ** ValidationException **   
  
HTTP Status Code: 400

## See Also<a name="API_ListExperienceEntities_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS Command Line Interface](https://docs.aws.amazon.com/goto/aws-cli/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for \.NET](https://docs.aws.amazon.com/goto/DotNetSDKV3/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for JavaScript](https://docs.aws.amazon.com/goto/AWSJavaScriptSDK/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for PHP V3](https://docs.aws.amazon.com/goto/SdkForPHPV3/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for Python](https://docs.aws.amazon.com/goto/boto3/kendra-2019-02-03/ListExperienceEntities) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/ListExperienceEntities) 
--------

--------

# ServiceNowConfiguration<a name="API_ServiceNowConfiguration"></a>

Provides the configuration information to connect to ServiceNow as your data source\.

## Contents<a name="API_ServiceNowConfiguration_Contents"></a>

 ** AuthenticationType **   <a name="Kendra-Type-ServiceNowConfiguration-AuthenticationType"></a>
The type of authentication used to connect to the ServiceNow instance\. If you choose `HTTP_BASIC`, Amazon Kendra is authenticated using the user name and password provided in the AWS Secrets Manager secret in the `SecretArn` field\. When you choose `OAUTH2`, Amazon Kendra is authenticated using the OAuth token and secret provided in the Secrets Manager secret, and the user name and password are used to determine which information Amazon Kendra has access to\.  
When you use `OAUTH2` authentication, you must generate a token and a client secret using the ServiceNow console\. For more information, see [Using a ServiceNow data source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-servicenow.html)\.  
Type: String  
Valid Values:` HTTP_BASIC | OAUTH2`   
Required: No

 ** HostUrl **   <a name="Kendra-Type-ServiceNowConfiguration-HostUrl"></a>
The ServiceNow instance that the data source connects to\. The host endpoint should look like the following: *\{instance\}\.service\-now\.com\.*   
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 2048\.  
Pattern: `^(?!(^(https?|ftp|file):\/\/))[a-z0-9-]+(\.service-now\.com)$`   
Required: Yes

 ** KnowledgeArticleConfiguration **   <a name="Kendra-Type-ServiceNowConfiguration-KnowledgeArticleConfiguration"></a>
Configuration information for crawling knowledge articles in the ServiceNow site\.  
Type: [ServiceNowKnowledgeArticleConfiguration](API_ServiceNowKnowledgeArticleConfiguration.md) object  
Required: No

 ** SecretArn **   <a name="Kendra-Type-ServiceNowConfiguration-SecretArn"></a>
The Amazon Resource Name \(ARN\) of the AWS Secrets Manager secret that contains the user name and password required to connect to the ServiceNow instance\. You can also provide OAuth authentication credentials of user name, password, client ID, and client secret\. For more information, see [Authentication for a ServiceNow data source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-servicenow.html#servicenow-authentication)\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 1284\.  
Pattern: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`   
Required: Yes

 ** ServiceCatalogConfiguration **   <a name="Kendra-Type-ServiceNowConfiguration-ServiceCatalogConfiguration"></a>
Configuration information for crawling service catalogs in the ServiceNow site\.  
Type: [ServiceNowServiceCatalogConfiguration](API_ServiceNowServiceCatalogConfiguration.md) object  
Required: No

 ** ServiceNowBuildVersion **   <a name="Kendra-Type-ServiceNowConfiguration-ServiceNowBuildVersion"></a>
The identifier of the release that the ServiceNow host is running\. If the host is not running the `LONDON` release, use `OTHERS`\.  
Type: String  
Valid Values:` LONDON | OTHERS`   
Required: Yes

## See Also<a name="API_ServiceNowConfiguration_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/ServiceNowConfiguration) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/ServiceNowConfiguration) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/ServiceNowConfiguration) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/ServiceNowConfiguration) 
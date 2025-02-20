--------

--------

# SharePointConfiguration<a name="API_SharePointConfiguration"></a>

Provides the configuration information to connect to Microsoft SharePoint as your data source\.

## Contents<a name="API_SharePointConfiguration_Contents"></a>

 ** CrawlAttachments **   <a name="Kendra-Type-SharePointConfiguration-CrawlAttachments"></a>
 `TRUE` to index document attachments\.  
Type: Boolean  
Required: No

 ** DisableLocalGroups **   <a name="Kendra-Type-SharePointConfiguration-DisableLocalGroups"></a>
 `TRUE` to disable local groups information\.  
Type: Boolean  
Required: No

 ** DocumentTitleFieldName **   <a name="Kendra-Type-SharePointConfiguration-DocumentTitleFieldName"></a>
The Microsoft SharePoint attribute field that contains the title of the document\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 100\.  
Pattern: `^[a-zA-Z][a-zA-Z0-9_.]*$`   
Required: No

 ** ExclusionPatterns **   <a name="Kendra-Type-SharePointConfiguration-ExclusionPatterns"></a>
A list of regular expression patterns to exclude certain documents in your SharePoint\. Documents that match the patterns are excluded from the index\. Documents that don't match the patterns are included in the index\. If a document matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the document isn't included in the index\.  
The regex applies to the display URL of the SharePoint document\.  
Type: Array of strings  
Array Members: Minimum number of 0 items\. Maximum number of 100 items\.  
Length Constraints: Minimum length of 1\. Maximum length of 150\.  
Required: No

 ** FieldMappings **   <a name="Kendra-Type-SharePointConfiguration-FieldMappings"></a>
A list of `DataSourceToIndexFieldMapping` objects that map SharePoint data source attributes or field names to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to SharePoint fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The SharePoint data source field names must exist in your SharePoint custom metadata\.  
Type: Array of [DataSourceToIndexFieldMapping](API_DataSourceToIndexFieldMapping.md) objects  
Array Members: Minimum number of 1 item\. Maximum number of 100 items\.  
Required: No

 ** InclusionPatterns **   <a name="Kendra-Type-SharePointConfiguration-InclusionPatterns"></a>
A list of regular expression patterns to include certain documents in your SharePoint\. Documents that match the patterns are included in the index\. Documents that don't match the patterns are excluded from the index\. If a document matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the document isn't included in the index\.  
The regex applies to the display URL of the SharePoint document\.  
Type: Array of strings  
Array Members: Minimum number of 0 items\. Maximum number of 100 items\.  
Length Constraints: Minimum length of 1\. Maximum length of 150\.  
Required: No

 ** SecretArn **   <a name="Kendra-Type-SharePointConfiguration-SecretArn"></a>
The Amazon Resource Name \(ARN\) of an AWS Secrets Manager secret that contains the user name and password required to connect to the SharePoint instance\. If you use SharePoint Server, you also need to provide the sever domain name as part of the credentials\. For more information, see [Using a Microsoft SharePoint Data Source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-sharepoint.html)\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 1284\.  
Pattern: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`   
Required: Yes

 ** SharePointVersion **   <a name="Kendra-Type-SharePointConfiguration-SharePointVersion"></a>
The version of Microsoft SharePoint that you use\.  
Type: String  
Valid Values:` SHAREPOINT_2013 | SHAREPOINT_2016 | SHAREPOINT_ONLINE`   
Required: Yes

 ** SslCertificateS3Path **   <a name="Kendra-Type-SharePointConfiguration-SslCertificateS3Path"></a>
The path to the SSL certificate stored in an Amazon S3 bucket\. You use this to connect to SharePoint\.  
Type: [S3Path](API_S3Path.md) object  
Required: No

 ** Urls **   <a name="Kendra-Type-SharePointConfiguration-Urls"></a>
The Microsoft SharePoint site URLs for the documents you want to indext\.  
Type: Array of strings  
Array Members: Minimum number of 1 item\. Maximum number of 100 items\.  
Length Constraints: Minimum length of 1\. Maximum length of 2048\.  
Pattern: `^(https?|ftp|file):\/\/([^\s]*)`   
Required: Yes

 ** UseChangeLog **   <a name="Kendra-Type-SharePointConfiguration-UseChangeLog"></a>
 `TRUE` to use the SharePoint change log to determine which documents require updating in the index\. Depending on the change log's size, it may take longer for Amazon Kendra to use the change log than to scan all of your documents in SharePoint\.  
Type: Boolean  
Required: No

 ** VpcConfiguration **   <a name="Kendra-Type-SharePointConfiguration-VpcConfiguration"></a>
Configuration information for an Amazon Virtual Private Cloud to connect to your Microsoft SharePoint\. For more information, see [Configuring a VPC](https://docs.aws.amazon.com/kendra/latest/dg/vpc-configuration.html)\.  
Type: [DataSourceVpcConfiguration](API_DataSourceVpcConfiguration.md) object  
Required: No

## See Also<a name="API_SharePointConfiguration_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/SharePointConfiguration) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/SharePointConfiguration) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/SharePointConfiguration) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/SharePointConfiguration) 
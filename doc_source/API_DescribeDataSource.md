--------

--------

# DescribeDataSource<a name="API_DescribeDataSource"></a>

Gets information about an Amazon Kendra data source\.

## Request Syntax<a name="API_DescribeDataSource_RequestSyntax"></a>

```
{
   "Id": "string",
   "IndexId": "string"
}
```

## Request Parameters<a name="API_DescribeDataSource_RequestParameters"></a>

For information about the parameters that are common to all actions, see [Common Parameters](CommonParameters.md)\.

The request accepts the following data in JSON format\.

 ** [Id](#API_DescribeDataSource_RequestSyntax) **   <a name="Kendra-DescribeDataSource-request-Id"></a>
The unique identifier of the data source to describe\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 100\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*`   
Required: Yes

 ** [IndexId](#API_DescribeDataSource_RequestSyntax) **   <a name="Kendra-DescribeDataSource-request-IndexId"></a>
The identifier of the index that contains the data source\.  
Type: String  
Length Constraints: Fixed length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9-]*`   
Required: Yes

## Response Syntax<a name="API_DescribeDataSource_ResponseSyntax"></a>

```
{
   "Configuration": { 
      "AlfrescoConfiguration": { 
         "BlogFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "CrawlComments": boolean,
         "CrawlSystemFolders": boolean,
         "DocumentLibraryFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "EntityFilter": [ "string" ],
         "ExclusionPatterns": [ "string" ],
         "InclusionPatterns": [ "string" ],
         "SecretArn": "string",
         "SiteId": "string",
         "SiteUrl": "string",
         "SslCertificateS3Path": { 
            "Bucket": "string",
            "Key": "string"
         },
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         },
         "WikiFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ]
      },
      "BoxConfiguration": { 
         "CommentFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "CrawlComments": boolean,
         "CrawlTasks": boolean,
         "CrawlWebLinks": boolean,
         "EnterpriseId": "string",
         "ExclusionPatterns": [ "string" ],
         "FileFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "InclusionPatterns": [ "string" ],
         "SecretArn": "string",
         "TaskFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "UseChangeLog": boolean,
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         },
         "WebLinkFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ]
      },
      "ConfluenceConfiguration": { 
         "AttachmentConfiguration": { 
            "AttachmentFieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ],
            "CrawlAttachments": boolean
         },
         "BlogConfiguration": { 
            "BlogFieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ]
         },
         "ExclusionPatterns": [ "string" ],
         "InclusionPatterns": [ "string" ],
         "PageConfiguration": { 
            "PageFieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ]
         },
         "SecretArn": "string",
         "ServerUrl": "string",
         "SpaceConfiguration": { 
            "CrawlArchivedSpaces": boolean,
            "CrawlPersonalSpaces": boolean,
            "ExcludeSpaces": [ "string" ],
            "IncludeSpaces": [ "string" ],
            "SpaceFieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ]
         },
         "Version": "string",
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         }
      },
      "DatabaseConfiguration": { 
         "AclConfiguration": { 
            "AllowedGroupsColumnName": "string"
         },
         "ColumnConfiguration": { 
            "ChangeDetectingColumns": [ "string" ],
            "DocumentDataColumnName": "string",
            "DocumentIdColumnName": "string",
            "DocumentTitleColumnName": "string",
            "FieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ]
         },
         "ConnectionConfiguration": { 
            "DatabaseHost": "string",
            "DatabaseName": "string",
            "DatabasePort": number,
            "SecretArn": "string",
            "TableName": "string"
         },
         "DatabaseEngineType": "string",
         "SqlConfiguration": { 
            "QueryIdentifiersEnclosingOption": "string"
         },
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         }
      },
      "FsxConfiguration": { 
         "ExclusionPatterns": [ "string" ],
         "FieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "FileSystemId": "string",
         "FileSystemType": "string",
         "InclusionPatterns": [ "string" ],
         "SecretArn": "string",
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         }
      },
      "GitHubConfiguration": { 
         "ExclusionFileNamePatterns": [ "string" ],
         "ExclusionFileTypePatterns": [ "string" ],
         "ExclusionFolderNamePatterns": [ "string" ],
         "GitHubCommitConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "GitHubDocumentCrawlProperties": { 
            "CrawlIssue": boolean,
            "CrawlIssueComment": boolean,
            "CrawlIssueCommentAttachment": boolean,
            "CrawlPullRequest": boolean,
            "CrawlPullRequestComment": boolean,
            "CrawlPullRequestCommentAttachment": boolean,
            "CrawlRepositoryDocuments": boolean
         },
         "GitHubIssueAttachmentConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "GitHubIssueCommentConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "GitHubIssueDocumentConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "GitHubPullRequestCommentConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "GitHubPullRequestDocumentAttachmentConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "GitHubPullRequestDocumentConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "GitHubRepositoryConfigurationFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "InclusionFileNamePatterns": [ "string" ],
         "InclusionFileTypePatterns": [ "string" ],
         "InclusionFolderNamePatterns": [ "string" ],
         "OnPremiseConfiguration": { 
            "HostUrl": "string",
            "OrganizationName": "string",
            "SslCertificateS3Path": { 
               "Bucket": "string",
               "Key": "string"
            }
         },
         "RepositoryFilter": [ "string" ],
         "SaaSConfiguration": { 
            "HostUrl": "string",
            "OrganizationName": "string"
         },
         "SecretArn": "string",
         "Type": "string",
         "UseChangeLog": boolean,
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         }
      },
      "GoogleDriveConfiguration": { 
         "ExcludeMimeTypes": [ "string" ],
         "ExcludeSharedDrives": [ "string" ],
         "ExcludeUserAccounts": [ "string" ],
         "ExclusionPatterns": [ "string" ],
         "FieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "InclusionPatterns": [ "string" ],
         "SecretArn": "string"
      },
      "JiraConfiguration": { 
         "AttachmentFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "CommentFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "ExclusionPatterns": [ "string" ],
         "InclusionPatterns": [ "string" ],
         "IssueFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "IssueSubEntityFilter": [ "string" ],
         "IssueType": [ "string" ],
         "JiraAccountUrl": "string",
         "Project": [ "string" ],
         "ProjectFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "SecretArn": "string",
         "Status": [ "string" ],
         "UseChangeLog": boolean,
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         },
         "WorkLogFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ]
      },
      "OneDriveConfiguration": { 
         "DisableLocalGroups": boolean,
         "ExclusionPatterns": [ "string" ],
         "FieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "InclusionPatterns": [ "string" ],
         "OneDriveUsers": { 
            "OneDriveUserList": [ "string" ],
            "OneDriveUserS3Path": { 
               "Bucket": "string",
               "Key": "string"
            }
         },
         "SecretArn": "string",
         "TenantDomain": "string"
      },
      "QuipConfiguration": { 
         "AttachmentFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "CrawlAttachments": boolean,
         "CrawlChatRooms": boolean,
         "CrawlFileComments": boolean,
         "Domain": "string",
         "ExclusionPatterns": [ "string" ],
         "FolderIds": [ "string" ],
         "InclusionPatterns": [ "string" ],
         "MessageFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "SecretArn": "string",
         "ThreadFieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         }
      },
      "S3Configuration": { 
         "AccessControlListConfiguration": { 
            "KeyPath": "string"
         },
         "BucketName": "string",
         "DocumentsMetadataConfiguration": { 
            "S3Prefix": "string"
         },
         "ExclusionPatterns": [ "string" ],
         "InclusionPatterns": [ "string" ],
         "InclusionPrefixes": [ "string" ]
      },
      "SalesforceConfiguration": { 
         "ChatterFeedConfiguration": { 
            "DocumentDataFieldName": "string",
            "DocumentTitleFieldName": "string",
            "FieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ],
            "IncludeFilterTypes": [ "string" ]
         },
         "CrawlAttachments": boolean,
         "ExcludeAttachmentFilePatterns": [ "string" ],
         "IncludeAttachmentFilePatterns": [ "string" ],
         "KnowledgeArticleConfiguration": { 
            "CustomKnowledgeArticleTypeConfigurations": [ 
               { 
                  "DocumentDataFieldName": "string",
                  "DocumentTitleFieldName": "string",
                  "FieldMappings": [ 
                     { 
                        "DataSourceFieldName": "string",
                        "DateFieldFormat": "string",
                        "IndexFieldName": "string"
                     }
                  ],
                  "Name": "string"
               }
            ],
            "IncludedStates": [ "string" ],
            "StandardKnowledgeArticleTypeConfiguration": { 
               "DocumentDataFieldName": "string",
               "DocumentTitleFieldName": "string",
               "FieldMappings": [ 
                  { 
                     "DataSourceFieldName": "string",
                     "DateFieldFormat": "string",
                     "IndexFieldName": "string"
                  }
               ]
            }
         },
         "SecretArn": "string",
         "ServerUrl": "string",
         "StandardObjectAttachmentConfiguration": { 
            "DocumentTitleFieldName": "string",
            "FieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ]
         },
         "StandardObjectConfigurations": [ 
            { 
               "DocumentDataFieldName": "string",
               "DocumentTitleFieldName": "string",
               "FieldMappings": [ 
                  { 
                     "DataSourceFieldName": "string",
                     "DateFieldFormat": "string",
                     "IndexFieldName": "string"
                  }
               ],
               "Name": "string"
            }
         ]
      },
      "ServiceNowConfiguration": { 
         "AuthenticationType": "string",
         "HostUrl": "string",
         "KnowledgeArticleConfiguration": { 
            "CrawlAttachments": boolean,
            "DocumentDataFieldName": "string",
            "DocumentTitleFieldName": "string",
            "ExcludeAttachmentFilePatterns": [ "string" ],
            "FieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ],
            "FilterQuery": "string",
            "IncludeAttachmentFilePatterns": [ "string" ]
         },
         "SecretArn": "string",
         "ServiceCatalogConfiguration": { 
            "CrawlAttachments": boolean,
            "DocumentDataFieldName": "string",
            "DocumentTitleFieldName": "string",
            "ExcludeAttachmentFilePatterns": [ "string" ],
            "FieldMappings": [ 
               { 
                  "DataSourceFieldName": "string",
                  "DateFieldFormat": "string",
                  "IndexFieldName": "string"
               }
            ],
            "IncludeAttachmentFilePatterns": [ "string" ]
         },
         "ServiceNowBuildVersion": "string"
      },
      "SharePointConfiguration": { 
         "CrawlAttachments": boolean,
         "DisableLocalGroups": boolean,
         "DocumentTitleFieldName": "string",
         "ExclusionPatterns": [ "string" ],
         "FieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "InclusionPatterns": [ "string" ],
         "SecretArn": "string",
         "SharePointVersion": "string",
         "SslCertificateS3Path": { 
            "Bucket": "string",
            "Key": "string"
         },
         "Urls": [ "string" ],
         "UseChangeLog": boolean,
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         }
      },
      "SlackConfiguration": { 
         "CrawlBotMessage": boolean,
         "ExcludeArchived": boolean,
         "ExclusionPatterns": [ "string" ],
         "FieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "InclusionPatterns": [ "string" ],
         "LookBackPeriod": number,
         "PrivateChannelFilter": [ "string" ],
         "PublicChannelFilter": [ "string" ],
         "SecretArn": "string",
         "SinceCrawlDate": "string",
         "SlackEntityList": [ "string" ],
         "TeamId": "string",
         "UseChangeLog": boolean,
         "VpcConfiguration": { 
            "SecurityGroupIds": [ "string" ],
            "SubnetIds": [ "string" ]
         }
      },
      "WebCrawlerConfiguration": { 
         "AuthenticationConfiguration": { 
            "BasicAuthentication": [ 
               { 
                  "Credentials": "string",
                  "Host": "string",
                  "Port": number
               }
            ]
         },
         "CrawlDepth": number,
         "MaxContentSizePerPageInMegaBytes": number,
         "MaxLinksPerPage": number,
         "MaxUrlsPerMinuteCrawlRate": number,
         "ProxyConfiguration": { 
            "Credentials": "string",
            "Host": "string",
            "Port": number
         },
         "UrlExclusionPatterns": [ "string" ],
         "UrlInclusionPatterns": [ "string" ],
         "Urls": { 
            "SeedUrlConfiguration": { 
               "SeedUrls": [ "string" ],
               "WebCrawlerMode": "string"
            },
            "SiteMapsConfiguration": { 
               "SiteMaps": [ "string" ]
            }
         }
      },
      "WorkDocsConfiguration": { 
         "CrawlComments": boolean,
         "ExclusionPatterns": [ "string" ],
         "FieldMappings": [ 
            { 
               "DataSourceFieldName": "string",
               "DateFieldFormat": "string",
               "IndexFieldName": "string"
            }
         ],
         "InclusionPatterns": [ "string" ],
         "OrganizationId": "string",
         "UseChangeLog": boolean
      }
   },
   "CreatedAt": number,
   "CustomDocumentEnrichmentConfiguration": { 
      "InlineConfigurations": [ 
         { 
            "Condition": { 
               "ConditionDocumentAttributeKey": "string",
               "ConditionOnValue": { 
                  "DateValue": number,
                  "LongValue": number,
                  "StringListValue": [ "string" ],
                  "StringValue": "string"
               },
               "Operator": "string"
            },
            "DocumentContentDeletion": boolean,
            "Target": { 
               "TargetDocumentAttributeKey": "string",
               "TargetDocumentAttributeValue": { 
                  "DateValue": number,
                  "LongValue": number,
                  "StringListValue": [ "string" ],
                  "StringValue": "string"
               },
               "TargetDocumentAttributeValueDeletion": boolean
            }
         }
      ],
      "PostExtractionHookConfiguration": { 
         "InvocationCondition": { 
            "ConditionDocumentAttributeKey": "string",
            "ConditionOnValue": { 
               "DateValue": number,
               "LongValue": number,
               "StringListValue": [ "string" ],
               "StringValue": "string"
            },
            "Operator": "string"
         },
         "LambdaArn": "string",
         "S3Bucket": "string"
      },
      "PreExtractionHookConfiguration": { 
         "InvocationCondition": { 
            "ConditionDocumentAttributeKey": "string",
            "ConditionOnValue": { 
               "DateValue": number,
               "LongValue": number,
               "StringListValue": [ "string" ],
               "StringValue": "string"
            },
            "Operator": "string"
         },
         "LambdaArn": "string",
         "S3Bucket": "string"
      },
      "RoleArn": "string"
   },
   "Description": "string",
   "ErrorMessage": "string",
   "Id": "string",
   "IndexId": "string",
   "LanguageCode": "string",
   "Name": "string",
   "RoleArn": "string",
   "Schedule": "string",
   "Status": "string",
   "Type": "string",
   "UpdatedAt": number
}
```

## Response Elements<a name="API_DescribeDataSource_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response\.

The following data is returned in JSON format by the service\.

 ** [Configuration](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-Configuration"></a>
Describes how the data source is configured\. The specific information in the description depends on the data source provider\.  
Type: [DataSourceConfiguration](API_DataSourceConfiguration.md) object

 ** [CreatedAt](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-CreatedAt"></a>
The Unix timestamp of when the data source was created\.  
Type: Timestamp

 ** [CustomDocumentEnrichmentConfiguration](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-CustomDocumentEnrichmentConfiguration"></a>
Configuration information for altering document metadata and content during the document ingestion process when you describe a data source\.  
For more information on how to create, modify and delete document metadata, or make other content alterations when you ingest documents into Amazon Kendra, see [Customizing document metadata during the ingestion process](https://docs.aws.amazon.com/kendra/latest/dg/custom-document-enrichment.html)\.  
Type: [CustomDocumentEnrichmentConfiguration](API_CustomDocumentEnrichmentConfiguration.md) object

 ** [Description](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-Description"></a>
The description of the data source\.  
Type: String  
Length Constraints: Minimum length of 0\. Maximum length of 1000\.  
Pattern: `^\P{C}*$` 

 ** [ErrorMessage](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-ErrorMessage"></a>
When the `Status` field value is `FAILED`, the `ErrorMessage` field contains a description of the error that caused the data source to fail\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 2048\.  
Pattern: `^\P{C}*$` 

 ** [Id](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-Id"></a>
The identifier of the data source\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 100\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*` 

 ** [IndexId](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-IndexId"></a>
The identifier of the index that contains the data source\.  
Type: String  
Length Constraints: Fixed length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9-]*` 

 ** [LanguageCode](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-LanguageCode"></a>
The code for a language\. This shows a supported language for all documents in the data source\. English is supported by default\. For more information on supported languages, including their codes, see [Adding documents in languages other than English](https://docs.aws.amazon.com/kendra/latest/dg/in-adding-languages.html)\.  
Type: String  
Length Constraints: Minimum length of 2\. Maximum length of 10\.  
Pattern: `[a-zA-Z-]*` 

 ** [Name](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-Name"></a>
The name that you gave the data source when it was created\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 1000\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*` 

 ** [RoleArn](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-RoleArn"></a>
The Amazon Resource Name \(ARN\) of the role that enables the data source to access its resources\.  
Type: String  
Length Constraints: Minimum length of 0\. Maximum length of 1284\.  
Pattern: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}` 

 ** [Schedule](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-Schedule"></a>
The schedule for Amazon Kendra to update the index\.  
Type: String

 ** [Status](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-Status"></a>
The current status of the data source\. When the status is `ACTIVE` the data source is ready to use\. When the status is `FAILED`, the `ErrorMessage` field contains the reason that the data source failed\.  
Type: String  
Valid Values:` CREATING | DELETING | FAILED | UPDATING | ACTIVE` 

 ** [Type](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-Type"></a>
The type of the data source\.  
Type: String  
Valid Values:` S3 | SHAREPOINT | DATABASE | SALESFORCE | ONEDRIVE | SERVICENOW | CUSTOM | CONFLUENCE | GOOGLEDRIVE | WEBCRAWLER | WORKDOCS | FSX | SLACK | BOX | QUIP | JIRA | GITHUB | ALFRESCO` 

 ** [UpdatedAt](#API_DescribeDataSource_ResponseSyntax) **   <a name="Kendra-DescribeDataSource-response-UpdatedAt"></a>
The Unix timestamp of when the data source was last updated\.  
Type: Timestamp

## Errors<a name="API_DescribeDataSource_Errors"></a>

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

## See Also<a name="API_DescribeDataSource_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS Command Line Interface](https://docs.aws.amazon.com/goto/aws-cli/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for \.NET](https://docs.aws.amazon.com/goto/DotNetSDKV3/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for JavaScript](https://docs.aws.amazon.com/goto/AWSJavaScriptSDK/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for PHP V3](https://docs.aws.amazon.com/goto/SdkForPHPV3/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for Python](https://docs.aws.amazon.com/goto/boto3/kendra-2019-02-03/DescribeDataSource) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/DescribeDataSource) 
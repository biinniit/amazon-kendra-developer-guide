--------

--------

# ConfluenceAttachmentToIndexFieldMapping<a name="API_ConfluenceAttachmentToIndexFieldMapping"></a>

Maps attributes or field names of Confluence attachments to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to Confluence fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The Confuence data source field names must exist in your Confluence custom metadata\.

## Contents<a name="API_ConfluenceAttachmentToIndexFieldMapping_Contents"></a>

 ** DataSourceFieldName **   <a name="Kendra-Type-ConfluenceAttachmentToIndexFieldMapping-DataSourceFieldName"></a>
The name of the field in the data source\.   
You must first create the index field using the `UpdateIndex` API\.   
Type: String  
Valid Values:` AUTHOR | CONTENT_TYPE | CREATED_DATE | DISPLAY_URL | FILE_SIZE | ITEM_TYPE | PARENT_ID | SPACE_KEY | SPACE_NAME | URL | VERSION`   
Required: No

 ** DateFieldFormat **   <a name="Kendra-Type-ConfluenceAttachmentToIndexFieldMapping-DateFieldFormat"></a>
The format for date fields in the data source\. If the field specified in `DataSourceFieldName` is a date field you must specify the date format\. If the field is not a date field, an exception is thrown\.  
Type: String  
Length Constraints: Minimum length of 4\. Maximum length of 40\.  
Pattern: `^(?!\s).*(?<!\s)$`   
Required: No

 ** IndexFieldName **   <a name="Kendra-Type-ConfluenceAttachmentToIndexFieldMapping-IndexFieldName"></a>
The name of the index field to map to the Confluence data source field\. The index field type must match the Confluence field type\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 30\.  
Pattern: `^\P{C}*$`   
Required: No

## See Also<a name="API_ConfluenceAttachmentToIndexFieldMapping_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/ConfluenceAttachmentToIndexFieldMapping) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/ConfluenceAttachmentToIndexFieldMapping) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/ConfluenceAttachmentToIndexFieldMapping) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/ConfluenceAttachmentToIndexFieldMapping) 
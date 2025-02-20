--------

--------

# DataSourceSyncJobMetricTarget<a name="API_DataSourceSyncJobMetricTarget"></a>

Maps a particular data source sync job to a particular data source\.

## Contents<a name="API_DataSourceSyncJobMetricTarget_Contents"></a>

 ** DataSourceId **   <a name="Kendra-Type-DataSourceSyncJobMetricTarget-DataSourceId"></a>
The ID of the data source that is running the sync job\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 100\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*`   
Required: Yes

 ** DataSourceSyncJobId **   <a name="Kendra-Type-DataSourceSyncJobMetricTarget-DataSourceSyncJobId"></a>
The ID of the sync job that is running on the data source\.  
If the ID of a sync job is not provided and there is a sync job running, then the ID of this sync job is used and metrics are generated for this sync job\.  
If the ID of a sync job is not provided and there is no sync job running, then no metrics are generated and documents are indexed/deleted at the index level without sync job metrics included\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 100\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*`   
Required: No

## See Also<a name="API_DataSourceSyncJobMetricTarget_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/DataSourceSyncJobMetricTarget) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/DataSourceSyncJobMetricTarget) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/DataSourceSyncJobMetricTarget) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/DataSourceSyncJobMetricTarget) 
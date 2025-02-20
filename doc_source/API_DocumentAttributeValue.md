--------

--------

# DocumentAttributeValue<a name="API_DocumentAttributeValue"></a>

The value of a document attribute\. You can only provide one value for a document attribute\.

## Contents<a name="API_DocumentAttributeValue_Contents"></a>

 ** DateValue **   <a name="Kendra-Type-DocumentAttributeValue-DateValue"></a>
A date expressed as an ISO 8601 string\.  
It is important for the time zone to be included in the ISO 8601 date\-time format\. For example, 2012\-03\-25T12:30:10\+01:00 is the ISO 8601 date\-time format for March 25th 2012 at 12:30PM \(plus 10 seconds\) in Central European Time\.  
Type: Timestamp  
Required: No

 ** LongValue **   <a name="Kendra-Type-DocumentAttributeValue-LongValue"></a>
A long integer value\.  
Type: Long  
Required: No

 ** StringListValue **   <a name="Kendra-Type-DocumentAttributeValue-StringListValue"></a>
A list of strings\.   
Type: Array of strings  
Length Constraints: Minimum length of 1\. Maximum length of 2048\.  
Required: No

 ** StringValue **   <a name="Kendra-Type-DocumentAttributeValue-StringValue"></a>
A string, such as "department"\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 2048\.  
Required: No

## See Also<a name="API_DocumentAttributeValue_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/DocumentAttributeValue) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/DocumentAttributeValue) 
+  [AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/DocumentAttributeValue) 
+  [AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/DocumentAttributeValue) 
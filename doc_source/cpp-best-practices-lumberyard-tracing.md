# Tracing<a name="cpp-best-practices-lumberyard-tracing"></a>

**Recommended**: For code tracing needs, use `AZ_*` tracing macros\.

**Reason**: Error handling and tracing functions provide useful messages formatted for readability about errors that occur\. To facilitate debugging, `AZ_*` tracing functions indicate where in code the errors occurred\.

The following table describes the `AZ_Tracing` macros and their uses\.


****  

| AZ Tracing Macro | Description | 
| --- | --- | 
| AZ\_Assert |  Use for critical errors when the program cannot continue\. `AZ_Assert` macros print an error message, the file name and line number where the error occurred, and then break program execution\.  | 
| AZ\_Error |  Use when an obvious error has occurred but the program can continue safely\. `AZ_Error` macros print an error message and the file name and line number where the error occurred\. In some environments, `AZ_Error` notifies the user that an error has occurred \(for example, in a message box or onscreen message\)\.  | 
| AZ\_Warning |  Use when an error might have occurred\. `AZ_Warning` macros print an error message and the file name and line number of the possible error, but take no other action\.  | 
| AZ\_TracePrintf |  Use for informational purposes only\. `AZ_TracePrintf` macros print a message but take no other action\.  | 

 For source code, see `lumberyard_version\dev\Code\Framework\AzCore\AzCore\Debug\Trace.*`\.
# RedirectUrl

The MediaMarkup annotation tool page can be driven by the API by a third party without third party users logging into the main user interface. Third party users in this case will need to be authenticated using the PersonalUrl authentication flow to create Urls to the annotation tool on the fly and redirect users. If the user's session ends, or is not authenticated, instead of redirecting to the MediaMarkup login page the user will be redirected to the configiured RedirectUrl.

The RedirectUrl is configured within the account details and is available to all account administrators.

Parameters will be added to the RedirectUrl indicating the current approval id, version and if available, the comparison approval and id.

### **Parameters**

#### **redir:**

NotAuthenticated - User is not authenticated

IdNotSpecified - approval id not specified

ApprovalNotFound - Approval not found

VersionNotFound - Approval Version not found

UserNotAuthorizedOnApproval - If user is not within an approval group  
\[Not checked for admin/manager/guest \(observer\) roles\]

CompareApprovalNotFound - Comparison Approval not found \(if specified\)

CompareVersionNotFound - Comparison Approval Version not found \(if specified\)

UserNotAuthorizedOnCompare - If user is not within an approval group  
\[Not checked for admin/manager/guest \(observer\) roles\]



The RedirectUrl specified can contains custom parameters, but should not conflict with the above parameters.


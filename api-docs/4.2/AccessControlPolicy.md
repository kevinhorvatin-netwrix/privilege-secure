
<h1 id="nps-api-accesscontrolpolicy">AccessControlPolicy</h1>

[Get names and ids for all access policies. (Auth policies: MfaRequired, MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/ListNamesAsync.md)

[Retrieve all access policies. (Auth policies: MfaRequired, MfaRequired; roles: Admin,App)](AccessControlPolicy/GetAll.md)

[Create a new policy. (Auth policies: MfaRequired, MfaRequired; roles: Admin,App)](AccessControlPolicy/Post.md)

[Retrieve access policy by id. (Auth policies: MfaRequired, MfaRequired; roles: Admin,App,UserPlus)](AccessControlPolicy/Get.md)

[Delete access policy (Auth policies: MfaRequired, MfaRequired; roles: Admin)](AccessControlPolicy/Delete.md)

[Update access policy (Auth policies: MfaRequired, MfaRequired; roles: Admin,App,UserPlus)](AccessControlPolicy/Put.md)

[Change policy delete/disabled status. (Auth policies: MfaRequired, MfaRequired; roles: Admin)](AccessControlPolicy/PutStatus.md)

[Retrieve Activity Cards for managed account id. (Auth policies: MfaRequired)](AccessControlPolicy/GetPoliciesForAccountAsync.md)

[Remove user from all policies containing the managed account id. (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/RemoveManagedGroupAccountFromAllPolicies.md)

[Retrieve policy candidates by managed account id. (Auth policies: MfaRequired, MfaRequired; roles: Admin)](AccessControlPolicy/GetPolicyCandidatesForAccountGroupAsync.md)

[Add managed account to multiple policies. (Auth policies: MfaRequired, MfaRequired; roles: Admin)](AccessControlPolicy/AddManagedAccountToMultiplePoliciesAsync.md)

[Remove managed account from multiple policies. (Auth policies: MfaRequired, MfaRequired; roles: Admin)](AccessControlPolicy/RemoveManagedAccountFromMultiplePoliciesAsync.md)

[Add managed account group to multiple policies. (Auth policies: MfaRequired, MfaRequired; roles: Admin)](AccessControlPolicy/AddManagedAccountGroupToMultiplePoliciesAsync.md)

[Remove managed account group from multiple policies. (Auth policies: MfaRequired, MfaRequired; roles: Admin)](AccessControlPolicy/RemoveManagedAccountGroupFromMultiplePoliciesAsync.md)

[Search for access policies (Auth policies: MfaRequired)](AccessControlPolicy/SearchForPolicy.md)

[Retrieve policies by managed account group id. (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/SearchPoliciesForAccountGroupAsync.md)

[Retrieve policies by managed resource id. (Auth policies: MfaRequired; roles: Admin,App)](AccessControlPolicy/FindResourcePolicies.md)

[Retrieve policies by managed account/managed resource id pair. (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/FindPolicies.md)

[Retrieve managed accounts directly associated with a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/GetManagedAccountsAsync.md)

[Associate a managed account with a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/AddMultipleManagedAccountsToPolicy.md)

[Disassociate a managed account from a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/RemoveMultipleManagedAccountsFromPolicy.md)

[Retrieve managed account groups associated with a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/GetManagedAccountGroupsAsync.md)

[Associate a managed resource with a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/AddMultipleManagedResourcesToPolicy.md)

[Disassociate a managed resource from a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/RemoveMultipleManagedResourcesFromPolicy.md)

[Associate activity from a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/AddMultipleActivitiesToPolicy.md)

[Disassociate activity from a policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/RemoveMultipleActivitiesFromPolicy.md)

[Add credentials to a policy (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/AddMultipleCredentialsToPolicyAsync.md)

[Disassociate credential from a policy. (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/RemoveMultipleCredentialsFromPolicyAsync.md)

[Get available resources for access policy (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/GetResourceLookupForPolicyAsync.md)

[Get available credentials for access policy (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/GetCredentialLookupForPolicyAsync.md)

[Get ActivityId and Name dictionary for given policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/GetActivityLookupForPolicyAsync.md)

[Search for resources by policy that can be accessed. (Auth policies: MfaRequired)](AccessControlPolicy/ActivitySessionCandidateResources.md)

[Search for activities that are in the given policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/SearchActivitiesAsync.md)

[Search for activities that are not in the given policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/SearchActivityCandidatesAsync.md)

[Search for credentials in the given policy. (Auth policies: MfaRequired; roles: App,Admin,UserPlus)](AccessControlPolicy/SearchCredentialsAsync.md)

[Search for credentials not in the given policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/SearchCredentialCandidatesAsync.md)

[Search for managed accounts in given policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/SearchManagedAccountsAsync.md)

[Search for users and groups that are not a part of the policy. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/SearchManagedAccountCandidatesAsync.md)

[Search for resources for the given policy id. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/SearchResourcesAsync.md)

[Search for resources that are not a part of the given policy id. (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/SearchResourceCandidatesAsync.md)

[Get activity card information with access policy information (Auth policies: MfaRequired)](AccessControlPolicy/GetActivityCardsWithPolicies.md)

[Add secret vaults to access policy (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/AddVaultToPolicyMultipleAsync.md)

[Remove secret vaults from access policy (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/RemoveVaultFromPolicyMultipleAsync.md)

[Get roles for access policy (Auth policies: MfaRequired; roles: Admin,UserPlus)](AccessControlPolicy/GetRolesForPolicyAsync.md)

[Copy access policy to new policy (Auth policies: MfaRequired; roles: Admin)](AccessControlPolicy/CopyAccessControlPolicy.md)



---
title: "RoleManagementPolicyAssignment"
title_tag: "azure-native.authorization.RoleManagementPolicyAssignment"
meta_desc: "Documentation for the azure-native.authorization.RoleManagementPolicyAssignment resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Role management policy
API Version: 2020-10-01-preview.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### GetConfigurations


{{< example csharp >}}

```csharp
using Pulumi;
using AzureNative = Pulumi.AzureNative;

class MyStack : Stack
{
    public MyStack()
    {
        var roleManagementPolicyAssignment = new AzureNative.Authorization.RoleManagementPolicyAssignment("roleManagementPolicyAssignment", new AzureNative.Authorization.RoleManagementPolicyAssignmentArgs
        {
            PolicyId = "/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/RoleManagementPolicies/477f2d04-0fdc-417f-ab1b-d9fff8137134",
            RoleDefinitionId = "/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/roleDefinitions/a37489be-9462-48fb-a3b6-7b9bc2debbad",
            RoleManagementPolicyAssignmentName = "477f2d04-0fdc-417f-ab1b-d9fff8137134_a37489be-9462-48fb-a3b6-7b9bc2debbad",
            Scope = "/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	authorization "github.com/pulumi/pulumi-azure-native/sdk/go/azure/authorization"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := authorization.NewRoleManagementPolicyAssignment(ctx, "roleManagementPolicyAssignment", &authorization.RoleManagementPolicyAssignmentArgs{
			PolicyId:                           pulumi.String("/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/RoleManagementPolicies/477f2d04-0fdc-417f-ab1b-d9fff8137134"),
			RoleDefinitionId:                   pulumi.String("/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/roleDefinitions/a37489be-9462-48fb-a3b6-7b9bc2debbad"),
			RoleManagementPolicyAssignmentName: pulumi.String("477f2d04-0fdc-417f-ab1b-d9fff8137134_a37489be-9462-48fb-a3b6-7b9bc2debbad"),
			Scope:                              pulumi.String("/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3"),
		})
		if err != nil {
			return err
		}
		return nil
	})
}

```


{{< /example >}}


{{< example python >}}


```python
import pulumi
import pulumi_azure_native as azure_native

role_management_policy_assignment = azure_native.authorization.RoleManagementPolicyAssignment("roleManagementPolicyAssignment",
    policy_id="/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/RoleManagementPolicies/477f2d04-0fdc-417f-ab1b-d9fff8137134",
    role_definition_id="/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/roleDefinitions/a37489be-9462-48fb-a3b6-7b9bc2debbad",
    role_management_policy_assignment_name="477f2d04-0fdc-417f-ab1b-d9fff8137134_a37489be-9462-48fb-a3b6-7b9bc2debbad",
    scope="/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_native from "@pulumi/azure-native";

const roleManagementPolicyAssignment = new azure_native.authorization.RoleManagementPolicyAssignment("roleManagementPolicyAssignment", {
    policyId: "/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/RoleManagementPolicies/477f2d04-0fdc-417f-ab1b-d9fff8137134",
    roleDefinitionId: "/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/roleDefinitions/a37489be-9462-48fb-a3b6-7b9bc2debbad",
    roleManagementPolicyAssignmentName: "477f2d04-0fdc-417f-ab1b-d9fff8137134_a37489be-9462-48fb-a3b6-7b9bc2debbad",
    scope: "/subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3",
});

```


{{< /example >}}





{{% /examples %}}




## Create a RoleManagementPolicyAssignment Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">RoleManagementPolicyAssignment</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">RoleManagementPolicyAssignmentArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nx">RoleManagementPolicyAssignment</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">, </span><span class="nx">policy_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">role_definition_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">role_management_policy_assignment_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">scope</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewRoleManagementPolicyAssignment</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">RoleManagementPolicyAssignmentArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">RoleManagementPolicyAssignment</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">RoleManagementPolicyAssignment</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">, </span><span class="nx"><a href="#inputs">RoleManagementPolicyAssignmentArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">RoleManagementPolicyAssignmentArgs</a></span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd></dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type">
            <a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a>
        </span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties"><dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>
      Context object for the current deployment.
    </dd><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">RoleManagementPolicyAssignmentArgs</a></span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd></dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">RoleManagementPolicyAssignmentArgs</a></span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd></dl>

{{% /choosable %}}

## RoleManagementPolicyAssignment Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Programming Model docs.

### Inputs

The RoleManagementPolicyAssignment resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="scope_csharp">
<a href="#scope_csharp" style="color: inherit; text-decoration: inherit;">Scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy scope.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="policyid_csharp">
<a href="#policyid_csharp" style="color: inherit; text-decoration: inherit;">Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The policy id role management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="roledefinitionid_csharp">
<a href="#roledefinitionid_csharp" style="color: inherit; text-decoration: inherit;">Role<wbr>Definition<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role definition of management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="rolemanagementpolicyassignmentname_csharp">
<a href="#rolemanagementpolicyassignmentname_csharp" style="color: inherit; text-decoration: inherit;">Role<wbr>Management<wbr>Policy<wbr>Assignment<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of format {guid_guid} the role management policy assignment to upsert.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="scope_go">
<a href="#scope_go" style="color: inherit; text-decoration: inherit;">Scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy scope.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="policyid_go">
<a href="#policyid_go" style="color: inherit; text-decoration: inherit;">Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The policy id role management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="roledefinitionid_go">
<a href="#roledefinitionid_go" style="color: inherit; text-decoration: inherit;">Role<wbr>Definition<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role definition of management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="rolemanagementpolicyassignmentname_go">
<a href="#rolemanagementpolicyassignmentname_go" style="color: inherit; text-decoration: inherit;">Role<wbr>Management<wbr>Policy<wbr>Assignment<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of format {guid_guid} the role management policy assignment to upsert.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="scope_nodejs">
<a href="#scope_nodejs" style="color: inherit; text-decoration: inherit;">scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy scope.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="policyid_nodejs">
<a href="#policyid_nodejs" style="color: inherit; text-decoration: inherit;">policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The policy id role management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="roledefinitionid_nodejs">
<a href="#roledefinitionid_nodejs" style="color: inherit; text-decoration: inherit;">role<wbr>Definition<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role definition of management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="rolemanagementpolicyassignmentname_nodejs">
<a href="#rolemanagementpolicyassignmentname_nodejs" style="color: inherit; text-decoration: inherit;">role<wbr>Management<wbr>Policy<wbr>Assignment<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of format {guid_guid} the role management policy assignment to upsert.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="scope_python">
<a href="#scope_python" style="color: inherit; text-decoration: inherit;">scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The role management policy scope.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="policy_id_python">
<a href="#policy_id_python" style="color: inherit; text-decoration: inherit;">policy_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The policy id role management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="role_definition_id_python">
<a href="#role_definition_id_python" style="color: inherit; text-decoration: inherit;">role_<wbr>definition_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The role definition of management policy assignment.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="role_management_policy_assignment_name_python">
<a href="#role_management_policy_assignment_name_python" style="color: inherit; text-decoration: inherit;">role_<wbr>management_<wbr>policy_<wbr>assignment_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of format {guid_guid} the role management policy assignment to upsert.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the RoleManagementPolicyAssignment resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role management policy type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The role management policy name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The role management policy type.{{% /md %}}</dd></dl>
{{% /choosable %}}






## Import


An existing resource can be imported using its type token, name, and identifier, e.g.

```sh
$ pulumi import azure-native:authorization:RoleManagementPolicyAssignment 477f2d04-0fdc-417f-ab1b-d9fff8137134_a37489be-9462-48fb-a3b6-7b9bc2debbad /subscriptions/892f85f0-fd69-4fe8-8ee2-bda821252ac3/providers/Microsoft.Authorization/RoleManagementPolicyAssignment/477f2d04-0fdc-417f-ab1b-d9fff8137134_a37489be-9462-48fb-a3b6-7b9bc2debbad 
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>


---
title: "DataMaskingPolicy"
title_tag: "azure-native.sql.DataMaskingPolicy"
meta_desc: "Documentation for the azure-native.sql.DataMaskingPolicy resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Represents a database data masking policy.
API Version: 2014-04-01.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Create or update data masking policy max


{{< example csharp >}}

```csharp
using Pulumi;
using AzureNative = Pulumi.AzureNative;

class MyStack : Stack
{
    public MyStack()
    {
        var dataMaskingPolicy = new AzureNative.Sql.DataMaskingPolicy("dataMaskingPolicy", new AzureNative.Sql.DataMaskingPolicyArgs
        {
            DataMaskingPolicyName = "Default",
            DataMaskingState = "Enabled",
            DatabaseName = "sqlcrudtest-331",
            ExemptPrincipals = "testuser;",
            ResourceGroupName = "sqlcrudtest-6852",
            ServerName = "sqlcrudtest-2080",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	sql "github.com/pulumi/pulumi-azure-native/sdk/go/azure/sql"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := sql.NewDataMaskingPolicy(ctx, "dataMaskingPolicy", &sql.DataMaskingPolicyArgs{
			DataMaskingPolicyName: pulumi.String("Default"),
			DataMaskingState:      "Enabled",
			DatabaseName:          pulumi.String("sqlcrudtest-331"),
			ExemptPrincipals:      pulumi.String("testuser;"),
			ResourceGroupName:     pulumi.String("sqlcrudtest-6852"),
			ServerName:            pulumi.String("sqlcrudtest-2080"),
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

data_masking_policy = azure_native.sql.DataMaskingPolicy("dataMaskingPolicy",
    data_masking_policy_name="Default",
    data_masking_state="Enabled",
    database_name="sqlcrudtest-331",
    exempt_principals="testuser;",
    resource_group_name="sqlcrudtest-6852",
    server_name="sqlcrudtest-2080")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_native from "@pulumi/azure-native";

const dataMaskingPolicy = new azure_native.sql.DataMaskingPolicy("dataMaskingPolicy", {
    dataMaskingPolicyName: "Default",
    dataMaskingState: "Enabled",
    databaseName: "sqlcrudtest-331",
    exemptPrincipals: "testuser;",
    resourceGroupName: "sqlcrudtest-6852",
    serverName: "sqlcrudtest-2080",
});

```


{{< /example >}}




### Create or update data masking policy min


{{< example csharp >}}

```csharp
using Pulumi;
using AzureNative = Pulumi.AzureNative;

class MyStack : Stack
{
    public MyStack()
    {
        var dataMaskingPolicy = new AzureNative.Sql.DataMaskingPolicy("dataMaskingPolicy", new AzureNative.Sql.DataMaskingPolicyArgs
        {
            DataMaskingPolicyName = "Default",
            DataMaskingState = "Enabled",
            DatabaseName = "sqlcrudtest-331",
            ResourceGroupName = "sqlcrudtest-6852",
            ServerName = "sqlcrudtest-2080",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	sql "github.com/pulumi/pulumi-azure-native/sdk/go/azure/sql"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := sql.NewDataMaskingPolicy(ctx, "dataMaskingPolicy", &sql.DataMaskingPolicyArgs{
			DataMaskingPolicyName: pulumi.String("Default"),
			DataMaskingState:      "Enabled",
			DatabaseName:          pulumi.String("sqlcrudtest-331"),
			ResourceGroupName:     pulumi.String("sqlcrudtest-6852"),
			ServerName:            pulumi.String("sqlcrudtest-2080"),
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

data_masking_policy = azure_native.sql.DataMaskingPolicy("dataMaskingPolicy",
    data_masking_policy_name="Default",
    data_masking_state="Enabled",
    database_name="sqlcrudtest-331",
    resource_group_name="sqlcrudtest-6852",
    server_name="sqlcrudtest-2080")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_native from "@pulumi/azure-native";

const dataMaskingPolicy = new azure_native.sql.DataMaskingPolicy("dataMaskingPolicy", {
    dataMaskingPolicyName: "Default",
    dataMaskingState: "Enabled",
    databaseName: "sqlcrudtest-331",
    resourceGroupName: "sqlcrudtest-6852",
    serverName: "sqlcrudtest-2080",
});

```


{{< /example >}}





{{% /examples %}}




## Create a DataMaskingPolicy Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">DataMaskingPolicy</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">DataMaskingPolicyArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nx">DataMaskingPolicy</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">, </span><span class="nx">data_masking_policy_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">data_masking_state</span><span class="p">:</span> <span class="nx">Optional[DataMaskingState]</span> = None<span class="p">, </span><span class="nx">database_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">exempt_principals</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">server_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewDataMaskingPolicy</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">DataMaskingPolicyArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">DataMaskingPolicy</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">DataMaskingPolicy</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">, </span><span class="nx"><a href="#inputs">DataMaskingPolicyArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">DataMaskingPolicyArgs</a></span>
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
        <span class="property-type"><a href="#inputs">DataMaskingPolicyArgs</a></span>
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
        <span class="property-type"><a href="#inputs">DataMaskingPolicyArgs</a></span>
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

## DataMaskingPolicy Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Programming Model docs.

### Inputs

The DataMaskingPolicy resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="datamaskingstate_csharp">
<a href="#datamaskingstate_csharp" style="color: inherit; text-decoration: inherit;">Data<wbr>Masking<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#datamaskingstate">Pulumi.<wbr>Azure<wbr>Native.<wbr>Sql.<wbr>Data<wbr>Masking<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}The state of the data masking policy.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="databasename_csharp">
<a href="#databasename_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servername_csharp">
<a href="#servername_csharp" style="color: inherit; text-decoration: inherit;">Server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="datamaskingpolicyname_csharp">
<a href="#datamaskingpolicyname_csharp" style="color: inherit; text-decoration: inherit;">Data<wbr>Masking<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database for which the data masking rule applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="exemptprincipals_csharp">
<a href="#exemptprincipals_csharp" style="color: inherit; text-decoration: inherit;">Exempt<wbr>Principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The list of the exempt principals. Specifies the semicolon-separated list of database users for which the data masking policy does not apply. The specified users receive data results without masking for all of the database queries.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="datamaskingstate_go">
<a href="#datamaskingstate_go" style="color: inherit; text-decoration: inherit;">Data<wbr>Masking<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#datamaskingstate">Data<wbr>Masking<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}The state of the data masking policy.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="databasename_go">
<a href="#databasename_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servername_go">
<a href="#servername_go" style="color: inherit; text-decoration: inherit;">Server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="datamaskingpolicyname_go">
<a href="#datamaskingpolicyname_go" style="color: inherit; text-decoration: inherit;">Data<wbr>Masking<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database for which the data masking rule applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="exemptprincipals_go">
<a href="#exemptprincipals_go" style="color: inherit; text-decoration: inherit;">Exempt<wbr>Principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The list of the exempt principals. Specifies the semicolon-separated list of database users for which the data masking policy does not apply. The specified users receive data results without masking for all of the database queries.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="datamaskingstate_nodejs">
<a href="#datamaskingstate_nodejs" style="color: inherit; text-decoration: inherit;">data<wbr>Masking<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#datamaskingstate">Data<wbr>Masking<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}The state of the data masking policy.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="databasename_nodejs">
<a href="#databasename_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servername_nodejs">
<a href="#servername_nodejs" style="color: inherit; text-decoration: inherit;">server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="datamaskingpolicyname_nodejs">
<a href="#datamaskingpolicyname_nodejs" style="color: inherit; text-decoration: inherit;">data<wbr>Masking<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database for which the data masking rule applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="exemptprincipals_nodejs">
<a href="#exemptprincipals_nodejs" style="color: inherit; text-decoration: inherit;">exempt<wbr>Principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The list of the exempt principals. Specifies the semicolon-separated list of database users for which the data masking policy does not apply. The specified users receive data results without masking for all of the database queries.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="data_masking_state_python">
<a href="#data_masking_state_python" style="color: inherit; text-decoration: inherit;">data_<wbr>masking_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#datamaskingstate">Data<wbr>Masking<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}The state of the data masking policy.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="database_name_python">
<a href="#database_name_python" style="color: inherit; text-decoration: inherit;">database_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="server_name_python">
<a href="#server_name_python" style="color: inherit; text-decoration: inherit;">server_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="data_masking_policy_name_python">
<a href="#data_masking_policy_name_python" style="color: inherit; text-decoration: inherit;">data_<wbr>masking_<wbr>policy_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the database for which the data masking rule applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="exempt_principals_python">
<a href="#exempt_principals_python" style="color: inherit; text-decoration: inherit;">exempt_<wbr>principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The list of the exempt principals. Specifies the semicolon-separated list of database users for which the data masking policy does not apply. The specified users receive data results without masking for all of the database queries.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the DataMaskingPolicy resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="applicationprincipals_csharp">
<a href="#applicationprincipals_csharp" style="color: inherit; text-decoration: inherit;">Application<wbr>Principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The list of the application principals. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_csharp">
<a href="#kind_csharp" style="color: inherit; text-decoration: inherit;">Kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The kind of data masking policy. Metadata, used for Azure portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location of the data masking policy.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="maskinglevel_csharp">
<a href="#maskinglevel_csharp" style="color: inherit; text-decoration: inherit;">Masking<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The masking level. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="applicationprincipals_go">
<a href="#applicationprincipals_go" style="color: inherit; text-decoration: inherit;">Application<wbr>Principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The list of the application principals. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_go">
<a href="#kind_go" style="color: inherit; text-decoration: inherit;">Kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The kind of data masking policy. Metadata, used for Azure portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location of the data masking policy.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="maskinglevel_go">
<a href="#maskinglevel_go" style="color: inherit; text-decoration: inherit;">Masking<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The masking level. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="applicationprincipals_nodejs">
<a href="#applicationprincipals_nodejs" style="color: inherit; text-decoration: inherit;">application<wbr>Principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The list of the application principals. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_nodejs">
<a href="#kind_nodejs" style="color: inherit; text-decoration: inherit;">kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The kind of data masking policy. Metadata, used for Azure portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location of the data masking policy.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="maskinglevel_nodejs">
<a href="#maskinglevel_nodejs" style="color: inherit; text-decoration: inherit;">masking<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The masking level. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="application_principals_python">
<a href="#application_principals_python" style="color: inherit; text-decoration: inherit;">application_<wbr>principals</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The list of the application principals. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_python">
<a href="#kind_python" style="color: inherit; text-decoration: inherit;">kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The kind of data masking policy. Metadata, used for Azure portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The location of the data masking policy.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="masking_level_python">
<a href="#masking_level_python" style="color: inherit; text-decoration: inherit;">masking_<wbr>level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The masking level. This is a legacy parameter and is no longer used.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="datamaskingstate">Data<wbr>Masking<wbr>State</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Disabled</dt>
    <dd>Disabled</dd><dt>Enabled</dt>
    <dd>Enabled</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Data<wbr>Masking<wbr>State<wbr>Disabled</dt>
    <dd>Disabled</dd><dt>Data<wbr>Masking<wbr>State<wbr>Enabled</dt>
    <dd>Enabled</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Disabled</dt>
    <dd>Disabled</dd><dt>Enabled</dt>
    <dd>Enabled</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>DISABLED</dt>
    <dd>Disabled</dd><dt>ENABLED</dt>
    <dd>Enabled</dd></dl>
{{% /choosable %}}
## Import


An existing resource can be imported using its type token, name, and identifier, e.g.

```sh
$ pulumi import azure-native:sql:DataMaskingPolicy Default /subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/sqlcrudtest-6852/providers/Microsoft.Sql/servers/sqlcrudtest-2080/databases/sqlcrudtest-331/dataMaskingPolicies/Default 
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

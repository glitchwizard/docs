
---
title: "WorkspaceConnection"
title_tag: "azure-native.machinelearningservices.WorkspaceConnection"
meta_desc: "Documentation for the azure-native.machinelearningservices.WorkspaceConnection resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Workspace connection.
API Version: 2021-01-01.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### CreateWorkspaceConnection


{{< example csharp >}}

```csharp
using Pulumi;
using AzureNative = Pulumi.AzureNative;

class MyStack : Stack
{
    public MyStack()
    {
        var workspaceConnection = new AzureNative.MachineLearningServices.WorkspaceConnection("workspaceConnection", new AzureNative.MachineLearningServices.WorkspaceConnectionArgs
        {
            AuthType = "PAT",
            Category = "ACR",
            ConnectionName = "connection-1",
            Name = "connection-1",
            ResourceGroupName = "resourceGroup-1",
            Target = "www.facebook.com",
            Value = "secrets",
            WorkspaceName = "workspace-1",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	machinelearningservices "github.com/pulumi/pulumi-azure-native/sdk/go/azure/machinelearningservices"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := machinelearningservices.NewWorkspaceConnection(ctx, "workspaceConnection", &machinelearningservices.WorkspaceConnectionArgs{
			AuthType:          pulumi.String("PAT"),
			Category:          pulumi.String("ACR"),
			ConnectionName:    pulumi.String("connection-1"),
			Name:              pulumi.String("connection-1"),
			ResourceGroupName: pulumi.String("resourceGroup-1"),
			Target:            pulumi.String("www.facebook.com"),
			Value:             pulumi.String("secrets"),
			WorkspaceName:     pulumi.String("workspace-1"),
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

workspace_connection = azure_native.machinelearningservices.WorkspaceConnection("workspaceConnection",
    auth_type="PAT",
    category="ACR",
    connection_name="connection-1",
    name="connection-1",
    resource_group_name="resourceGroup-1",
    target="www.facebook.com",
    value="secrets",
    workspace_name="workspace-1")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_native from "@pulumi/azure-native";

const workspaceConnection = new azure_native.machinelearningservices.WorkspaceConnection("workspaceConnection", {
    authType: "PAT",
    category: "ACR",
    connectionName: "connection-1",
    name: "connection-1",
    resourceGroupName: "resourceGroup-1",
    target: "www.facebook.com",
    value: "secrets",
    workspaceName: "workspace-1",
});

```


{{< /example >}}





{{% /examples %}}




## Create a WorkspaceConnection Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">WorkspaceConnection</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">WorkspaceConnectionArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nx">WorkspaceConnection</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">, </span><span class="nx">auth_type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">category</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">connection_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">target</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">value</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">value_format</span><span class="p">:</span> <span class="nx">Optional[Union[str, ValueFormat]]</span> = None<span class="p">, </span><span class="nx">workspace_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewWorkspaceConnection</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">WorkspaceConnectionArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">WorkspaceConnection</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">WorkspaceConnection</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">, </span><span class="nx"><a href="#inputs">WorkspaceConnectionArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">WorkspaceConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">WorkspaceConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">WorkspaceConnectionArgs</a></span>
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

## WorkspaceConnection Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Programming Model docs.

### Inputs

The WorkspaceConnection resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource group in which workspace is located.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_csharp">
<a href="#workspacename_csharp" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Azure Machine Learning workspace.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="authtype_csharp">
<a href="#authtype_csharp" style="color: inherit; text-decoration: inherit;">Auth<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization type of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="category_csharp">
<a href="#category_csharp" style="color: inherit; text-decoration: inherit;">Category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Category of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connectionname_csharp">
<a href="#connectionname_csharp" style="color: inherit; text-decoration: inherit;">Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="target_csharp">
<a href="#target_csharp" style="color: inherit; text-decoration: inherit;">Target</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Target of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value details of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="valueformat_csharp">
<a href="#valueformat_csharp" style="color: inherit; text-decoration: inherit;">Value<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#valueformat">Pulumi.<wbr>Azure<wbr>Native.<wbr>Machine<wbr>Learning<wbr>Services.<wbr>Value<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}format for the workspace connection value{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource group in which workspace is located.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_go">
<a href="#workspacename_go" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Azure Machine Learning workspace.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="authtype_go">
<a href="#authtype_go" style="color: inherit; text-decoration: inherit;">Auth<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization type of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="category_go">
<a href="#category_go" style="color: inherit; text-decoration: inherit;">Category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Category of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connectionname_go">
<a href="#connectionname_go" style="color: inherit; text-decoration: inherit;">Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="target_go">
<a href="#target_go" style="color: inherit; text-decoration: inherit;">Target</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Target of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value details of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="valueformat_go">
<a href="#valueformat_go" style="color: inherit; text-decoration: inherit;">Value<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#valueformat">Value<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}format for the workspace connection value{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource group in which workspace is located.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_nodejs">
<a href="#workspacename_nodejs" style="color: inherit; text-decoration: inherit;">workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Azure Machine Learning workspace.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="authtype_nodejs">
<a href="#authtype_nodejs" style="color: inherit; text-decoration: inherit;">auth<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization type of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="category_nodejs">
<a href="#category_nodejs" style="color: inherit; text-decoration: inherit;">category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Category of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connectionname_nodejs">
<a href="#connectionname_nodejs" style="color: inherit; text-decoration: inherit;">connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="target_nodejs">
<a href="#target_nodejs" style="color: inherit; text-decoration: inherit;">target</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Target of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value details of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="valueformat_nodejs">
<a href="#valueformat_nodejs" style="color: inherit; text-decoration: inherit;">value<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#valueformat">Value<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}format for the workspace connection value{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the resource group in which workspace is located.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspace_name_python">
<a href="#workspace_name_python" style="color: inherit; text-decoration: inherit;">workspace_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of Azure Machine Learning workspace.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="auth_type_python">
<a href="#auth_type_python" style="color: inherit; text-decoration: inherit;">auth_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Authorization type of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="category_python">
<a href="#category_python" style="color: inherit; text-decoration: inherit;">category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Category of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connection_name_python">
<a href="#connection_name_python" style="color: inherit; text-decoration: inherit;">connection_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Friendly name of the workspace connection{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="target_python">
<a href="#target_python" style="color: inherit; text-decoration: inherit;">target</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Target of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Value details of the workspace connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="value_format_python">
<a href="#value_format_python" style="color: inherit; text-decoration: inherit;">value_<wbr>format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str | <a href="#valueformat">Value<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}format for the workspace connection value{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the WorkspaceConnection resource produces the following output properties:



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
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type of workspace connection.{{% /md %}}</dd></dl>
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
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type of workspace connection.{{% /md %}}</dd></dl>
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
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type of workspace connection.{{% /md %}}</dd></dl>
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
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type of workspace connection.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="valueformat">Value<wbr>Format</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>JSON</dt>
    <dd>JSON</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Value<wbr>Format<wbr>JSON</dt>
    <dd>JSON</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>JSON</dt>
    <dd>JSON</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>JSON</dt>
    <dd>JSON</dd></dl>
{{% /choosable %}}
## Import


An existing resource can be imported using its type token, name, and identifier, e.g.

```sh
$ pulumi import azure-native:machinelearningservices:WorkspaceConnection connection-1 /subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/resourceGroup-1/providers/Microsoft.MachineLearningServices/workspaces/workspace-1/connections/connection-1 
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>


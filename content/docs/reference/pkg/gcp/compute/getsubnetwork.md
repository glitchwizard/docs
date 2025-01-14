
---
title: "getSubnetwork"
title_tag: "gcp.compute.getSubnetwork"
meta_desc: "Documentation for the gcp.compute.getSubnetwork function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Get a subnetwork within GCE from its name and region.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Gcp = Pulumi.Gcp;

class MyStack : Stack
{
    public MyStack()
    {
        var my_subnetwork = Output.Create(Gcp.Compute.GetSubnetwork.InvokeAsync(new Gcp.Compute.GetSubnetworkArgs
        {
            Name = "default-us-east1",
            Region = "us-east1",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-gcp/sdk/v4/go/gcp/compute"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "default-us-east1"
		opt1 := "us-east1"
		_, err := compute.LookupSubnetwork(ctx, &compute.LookupSubnetworkArgs{
			Name:   &opt0,
			Region: &opt1,
		}, nil)
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
import pulumi_gcp as gcp

my_subnetwork = gcp.compute.get_subnetwork(name="default-us-east1",
    region="us-east1")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gcp from "@pulumi/gcp";

const my_subnetwork = pulumi.output(gcp.compute.getSubnetwork({
    name: "default-us-east1",
    region: "us-east1",
}, { async: true }));
```


{{< /example >}}





{{% /examples %}}




## Using getSubnetwork {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getSubnetwork<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetSubnetworkArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetSubnetworkResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_subnetwork(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">region</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">self_link</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetSubnetworkResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupSubnetwork<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">LookupSubnetworkArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupSubnetworkResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupSubnetwork` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetSubnetwork </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetSubnetworkResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetSubnetworkArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subnetwork. One of `name` or `self_link`
must be specified.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_csharp">
<a href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region this subnetwork has been created in. If
unspecified, this defaults to the region configured in the provider.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="selflink_csharp">
<a href="#selflink_csharp" style="color: inherit; text-decoration: inherit;">Self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The self link of the subnetwork. If `self_link` is
specified, `name`, `project`, and `region` are ignored.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subnetwork. One of `name` or `self_link`
must be specified.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_go">
<a href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region this subnetwork has been created in. If
unspecified, this defaults to the region configured in the provider.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="selflink_go">
<a href="#selflink_go" style="color: inherit; text-decoration: inherit;">Self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The self link of the subnetwork. If `self_link` is
specified, `name`, `project`, and `region` are ignored.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subnetwork. One of `name` or `self_link`
must be specified.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_nodejs">
<a href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region this subnetwork has been created in. If
unspecified, this defaults to the region configured in the provider.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="selflink_nodejs">
<a href="#selflink_nodejs" style="color: inherit; text-decoration: inherit;">self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The self link of the subnetwork. If `self_link` is
specified, `name`, `project`, and `region` are ignored.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the subnetwork. One of `name` or `self_link`
must be specified.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_python">
<a href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region this subnetwork has been created in. If
unspecified, this defaults to the region configured in the provider.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="self_link_python">
<a href="#self_link_python" style="color: inherit; text-decoration: inherit;">self_<wbr>link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The self link of the subnetwork. If `self_link` is
specified, `name`, `project`, and `region` are ignored.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getSubnetwork Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gatewayaddress_csharp">
<a href="#gatewayaddress_csharp" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address of the gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ipcidrrange_csharp">
<a href="#ipcidrrange_csharp" style="color: inherit; text-decoration: inherit;">Ip<wbr>Cidr<wbr>Range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="network_csharp">
<a href="#network_csharp" style="color: inherit; text-decoration: inherit;">Network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network name or resource link to the parent
network of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateipgoogleaccess_csharp">
<a href="#privateipgoogleaccess_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Ip<wbr>Google<wbr>Access</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the VMs in this subnet
can access Google services without assigned external IP
addresses.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_csharp">
<a href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryipranges_csharp">
<a href="#secondaryipranges_csharp" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Ip<wbr>Ranges</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsubnetworksecondaryiprange">List&lt;Get<wbr>Subnetwork<wbr>Secondary<wbr>Ip<wbr>Range&gt;</a></span>
    </dt>
    <dd>{{% md %}}An array of configurations for secondary IP ranges for
VM instances contained in this subnetwork. Structure is documented below.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflink_csharp">
<a href="#selflink_csharp" style="color: inherit; text-decoration: inherit;">Self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gatewayaddress_go">
<a href="#gatewayaddress_go" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address of the gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ipcidrrange_go">
<a href="#ipcidrrange_go" style="color: inherit; text-decoration: inherit;">Ip<wbr>Cidr<wbr>Range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="network_go">
<a href="#network_go" style="color: inherit; text-decoration: inherit;">Network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network name or resource link to the parent
network of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateipgoogleaccess_go">
<a href="#privateipgoogleaccess_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Ip<wbr>Google<wbr>Access</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the VMs in this subnet
can access Google services without assigned external IP
addresses.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_go">
<a href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryipranges_go">
<a href="#secondaryipranges_go" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Ip<wbr>Ranges</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsubnetworksecondaryiprange">[]Get<wbr>Subnetwork<wbr>Secondary<wbr>Ip<wbr>Range</a></span>
    </dt>
    <dd>{{% md %}}An array of configurations for secondary IP ranges for
VM instances contained in this subnetwork. Structure is documented below.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflink_go">
<a href="#selflink_go" style="color: inherit; text-decoration: inherit;">Self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gatewayaddress_nodejs">
<a href="#gatewayaddress_nodejs" style="color: inherit; text-decoration: inherit;">gateway<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address of the gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ipcidrrange_nodejs">
<a href="#ipcidrrange_nodejs" style="color: inherit; text-decoration: inherit;">ip<wbr>Cidr<wbr>Range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="network_nodejs">
<a href="#network_nodejs" style="color: inherit; text-decoration: inherit;">network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network name or resource link to the parent
network of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateipgoogleaccess_nodejs">
<a href="#privateipgoogleaccess_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Ip<wbr>Google<wbr>Access</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether the VMs in this subnet
can access Google services without assigned external IP
addresses.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_nodejs">
<a href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryipranges_nodejs">
<a href="#secondaryipranges_nodejs" style="color: inherit; text-decoration: inherit;">secondary<wbr>Ip<wbr>Ranges</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsubnetworksecondaryiprange">Get<wbr>Subnetwork<wbr>Secondary<wbr>Ip<wbr>Range[]</a></span>
    </dt>
    <dd>{{% md %}}An array of configurations for secondary IP ranges for
VM instances contained in this subnetwork. Structure is documented below.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflink_nodejs">
<a href="#selflink_nodejs" style="color: inherit; text-decoration: inherit;">self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Description of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gateway_address_python">
<a href="#gateway_address_python" style="color: inherit; text-decoration: inherit;">gateway_<wbr>address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP address of the gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ip_cidr_range_python">
<a href="#ip_cidr_range_python" style="color: inherit; text-decoration: inherit;">ip_<wbr>cidr_<wbr>range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="network_python">
<a href="#network_python" style="color: inherit; text-decoration: inherit;">network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The network name or resource link to the parent
network of this subnetwork.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="private_ip_google_access_python">
<a href="#private_ip_google_access_python" style="color: inherit; text-decoration: inherit;">private_<wbr>ip_<wbr>google_<wbr>access</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the VMs in this subnet
can access Google services without assigned external IP
addresses.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_python">
<a href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondary_ip_ranges_python">
<a href="#secondary_ip_ranges_python" style="color: inherit; text-decoration: inherit;">secondary_<wbr>ip_<wbr>ranges</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsubnetworksecondaryiprange">Sequence[Get<wbr>Subnetwork<wbr>Secondary<wbr>Ip<wbr>Range]</a></span>
    </dt>
    <dd>{{% md %}}An array of configurations for secondary IP ranges for
VM instances contained in this subnetwork. Structure is documented below.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="self_link_python">
<a href="#self_link_python" style="color: inherit; text-decoration: inherit;">self_<wbr>link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getsubnetworksecondaryiprange">Get<wbr>Subnetwork<wbr>Secondary<wbr>Ip<wbr>Range</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="ipcidrrange_csharp">
<a href="#ipcidrrange_csharp" style="color: inherit; text-decoration: inherit;">Ip<wbr>Cidr<wbr>Range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rangename_csharp">
<a href="#rangename_csharp" style="color: inherit; text-decoration: inherit;">Range<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name associated with this subnetwork secondary range, used
when adding an alias IP range to a VM instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="ipcidrrange_go">
<a href="#ipcidrrange_go" style="color: inherit; text-decoration: inherit;">Ip<wbr>Cidr<wbr>Range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rangename_go">
<a href="#rangename_go" style="color: inherit; text-decoration: inherit;">Range<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name associated with this subnetwork secondary range, used
when adding an alias IP range to a VM instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="ipcidrrange_nodejs">
<a href="#ipcidrrange_nodejs" style="color: inherit; text-decoration: inherit;">ip<wbr>Cidr<wbr>Range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rangename_nodejs">
<a href="#rangename_nodejs" style="color: inherit; text-decoration: inherit;">range<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name associated with this subnetwork secondary range, used
when adding an alias IP range to a VM instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="ip_cidr_range_python">
<a href="#ip_cidr_range_python" style="color: inherit; text-decoration: inherit;">ip_<wbr>cidr_<wbr>range</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses belonging to this subnetwork
secondary range.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="range_name_python">
<a href="#range_name_python" style="color: inherit; text-decoration: inherit;">range_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name associated with this subnetwork secondary range, used
when adding an alias IP range to a VM instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-gcp">https://github.com/pulumi/pulumi-gcp</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`google-beta` Terraform Provider](https://github.com/hashicorp/terraform-provider-google-beta).{{% /md %}}</dd>
</dl>


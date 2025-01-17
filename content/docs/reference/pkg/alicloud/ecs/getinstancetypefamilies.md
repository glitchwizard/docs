
---
title: "getInstanceTypeFamilies"
title_tag: "alicloud.ecs.getInstanceTypeFamilies"
meta_desc: "Documentation for the alicloud.ecs.getInstanceTypeFamilies function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This data source provides the ECS instance type families of Alibaba Cloud.

> **NOTE:** Available in 1.54.0+


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using AliCloud = Pulumi.AliCloud;

class MyStack : Stack
{
    public MyStack()
    {
        var @default = Output.Create(AliCloud.Ecs.GetInstanceTypeFamilies.InvokeAsync(new AliCloud.Ecs.GetInstanceTypeFamiliesArgs
        {
            InstanceChargeType = "PrePaid",
        }));
        this.FirstInstanceTypeFamilyId = @default.Apply(@default => @default.Families[0].Id);
        this.InstanceIds = @default.Apply(@default => @default.Ids);
    }

    [Output("firstInstanceTypeFamilyId")]
    public Output<string> FirstInstanceTypeFamilyId { get; set; }
    [Output("instanceIds")]
    public Output<string> InstanceIds { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-alicloud/sdk/v2/go/alicloud/ecs"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "PrePaid"
		_default, err := ecs.GetInstanceTypeFamilies(ctx, &ecs.GetInstanceTypeFamiliesArgs{
			InstanceChargeType: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("firstInstanceTypeFamilyId", _default.Families[0].Id)
		ctx.Export("instanceIds", _default.Ids)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_alicloud as alicloud

default = alicloud.ecs.get_instance_type_families(instance_charge_type="PrePaid")
pulumi.export("firstInstanceTypeFamilyId", default.families[0].id)
pulumi.export("instanceIds", default.ids)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const defaultInstanceTypeFamilies = pulumi.output(alicloud.ecs.getInstanceTypeFamilies({
    instanceChargeType: "PrePaid",
}, { async: true }));

export const firstInstanceTypeFamilyId = defaultInstanceTypeFamilies.families[0].id;
export const instanceIds = defaultInstanceTypeFamilies.ids;
```


{{< /example >}}





{{% /examples %}}




## Using getInstanceTypeFamilies {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getInstanceTypeFamilies<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetInstanceTypeFamiliesArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetInstanceTypeFamiliesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_instance_type_families(</span><span class="nx">generation</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">instance_charge_type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">output_file</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">spot_strategy</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">zone_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetInstanceTypeFamiliesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetInstanceTypeFamilies<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">GetInstanceTypeFamiliesArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetInstanceTypeFamiliesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetInstanceTypeFamilies` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetInstanceTypeFamilies </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetInstanceTypeFamiliesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetInstanceTypeFamiliesArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="generation_csharp">
<a href="#generation_csharp" style="color: inherit; text-decoration: inherit;">Generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instancechargetype_csharp">
<a href="#instancechargetype_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Charge<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="spotstrategy_csharp">
<a href="#spotstrategy_csharp" style="color: inherit; text-decoration: inherit;">Spot<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by ECS spot type. Valid values: `NoSpot`, `SpotWithPriceLimit` and `SpotAsPriceGo`. Default to `NoSpot`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zoneid_csharp">
<a href="#zoneid_csharp" style="color: inherit; text-decoration: inherit;">Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="generation_go">
<a href="#generation_go" style="color: inherit; text-decoration: inherit;">Generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instancechargetype_go">
<a href="#instancechargetype_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Charge<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="spotstrategy_go">
<a href="#spotstrategy_go" style="color: inherit; text-decoration: inherit;">Spot<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by ECS spot type. Valid values: `NoSpot`, `SpotWithPriceLimit` and `SpotAsPriceGo`. Default to `NoSpot`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zoneid_go">
<a href="#zoneid_go" style="color: inherit; text-decoration: inherit;">Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="generation_nodejs">
<a href="#generation_nodejs" style="color: inherit; text-decoration: inherit;">generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instancechargetype_nodejs">
<a href="#instancechargetype_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Charge<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="spotstrategy_nodejs">
<a href="#spotstrategy_nodejs" style="color: inherit; text-decoration: inherit;">spot<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by ECS spot type. Valid values: `NoSpot`, `SpotWithPriceLimit` and `SpotAsPriceGo`. Default to `NoSpot`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zoneid_nodejs">
<a href="#zoneid_nodejs" style="color: inherit; text-decoration: inherit;">zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="generation_python">
<a href="#generation_python" style="color: inherit; text-decoration: inherit;">generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instance_charge_type_python">
<a href="#instance_charge_type_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>charge_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="spot_strategy_python">
<a href="#spot_strategy_python" style="color: inherit; text-decoration: inherit;">spot_<wbr>strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Filter the results by ECS spot type. Valid values: `NoSpot`, `SpotWithPriceLimit` and `SpotAsPriceGo`. Default to `NoSpot`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zone_id_python">
<a href="#zone_id_python" style="color: inherit; text-decoration: inherit;">zone_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getInstanceTypeFamilies Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="families_csharp">
<a href="#families_csharp" style="color: inherit; text-decoration: inherit;">Families</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypefamiliesfamily">List&lt;Pulumi.<wbr>Ali<wbr>Cloud.<wbr>Ecs.<wbr>Outputs.<wbr>Get<wbr>Instance<wbr>Type<wbr>Families<wbr>Family&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="ids_csharp">
<a href="#ids_csharp" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of instance type family IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="generation_csharp">
<a href="#generation_csharp" style="color: inherit; text-decoration: inherit;">Generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instancechargetype_csharp">
<a href="#instancechargetype_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Charge<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="spotstrategy_csharp">
<a href="#spotstrategy_csharp" style="color: inherit; text-decoration: inherit;">Spot<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zoneid_csharp">
<a href="#zoneid_csharp" style="color: inherit; text-decoration: inherit;">Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="families_go">
<a href="#families_go" style="color: inherit; text-decoration: inherit;">Families</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypefamiliesfamily">[]Get<wbr>Instance<wbr>Type<wbr>Families<wbr>Family</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="ids_go">
<a href="#ids_go" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of instance type family IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="generation_go">
<a href="#generation_go" style="color: inherit; text-decoration: inherit;">Generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instancechargetype_go">
<a href="#instancechargetype_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Charge<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="spotstrategy_go">
<a href="#spotstrategy_go" style="color: inherit; text-decoration: inherit;">Spot<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zoneid_go">
<a href="#zoneid_go" style="color: inherit; text-decoration: inherit;">Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="families_nodejs">
<a href="#families_nodejs" style="color: inherit; text-decoration: inherit;">families</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypefamiliesfamily">Get<wbr>Instance<wbr>Type<wbr>Families<wbr>Family[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="ids_nodejs">
<a href="#ids_nodejs" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of instance type family IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="generation_nodejs">
<a href="#generation_nodejs" style="color: inherit; text-decoration: inherit;">generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instancechargetype_nodejs">
<a href="#instancechargetype_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Charge<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="spotstrategy_nodejs">
<a href="#spotstrategy_nodejs" style="color: inherit; text-decoration: inherit;">spot<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zoneid_nodejs">
<a href="#zoneid_nodejs" style="color: inherit; text-decoration: inherit;">zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="families_python">
<a href="#families_python" style="color: inherit; text-decoration: inherit;">families</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypefamiliesfamily">Sequence[Get<wbr>Instance<wbr>Type<wbr>Families<wbr>Family]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="ids_python">
<a href="#ids_python" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of instance type family IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="generation_python">
<a href="#generation_python" style="color: inherit; text-decoration: inherit;">generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instance_charge_type_python">
<a href="#instance_charge_type_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>charge_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="spot_strategy_python">
<a href="#spot_strategy_python" style="color: inherit; text-decoration: inherit;">spot_<wbr>strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zone_id_python">
<a href="#zone_id_python" style="color: inherit; text-decoration: inherit;">zone_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getinstancetypefamiliesfamily">Get<wbr>Instance<wbr>Type<wbr>Families<wbr>Family</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="generation_csharp">
<a href="#generation_csharp" style="color: inherit; text-decoration: inherit;">Generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the instance type family.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="zoneids_csharp">
<a href="#zoneids_csharp" style="color: inherit; text-decoration: inherit;">Zone<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="generation_go">
<a href="#generation_go" style="color: inherit; text-decoration: inherit;">Generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the instance type family.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="zoneids_go">
<a href="#zoneids_go" style="color: inherit; text-decoration: inherit;">Zone<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="generation_nodejs">
<a href="#generation_nodejs" style="color: inherit; text-decoration: inherit;">generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the instance type family.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="zoneids_nodejs">
<a href="#zoneids_nodejs" style="color: inherit; text-decoration: inherit;">zone<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="generation_python">
<a href="#generation_python" style="color: inherit; text-decoration: inherit;">generation</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The generation of the instance type family, Valid values: `ecs-1`, `ecs-2`, `ecs-3` and `ecs-4`. For more information, see [Instance type families](https://www.alibabacloud.com/help/doc-detail/25378.htm).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the instance type family.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="zone_ids_python">
<a href="#zone_ids_python" style="color: inherit; text-decoration: inherit;">zone_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of Zone to launch the instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`alicloud` Terraform Provider](https://github.com/aliyun/terraform-provider-alicloud).{{% /md %}}</dd>
</dl>


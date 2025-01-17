
---
title: "getApp"
title_tag: "okta.app.getApp"
meta_desc: "Documentation for the okta.app.getApp function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to retrieve the collaborators for a given repository.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Okta = Pulumi.Okta;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Okta.App.GetApp.InvokeAsync(new Okta.App.GetAppArgs
        {
            Label = "Example App",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-okta/sdk/v2/go/okta/app"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "Example App"
		_, err := app.GetApp(ctx, &app.GetAppArgs{
			Label: &opt0,
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
import pulumi_okta as okta

example = okta.app.get_app(label="Example App")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as okta from "@pulumi/okta";

const example = pulumi.output(okta.app.getApp({
    label: "Example App",
}, { async: true }));
```


{{< /example >}}





{{% /examples %}}




## Using getApp {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getApp<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetAppArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetAppResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_app(</span><span class="nx">active_only</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">, </span><span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">label</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">label_prefix</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetAppResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetApp<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">GetAppArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetAppResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetApp` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetApp </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetAppResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetAppArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="activeonly_csharp">
<a href="#activeonly_csharp" style="color: inherit; text-decoration: inherit;">Active<wbr>Only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}tells the provider to query for only `ACTIVE` applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`id` of application to retrieve, conflicts with `label` and `label_prefix`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_csharp">
<a href="#label_csharp" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The label of the app to retrieve, conflicts with `label_prefix` and `id`. Label uses the `?q=<label>` query parameter exposed by Okta's API. It should be noted that at this time this searches both `name` and `label`. This is used to avoid paginating through all applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="labelprefix_csharp">
<a href="#labelprefix_csharp" style="color: inherit; text-decoration: inherit;">Label<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Label prefix of the app to retrieve, conflicts with `label` and `id`. This will tell the provider to do a `starts with` query as opposed to an `equals` query.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="activeonly_go">
<a href="#activeonly_go" style="color: inherit; text-decoration: inherit;">Active<wbr>Only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}tells the provider to query for only `ACTIVE` applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`id` of application to retrieve, conflicts with `label` and `label_prefix`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_go">
<a href="#label_go" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The label of the app to retrieve, conflicts with `label_prefix` and `id`. Label uses the `?q=<label>` query parameter exposed by Okta's API. It should be noted that at this time this searches both `name` and `label`. This is used to avoid paginating through all applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="labelprefix_go">
<a href="#labelprefix_go" style="color: inherit; text-decoration: inherit;">Label<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Label prefix of the app to retrieve, conflicts with `label` and `id`. This will tell the provider to do a `starts with` query as opposed to an `equals` query.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="activeonly_nodejs">
<a href="#activeonly_nodejs" style="color: inherit; text-decoration: inherit;">active<wbr>Only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}tells the provider to query for only `ACTIVE` applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`id` of application to retrieve, conflicts with `label` and `label_prefix`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_nodejs">
<a href="#label_nodejs" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The label of the app to retrieve, conflicts with `label_prefix` and `id`. Label uses the `?q=<label>` query parameter exposed by Okta's API. It should be noted that at this time this searches both `name` and `label`. This is used to avoid paginating through all applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="labelprefix_nodejs">
<a href="#labelprefix_nodejs" style="color: inherit; text-decoration: inherit;">label<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Label prefix of the app to retrieve, conflicts with `label` and `id`. This will tell the provider to do a `starts with` query as opposed to an `equals` query.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="active_only_python">
<a href="#active_only_python" style="color: inherit; text-decoration: inherit;">active_<wbr>only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}tells the provider to query for only `ACTIVE` applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`id` of application to retrieve, conflicts with `label` and `label_prefix`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_python">
<a href="#label_python" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The label of the app to retrieve, conflicts with `label_prefix` and `id`. Label uses the `?q=<label>` query parameter exposed by Okta's API. It should be noted that at this time this searches both `name` and `label`. This is used to avoid paginating through all applications.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_prefix_python">
<a href="#label_prefix_python" style="color: inherit; text-decoration: inherit;">label_<wbr>prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Label prefix of the app to retrieve, conflicts with `label` and `id`. This will tell the provider to do a `starts with` query as opposed to an `equals` query.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getApp Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`name` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_csharp">
<a href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`status` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="activeonly_csharp">
<a href="#activeonly_csharp" style="color: inherit; text-decoration: inherit;">Active<wbr>Only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`id` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_csharp">
<a href="#label_csharp" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`label` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labelprefix_csharp">
<a href="#labelprefix_csharp" style="color: inherit; text-decoration: inherit;">Label<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`name` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_go">
<a href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`status` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="activeonly_go">
<a href="#activeonly_go" style="color: inherit; text-decoration: inherit;">Active<wbr>Only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`id` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_go">
<a href="#label_go" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`label` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labelprefix_go">
<a href="#labelprefix_go" style="color: inherit; text-decoration: inherit;">Label<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`name` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_nodejs">
<a href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`status` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="activeonly_nodejs">
<a href="#activeonly_nodejs" style="color: inherit; text-decoration: inherit;">active<wbr>Only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`id` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_nodejs">
<a href="#label_nodejs" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`label` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labelprefix_nodejs">
<a href="#labelprefix_nodejs" style="color: inherit; text-decoration: inherit;">label<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`name` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_python">
<a href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`status` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="active_only_python">
<a href="#active_only_python" style="color: inherit; text-decoration: inherit;">active_<wbr>only</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`id` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_python">
<a href="#label_python" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`label` of application.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_prefix_python">
<a href="#label_prefix_python" style="color: inherit; text-decoration: inherit;">label_<wbr>prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-okta">https://github.com/pulumi/pulumi-okta</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`okta` Terraform Provider](https://github.com/oktadeveloper/terraform-provider-okta).{{% /md %}}</dd>
</dl>


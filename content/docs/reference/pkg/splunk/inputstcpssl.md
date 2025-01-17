
---
title: "InputsTcpSsl"
title_tag: "splunk.InputsTcpSsl"
meta_desc: "Documentation for the splunk.InputsTcpSsl resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

## # Resource: splunk.InputsTcpSsl

Access or update the SSL configuration for the host.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Splunk = Pulumi.Splunk;

class MyStack : Stack
{
    public MyStack()
    {
        var test = new Splunk.InputsTcpSsl("test", new Splunk.InputsTcpSslArgs
        {
            Disabled = false,
            RequireClientCert = true,
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-splunk/sdk/go/splunk"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := splunk.NewInputsTcpSsl(ctx, "test", &splunk.InputsTcpSslArgs{
			Disabled:          pulumi.Bool(false),
			RequireClientCert: pulumi.Bool(true),
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
import pulumi_splunk as splunk

test = splunk.InputsTcpSsl("test",
    disabled=False,
    require_client_cert=True)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as splunk from "@pulumi/splunk";

const test = new splunk.InputsTcpSsl("test", {
    disabled: false,
    requireClientCert: true,
});
```


{{< /example >}}





{{% /examples %}}




## Create a InputsTcpSsl Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">InputsTcpSsl</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p">?:</span> <span class="nx"><a href="#inputs">InputsTcpSslArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nx">InputsTcpSsl</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">, </span><span class="nx">disabled</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">, </span><span class="nx">password</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">require_client_cert</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">, </span><span class="nx">root_ca</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">server_cert</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewInputsTcpSsl</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx"><a href="#inputs">InputsTcpSslArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">InputsTcpSsl</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">InputsTcpSsl</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">, </span><span class="nx"><a href="#inputs">InputsTcpSslArgs</a></span><span class="p">? </span><span class="nx">args = null<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">InputsTcpSslArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">InputsTcpSslArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">InputsTcpSslArgs</a></span>
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

## InputsTcpSsl Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Programming Model docs.

### Inputs

The InputsTcpSsl resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="disabled_csharp">
<a href="#disabled_csharp" style="color: inherit; text-decoration: inherit;">Disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="password_csharp">
<a href="#password_csharp" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requireclientcert_csharp">
<a href="#requireclientcert_csharp" style="color: inherit; text-decoration: inherit;">Require<wbr>Client<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="rootca_csharp">
<a href="#rootca_csharp" style="color: inherit; text-decoration: inherit;">Root<wbr>Ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="servercert_csharp">
<a href="#servercert_csharp" style="color: inherit; text-decoration: inherit;">Server<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="disabled_go">
<a href="#disabled_go" style="color: inherit; text-decoration: inherit;">Disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="password_go">
<a href="#password_go" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requireclientcert_go">
<a href="#requireclientcert_go" style="color: inherit; text-decoration: inherit;">Require<wbr>Client<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="rootca_go">
<a href="#rootca_go" style="color: inherit; text-decoration: inherit;">Root<wbr>Ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="servercert_go">
<a href="#servercert_go" style="color: inherit; text-decoration: inherit;">Server<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="disabled_nodejs">
<a href="#disabled_nodejs" style="color: inherit; text-decoration: inherit;">disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="password_nodejs">
<a href="#password_nodejs" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requireclientcert_nodejs">
<a href="#requireclientcert_nodejs" style="color: inherit; text-decoration: inherit;">require<wbr>Client<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="rootca_nodejs">
<a href="#rootca_nodejs" style="color: inherit; text-decoration: inherit;">root<wbr>Ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="servercert_nodejs">
<a href="#servercert_nodejs" style="color: inherit; text-decoration: inherit;">server<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="disabled_python">
<a href="#disabled_python" style="color: inherit; text-decoration: inherit;">disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="password_python">
<a href="#password_python" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="require_client_cert_python">
<a href="#require_client_cert_python" style="color: inherit; text-decoration: inherit;">require_<wbr>client_<wbr>cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="root_ca_python">
<a href="#root_ca_python" style="color: inherit; text-decoration: inherit;">root_<wbr>ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="server_cert_python">
<a href="#server_cert_python" style="color: inherit; text-decoration: inherit;">server_<wbr>cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the InputsTcpSsl resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing InputsTcpSsl Resource {#look-up}

Get an existing InputsTcpSsl resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">, </span><span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span><span class="p">?:</span> <span class="nx">InputsTcpSslState</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">InputsTcpSsl</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">, </span><span class="nx">disabled</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">, </span><span class="nx">password</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">require_client_cert</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">, </span><span class="nx">root_ca</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">server_cert</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> InputsTcpSsl</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetInputsTcpSsl<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">, </span><span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span><span class="p"> *</span><span class="nx">InputsTcpSslState</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">InputsTcpSsl</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">InputsTcpSsl</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">, </span><span class="nx">InputsTcpSslState</span><span class="p">? </span><span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_disabled_csharp">
<a href="#state_disabled_csharp" style="color: inherit; text-decoration: inherit;">Disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_password_csharp">
<a href="#state_password_csharp" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_requireclientcert_csharp">
<a href="#state_requireclientcert_csharp" style="color: inherit; text-decoration: inherit;">Require<wbr>Client<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_rootca_csharp">
<a href="#state_rootca_csharp" style="color: inherit; text-decoration: inherit;">Root<wbr>Ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_servercert_csharp">
<a href="#state_servercert_csharp" style="color: inherit; text-decoration: inherit;">Server<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_disabled_go">
<a href="#state_disabled_go" style="color: inherit; text-decoration: inherit;">Disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_password_go">
<a href="#state_password_go" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_requireclientcert_go">
<a href="#state_requireclientcert_go" style="color: inherit; text-decoration: inherit;">Require<wbr>Client<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_rootca_go">
<a href="#state_rootca_go" style="color: inherit; text-decoration: inherit;">Root<wbr>Ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_servercert_go">
<a href="#state_servercert_go" style="color: inherit; text-decoration: inherit;">Server<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_disabled_nodejs">
<a href="#state_disabled_nodejs" style="color: inherit; text-decoration: inherit;">disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_password_nodejs">
<a href="#state_password_nodejs" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_requireclientcert_nodejs">
<a href="#state_requireclientcert_nodejs" style="color: inherit; text-decoration: inherit;">require<wbr>Client<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_rootca_nodejs">
<a href="#state_rootca_nodejs" style="color: inherit; text-decoration: inherit;">root<wbr>Ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_servercert_nodejs">
<a href="#state_servercert_nodejs" style="color: inherit; text-decoration: inherit;">server<wbr>Cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_disabled_python">
<a href="#state_disabled_python" style="color: inherit; text-decoration: inherit;">disabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if input is disabled.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_password_python">
<a href="#state_password_python" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Server certificate password, if any.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_require_client_cert_python">
<a href="#state_require_client_cert_python" style="color: inherit; text-decoration: inherit;">require_<wbr>client_<wbr>cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a client must authenticate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_root_ca_python">
<a href="#state_root_ca_python" style="color: inherit; text-decoration: inherit;">root_<wbr>ca</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Certificate authority list (root file)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_server_cert_python">
<a href="#state_server_cert_python" style="color: inherit; text-decoration: inherit;">server_<wbr>cert</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Full path to the server certificate.
{{% /md %}}</dd></dl>
{{% /choosable %}}







<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-splunk">https://github.com/pulumi/pulumi-splunk</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`splunk` Terraform Provider](https://github.com/splunk/terraform-provider-splunk).{{% /md %}}</dd>
</dl>


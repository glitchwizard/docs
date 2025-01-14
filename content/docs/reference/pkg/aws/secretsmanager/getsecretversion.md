
---
title: "getSecretVersion"
title_tag: "aws.secretsmanager.getSecretVersion"
meta_desc: "Documentation for the aws.secretsmanager.getSecretVersion function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Retrieve information about a Secrets Manager secret version, including its secret value. To retrieve secret metadata, see the `aws.secretsmanager.Secret` data source.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Retrieve Current Secret Version


{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Aws.SecretsManager.GetSecretVersion.InvokeAsync(new Aws.SecretsManager.GetSecretVersionArgs
        {
            SecretId = data.Aws_secretsmanager_secret.Example.Id,
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v3/go/aws/secretsmanager"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := secretsmanager.LookupSecretVersion(ctx, &secretsmanager.LookupSecretVersionArgs{
			SecretId: data.Aws_secretsmanager_secret.Example.Id,
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
import pulumi_aws as aws

example = aws.secretsmanager.get_secret_version(secret_id=data["aws_secretsmanager_secret"]["example"]["id"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = aws.secretsmanager.getSecretVersion({
    secretId: data.aws_secretsmanager_secret.example.id,
});
```


{{< /example >}}




### Retrieve Specific Secret Version


{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var by_version_stage = Output.Create(Aws.SecretsManager.GetSecretVersion.InvokeAsync(new Aws.SecretsManager.GetSecretVersionArgs
        {
            SecretId = data.Aws_secretsmanager_secret.Example.Id,
            VersionStage = "example",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v3/go/aws/secretsmanager"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "example"
		_, err := secretsmanager.LookupSecretVersion(ctx, &secretsmanager.LookupSecretVersionArgs{
			SecretId:     data.Aws_secretsmanager_secret.Example.Id,
			VersionStage: &opt0,
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
import pulumi_aws as aws

by_version_stage = aws.secretsmanager.get_secret_version(secret_id=data["aws_secretsmanager_secret"]["example"]["id"],
    version_stage="example")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const by-version-stage = aws.secretsmanager.getSecretVersion({
    secretId: data.aws_secretsmanager_secret.example.id,
    versionStage: "example",
});
```


{{< /example >}}





{{% /examples %}}




## Using getSecretVersion {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getSecretVersion<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetSecretVersionArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetSecretVersionResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_secret_version(</span><span class="nx">secret_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">version_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">version_stage</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetSecretVersionResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupSecretVersion<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">LookupSecretVersionArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupSecretVersionResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupSecretVersion` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetSecretVersion </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetSecretVersionResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetSecretVersionArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="secretid_csharp">
<a href="#secretid_csharp" style="color: inherit; text-decoration: inherit;">Secret<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the secret containing the version that you want to retrieve. You can specify either the Amazon Resource Name (ARN) or the friendly name of the secret.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="versionid_csharp">
<a href="#versionid_csharp" style="color: inherit; text-decoration: inherit;">Version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the unique identifier of the version of the secret that you want to retrieve. Overrides `version_stage`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="versionstage_csharp">
<a href="#versionstage_csharp" style="color: inherit; text-decoration: inherit;">Version<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the secret version that you want to retrieve by the staging label attached to the version. Defaults to `AWSCURRENT`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="secretid_go">
<a href="#secretid_go" style="color: inherit; text-decoration: inherit;">Secret<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the secret containing the version that you want to retrieve. You can specify either the Amazon Resource Name (ARN) or the friendly name of the secret.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="versionid_go">
<a href="#versionid_go" style="color: inherit; text-decoration: inherit;">Version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the unique identifier of the version of the secret that you want to retrieve. Overrides `version_stage`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="versionstage_go">
<a href="#versionstage_go" style="color: inherit; text-decoration: inherit;">Version<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the secret version that you want to retrieve by the staging label attached to the version. Defaults to `AWSCURRENT`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="secretid_nodejs">
<a href="#secretid_nodejs" style="color: inherit; text-decoration: inherit;">secret<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the secret containing the version that you want to retrieve. You can specify either the Amazon Resource Name (ARN) or the friendly name of the secret.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="versionid_nodejs">
<a href="#versionid_nodejs" style="color: inherit; text-decoration: inherit;">version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the unique identifier of the version of the secret that you want to retrieve. Overrides `version_stage`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="versionstage_nodejs">
<a href="#versionstage_nodejs" style="color: inherit; text-decoration: inherit;">version<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the secret version that you want to retrieve by the staging label attached to the version. Defaults to `AWSCURRENT`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="secret_id_python">
<a href="#secret_id_python" style="color: inherit; text-decoration: inherit;">secret_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the secret containing the version that you want to retrieve. You can specify either the Amazon Resource Name (ARN) or the friendly name of the secret.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="version_id_python">
<a href="#version_id_python" style="color: inherit; text-decoration: inherit;">version_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the unique identifier of the version of the secret that you want to retrieve. Overrides `version_stage`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="version_stage_python">
<a href="#version_stage_python" style="color: inherit; text-decoration: inherit;">version_<wbr>stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the secret version that you want to retrieve by the staging label attached to the version. Defaults to `AWSCURRENT`.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getSecretVersion Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_csharp">
<a href="#arn_csharp" style="color: inherit; text-decoration: inherit;">Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the secret.
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
        <span id="secretbinary_csharp">
<a href="#secretbinary_csharp" style="color: inherit; text-decoration: inherit;">Secret<wbr>Binary</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a binary. Base64 encoded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secretid_csharp">
<a href="#secretid_csharp" style="color: inherit; text-decoration: inherit;">Secret<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secretstring_csharp">
<a href="#secretstring_csharp" style="color: inherit; text-decoration: inherit;">Secret<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a string.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionid_csharp">
<a href="#versionid_csharp" style="color: inherit; text-decoration: inherit;">Version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this version of the secret.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionstages_csharp">
<a href="#versionstages_csharp" style="color: inherit; text-decoration: inherit;">Version<wbr>Stages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionstage_csharp">
<a href="#versionstage_csharp" style="color: inherit; text-decoration: inherit;">Version<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_go">
<a href="#arn_go" style="color: inherit; text-decoration: inherit;">Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the secret.
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
        <span id="secretbinary_go">
<a href="#secretbinary_go" style="color: inherit; text-decoration: inherit;">Secret<wbr>Binary</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a binary. Base64 encoded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secretid_go">
<a href="#secretid_go" style="color: inherit; text-decoration: inherit;">Secret<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secretstring_go">
<a href="#secretstring_go" style="color: inherit; text-decoration: inherit;">Secret<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a string.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionid_go">
<a href="#versionid_go" style="color: inherit; text-decoration: inherit;">Version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this version of the secret.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionstages_go">
<a href="#versionstages_go" style="color: inherit; text-decoration: inherit;">Version<wbr>Stages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionstage_go">
<a href="#versionstage_go" style="color: inherit; text-decoration: inherit;">Version<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_nodejs">
<a href="#arn_nodejs" style="color: inherit; text-decoration: inherit;">arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the secret.
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
        <span id="secretbinary_nodejs">
<a href="#secretbinary_nodejs" style="color: inherit; text-decoration: inherit;">secret<wbr>Binary</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a binary. Base64 encoded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secretid_nodejs">
<a href="#secretid_nodejs" style="color: inherit; text-decoration: inherit;">secret<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secretstring_nodejs">
<a href="#secretstring_nodejs" style="color: inherit; text-decoration: inherit;">secret<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a string.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionid_nodejs">
<a href="#versionid_nodejs" style="color: inherit; text-decoration: inherit;">version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this version of the secret.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionstages_nodejs">
<a href="#versionstages_nodejs" style="color: inherit; text-decoration: inherit;">version<wbr>Stages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versionstage_nodejs">
<a href="#versionstage_nodejs" style="color: inherit; text-decoration: inherit;">version<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_python">
<a href="#arn_python" style="color: inherit; text-decoration: inherit;">arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the secret.
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
        <span id="secret_binary_python">
<a href="#secret_binary_python" style="color: inherit; text-decoration: inherit;">secret_<wbr>binary</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a binary. Base64 encoded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secret_id_python">
<a href="#secret_id_python" style="color: inherit; text-decoration: inherit;">secret_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secret_string_python">
<a href="#secret_string_python" style="color: inherit; text-decoration: inherit;">secret_<wbr>string</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The decrypted part of the protected secret information that was originally provided as a string.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="version_id_python">
<a href="#version_id_python" style="color: inherit; text-decoration: inherit;">version_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this version of the secret.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="version_stages_python">
<a href="#version_stages_python" style="color: inherit; text-decoration: inherit;">version_<wbr>stages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="version_stage_python">
<a href="#version_stage_python" style="color: inherit; text-decoration: inherit;">version_<wbr>stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).{{% /md %}}</dd>
</dl>


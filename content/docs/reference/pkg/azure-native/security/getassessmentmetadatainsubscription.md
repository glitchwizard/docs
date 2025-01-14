
---
title: "getAssessmentMetadataInSubscription"
title_tag: "azure-native.security.getAssessmentMetadataInSubscription"
meta_desc: "Documentation for the azure-native.security.getAssessmentMetadataInSubscription function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Security assessment metadata
API Version: 2020-01-01.




## Using getAssessmentMetadataInSubscription {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getAssessmentMetadataInSubscription<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetAssessmentMetadataInSubscriptionArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetAssessmentMetadataInSubscriptionResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_assessment_metadata_in_subscription(</span><span class="nx">assessment_metadata_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetAssessmentMetadataInSubscriptionResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupAssessmentMetadataInSubscription<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">LookupAssessmentMetadataInSubscriptionArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupAssessmentMetadataInSubscriptionResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupAssessmentMetadataInSubscription` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetAssessmentMetadataInSubscription </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetAssessmentMetadataInSubscriptionResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetAssessmentMetadataInSubscriptionArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="assessmentmetadataname_csharp">
<a href="#assessmentmetadataname_csharp" style="color: inherit; text-decoration: inherit;">Assessment<wbr>Metadata<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Assessment Key - Unique key for the assessment type{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="assessmentmetadataname_go">
<a href="#assessmentmetadataname_go" style="color: inherit; text-decoration: inherit;">Assessment<wbr>Metadata<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Assessment Key - Unique key for the assessment type{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="assessmentmetadataname_nodejs">
<a href="#assessmentmetadataname_nodejs" style="color: inherit; text-decoration: inherit;">assessment<wbr>Metadata<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Assessment Key - Unique key for the assessment type{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="assessment_metadata_name_python">
<a href="#assessment_metadata_name_python" style="color: inherit; text-decoration: inherit;">assessment_<wbr>metadata_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Assessment Key - Unique key for the assessment type{{% /md %}}</dd></dl>
{{% /choosable %}}




## getAssessmentMetadataInSubscription Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="assessmenttype_csharp">
<a href="#assessmenttype_csharp" style="color: inherit; text-decoration: inherit;">Assessment<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}BuiltIn if the assessment based on built-in Azure Policy definition, Custom if the assessment based on custom Azure Policy definition{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_csharp">
<a href="#displayname_csharp" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User friendly display name of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="policydefinitionid_csharp">
<a href="#policydefinitionid_csharp" style="color: inherit; text-decoration: inherit;">Policy<wbr>Definition<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource ID of the policy definition that turns this assessment calculation on{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_csharp">
<a href="#severity_csharp" style="color: inherit; text-decoration: inherit;">Severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The severity level of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="category_csharp">
<a href="#category_csharp" style="color: inherit; text-decoration: inherit;">Category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human readable description of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="implementationeffort_csharp">
<a href="#implementationeffort_csharp" style="color: inherit; text-decoration: inherit;">Implementation<wbr>Effort</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The implementation effort required to remediate this assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="partnerdata_csharp">
<a href="#partnerdata_csharp" style="color: inherit; text-decoration: inherit;">Partner<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#securityassessmentmetadatapartnerdataresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Security.<wbr>Outputs.<wbr>Security<wbr>Assessment<wbr>Metadata<wbr>Partner<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the partner that created the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="preview_csharp">
<a href="#preview_csharp" style="color: inherit; text-decoration: inherit;">Preview</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}True if this assessment is in preview release status{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="remediationdescription_csharp">
<a href="#remediationdescription_csharp" style="color: inherit; text-decoration: inherit;">Remediation<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human readable description of what you should do to mitigate this security issue{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="threats_csharp">
<a href="#threats_csharp" style="color: inherit; text-decoration: inherit;">Threats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userimpact_csharp">
<a href="#userimpact_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Impact</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user impact of the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="assessmenttype_go">
<a href="#assessmenttype_go" style="color: inherit; text-decoration: inherit;">Assessment<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}BuiltIn if the assessment based on built-in Azure Policy definition, Custom if the assessment based on custom Azure Policy definition{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_go">
<a href="#displayname_go" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User friendly display name of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="policydefinitionid_go">
<a href="#policydefinitionid_go" style="color: inherit; text-decoration: inherit;">Policy<wbr>Definition<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource ID of the policy definition that turns this assessment calculation on{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_go">
<a href="#severity_go" style="color: inherit; text-decoration: inherit;">Severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The severity level of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="category_go">
<a href="#category_go" style="color: inherit; text-decoration: inherit;">Category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human readable description of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="implementationeffort_go">
<a href="#implementationeffort_go" style="color: inherit; text-decoration: inherit;">Implementation<wbr>Effort</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The implementation effort required to remediate this assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="partnerdata_go">
<a href="#partnerdata_go" style="color: inherit; text-decoration: inherit;">Partner<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#securityassessmentmetadatapartnerdataresponse">Security<wbr>Assessment<wbr>Metadata<wbr>Partner<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the partner that created the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="preview_go">
<a href="#preview_go" style="color: inherit; text-decoration: inherit;">Preview</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}True if this assessment is in preview release status{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="remediationdescription_go">
<a href="#remediationdescription_go" style="color: inherit; text-decoration: inherit;">Remediation<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human readable description of what you should do to mitigate this security issue{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="threats_go">
<a href="#threats_go" style="color: inherit; text-decoration: inherit;">Threats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userimpact_go">
<a href="#userimpact_go" style="color: inherit; text-decoration: inherit;">User<wbr>Impact</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user impact of the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="assessmenttype_nodejs">
<a href="#assessmenttype_nodejs" style="color: inherit; text-decoration: inherit;">assessment<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}BuiltIn if the assessment based on built-in Azure Policy definition, Custom if the assessment based on custom Azure Policy definition{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_nodejs">
<a href="#displayname_nodejs" style="color: inherit; text-decoration: inherit;">display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User friendly display name of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="policydefinitionid_nodejs">
<a href="#policydefinitionid_nodejs" style="color: inherit; text-decoration: inherit;">policy<wbr>Definition<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource ID of the policy definition that turns this assessment calculation on{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_nodejs">
<a href="#severity_nodejs" style="color: inherit; text-decoration: inherit;">severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The severity level of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="category_nodejs">
<a href="#category_nodejs" style="color: inherit; text-decoration: inherit;">category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human readable description of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="implementationeffort_nodejs">
<a href="#implementationeffort_nodejs" style="color: inherit; text-decoration: inherit;">implementation<wbr>Effort</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The implementation effort required to remediate this assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="partnerdata_nodejs">
<a href="#partnerdata_nodejs" style="color: inherit; text-decoration: inherit;">partner<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#securityassessmentmetadatapartnerdataresponse">Security<wbr>Assessment<wbr>Metadata<wbr>Partner<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the partner that created the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="preview_nodejs">
<a href="#preview_nodejs" style="color: inherit; text-decoration: inherit;">preview</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}True if this assessment is in preview release status{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="remediationdescription_nodejs">
<a href="#remediationdescription_nodejs" style="color: inherit; text-decoration: inherit;">remediation<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human readable description of what you should do to mitigate this security issue{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="threats_nodejs">
<a href="#threats_nodejs" style="color: inherit; text-decoration: inherit;">threats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userimpact_nodejs">
<a href="#userimpact_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Impact</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user impact of the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="assessment_type_python">
<a href="#assessment_type_python" style="color: inherit; text-decoration: inherit;">assessment_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BuiltIn if the assessment based on built-in Azure Policy definition, Custom if the assessment based on custom Azure Policy definition{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="display_name_python">
<a href="#display_name_python" style="color: inherit; text-decoration: inherit;">display_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}User friendly display name of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="policy_definition_id_python">
<a href="#policy_definition_id_python" style="color: inherit; text-decoration: inherit;">policy_<wbr>definition_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure resource ID of the policy definition that turns this assessment calculation on{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_python">
<a href="#severity_python" style="color: inherit; text-decoration: inherit;">severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The severity level of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="category_python">
<a href="#category_python" style="color: inherit; text-decoration: inherit;">category</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human readable description of the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="implementation_effort_python">
<a href="#implementation_effort_python" style="color: inherit; text-decoration: inherit;">implementation_<wbr>effort</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The implementation effort required to remediate this assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="partner_data_python">
<a href="#partner_data_python" style="color: inherit; text-decoration: inherit;">partner_<wbr>data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#securityassessmentmetadatapartnerdataresponse">Security<wbr>Assessment<wbr>Metadata<wbr>Partner<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the partner that created the assessment{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="preview_python">
<a href="#preview_python" style="color: inherit; text-decoration: inherit;">preview</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}True if this assessment is in preview release status{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="remediation_description_python">
<a href="#remediation_description_python" style="color: inherit; text-decoration: inherit;">remediation_<wbr>description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human readable description of what you should do to mitigate this security issue{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="threats_python">
<a href="#threats_python" style="color: inherit; text-decoration: inherit;">threats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="user_impact_python">
<a href="#user_impact_python" style="color: inherit; text-decoration: inherit;">user_<wbr>impact</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The user impact of the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="securityassessmentmetadatapartnerdataresponse">Security<wbr>Assessment<wbr>Metadata<wbr>Partner<wbr>Data<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="partnername_csharp">
<a href="#partnername_csharp" style="color: inherit; text-decoration: inherit;">Partner<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the company of the partner{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="secret_csharp">
<a href="#secret_csharp" style="color: inherit; text-decoration: inherit;">Secret</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Secret to authenticate the partner and verify it created the assessment - write only{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="productname_csharp">
<a href="#productname_csharp" style="color: inherit; text-decoration: inherit;">Product<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the product of the partner that created the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="partnername_go">
<a href="#partnername_go" style="color: inherit; text-decoration: inherit;">Partner<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the company of the partner{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="secret_go">
<a href="#secret_go" style="color: inherit; text-decoration: inherit;">Secret</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Secret to authenticate the partner and verify it created the assessment - write only{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="productname_go">
<a href="#productname_go" style="color: inherit; text-decoration: inherit;">Product<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the product of the partner that created the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="partnername_nodejs">
<a href="#partnername_nodejs" style="color: inherit; text-decoration: inherit;">partner<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the company of the partner{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="secret_nodejs">
<a href="#secret_nodejs" style="color: inherit; text-decoration: inherit;">secret</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Secret to authenticate the partner and verify it created the assessment - write only{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="productname_nodejs">
<a href="#productname_nodejs" style="color: inherit; text-decoration: inherit;">product<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the product of the partner that created the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="partner_name_python">
<a href="#partner_name_python" style="color: inherit; text-decoration: inherit;">partner_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the company of the partner{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="secret_python">
<a href="#secret_python" style="color: inherit; text-decoration: inherit;">secret</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Secret to authenticate the partner and verify it created the assessment - write only{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="product_name_python">
<a href="#product_name_python" style="color: inherit; text-decoration: inherit;">product_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the product of the partner that created the assessment{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>


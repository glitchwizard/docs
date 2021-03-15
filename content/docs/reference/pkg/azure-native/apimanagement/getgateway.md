
---
title: "getGateway"
title_tag: "azure-native.apimanagement.getGateway"
meta_desc: "Documentation for the azure-native.apimanagement.getGateway function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Gateway details.
API Version: 2019-12-01.




## Using getGateway {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getGateway<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetGatewayArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetGatewayResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_gateway(</span><span class="nx">gateway_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">service_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetGatewayResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupGateway<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">LookupGatewayArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupGatewayResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupGateway` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetGateway </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetGatewayResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetGatewayArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gatewayid_csharp">
<a href="#gatewayid_csharp" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Gateway entity identifier. Must be unique in the current API Management service instance. Must not have value 'managed'{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servicename_csharp">
<a href="#servicename_csharp" style="color: inherit; text-decoration: inherit;">Service<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the API Management service.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gatewayid_go">
<a href="#gatewayid_go" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Gateway entity identifier. Must be unique in the current API Management service instance. Must not have value 'managed'{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servicename_go">
<a href="#servicename_go" style="color: inherit; text-decoration: inherit;">Service<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the API Management service.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gatewayid_nodejs">
<a href="#gatewayid_nodejs" style="color: inherit; text-decoration: inherit;">gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Gateway entity identifier. Must be unique in the current API Management service instance. Must not have value 'managed'{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servicename_nodejs">
<a href="#servicename_nodejs" style="color: inherit; text-decoration: inherit;">service<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the API Management service.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gateway_id_python">
<a href="#gateway_id_python" style="color: inherit; text-decoration: inherit;">gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Gateway entity identifier. Must be unique in the current API Management service instance. Must not have value 'managed'{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="service_name_python">
<a href="#service_name_python" style="color: inherit; text-decoration: inherit;">service_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the API Management service.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getGateway Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
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
    <dd>{{% md %}}Resource type for API Management resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Gateway description{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationdata_csharp">
<a href="#locationdata_csharp" style="color: inherit; text-decoration: inherit;">Location<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#resourcelocationdatacontractresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Api<wbr>Management.<wbr>Outputs.<wbr>Resource<wbr>Location<wbr>Data<wbr>Contract<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Gateway location.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
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
    <dd>{{% md %}}Resource type for API Management resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Gateway description{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationdata_go">
<a href="#locationdata_go" style="color: inherit; text-decoration: inherit;">Location<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#resourcelocationdatacontractresponse">Resource<wbr>Location<wbr>Data<wbr>Contract<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Gateway location.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
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
    <dd>{{% md %}}Resource type for API Management resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Gateway description{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationdata_nodejs">
<a href="#locationdata_nodejs" style="color: inherit; text-decoration: inherit;">location<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#resourcelocationdatacontractresponse">Resource<wbr>Location<wbr>Data<wbr>Contract<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Gateway location.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
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
    <dd>{{% md %}}Resource type for API Management resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Gateway description{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_data_python">
<a href="#location_data_python" style="color: inherit; text-decoration: inherit;">location_<wbr>data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#resourcelocationdatacontractresponse">Resource<wbr>Location<wbr>Data<wbr>Contract<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Gateway location.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="resourcelocationdatacontractresponse">Resource<wbr>Location<wbr>Data<wbr>Contract<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A canonical name for the geographic or physical location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="city_csharp">
<a href="#city_csharp" style="color: inherit; text-decoration: inherit;">City</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The city or locality where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="countryorregion_csharp">
<a href="#countryorregion_csharp" style="color: inherit; text-decoration: inherit;">Country<wbr>Or<wbr>Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The country or region where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="district_csharp">
<a href="#district_csharp" style="color: inherit; text-decoration: inherit;">District</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The district, state, or province where the resource is located.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A canonical name for the geographic or physical location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="city_go">
<a href="#city_go" style="color: inherit; text-decoration: inherit;">City</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The city or locality where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="countryorregion_go">
<a href="#countryorregion_go" style="color: inherit; text-decoration: inherit;">Country<wbr>Or<wbr>Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The country or region where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="district_go">
<a href="#district_go" style="color: inherit; text-decoration: inherit;">District</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The district, state, or province where the resource is located.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A canonical name for the geographic or physical location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="city_nodejs">
<a href="#city_nodejs" style="color: inherit; text-decoration: inherit;">city</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The city or locality where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="countryorregion_nodejs">
<a href="#countryorregion_nodejs" style="color: inherit; text-decoration: inherit;">country<wbr>Or<wbr>Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The country or region where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="district_nodejs">
<a href="#district_nodejs" style="color: inherit; text-decoration: inherit;">district</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The district, state, or province where the resource is located.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A canonical name for the geographic or physical location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="city_python">
<a href="#city_python" style="color: inherit; text-decoration: inherit;">city</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The city or locality where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="country_or_region_python">
<a href="#country_or_region_python" style="color: inherit; text-decoration: inherit;">country_<wbr>or_<wbr>region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The country or region where the resource is located.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="district_python">
<a href="#district_python" style="color: inherit; text-decoration: inherit;">district</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The district, state, or province where the resource is located.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

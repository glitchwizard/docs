
---
title: "getGallery"
title_tag: "azure-native.compute.getGallery"
meta_desc: "Documentation for the azure-native.compute.getGallery function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Specifies information about the Shared Image Gallery that you want to create or update.
API Version: 2020-09-30.




## Using getGallery {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getGallery<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetGalleryArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetGalleryResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_gallery(</span><span class="nx">gallery_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">select</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetGalleryResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupGallery<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">LookupGalleryArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupGalleryResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupGallery` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetGallery </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetGalleryResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetGalleryArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="galleryname_csharp">
<a href="#galleryname_csharp" style="color: inherit; text-decoration: inherit;">Gallery<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Shared Image Gallery.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="select_csharp">
<a href="#select_csharp" style="color: inherit; text-decoration: inherit;">Select</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The select expression to apply on the operation.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="galleryname_go">
<a href="#galleryname_go" style="color: inherit; text-decoration: inherit;">Gallery<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Shared Image Gallery.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="select_go">
<a href="#select_go" style="color: inherit; text-decoration: inherit;">Select</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The select expression to apply on the operation.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="galleryname_nodejs">
<a href="#galleryname_nodejs" style="color: inherit; text-decoration: inherit;">gallery<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Shared Image Gallery.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="select_nodejs">
<a href="#select_nodejs" style="color: inherit; text-decoration: inherit;">select</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The select expression to apply on the operation.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gallery_name_python">
<a href="#gallery_name_python" style="color: inherit; text-decoration: inherit;">gallery_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Shared Image Gallery.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="select_python">
<a href="#select_python" style="color: inherit; text-decoration: inherit;">select</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The select expression to apply on the operation.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getGallery Result {#result}

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
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource location{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_csharp">
<a href="#provisioningstate_csharp" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state, which only appears in the response.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of this Shared Image Gallery resource. This property is updatable.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="identifier_csharp">
<a href="#identifier_csharp" style="color: inherit; text-decoration: inherit;">Identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#galleryidentifierresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Compute.<wbr>Outputs.<wbr>Gallery<wbr>Identifier<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the gallery unique name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sharingprofile_csharp">
<a href="#sharingprofile_csharp" style="color: inherit; text-decoration: inherit;">Sharing<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofileresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Compute.<wbr>Outputs.<wbr>Sharing<wbr>Profile<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Profile for gallery sharing to subscription or tenant{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Resource tags{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource location{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_go">
<a href="#provisioningstate_go" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state, which only appears in the response.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of this Shared Image Gallery resource. This property is updatable.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="identifier_go">
<a href="#identifier_go" style="color: inherit; text-decoration: inherit;">Identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#galleryidentifierresponse">Gallery<wbr>Identifier<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the gallery unique name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sharingprofile_go">
<a href="#sharingprofile_go" style="color: inherit; text-decoration: inherit;">Sharing<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofileresponse">Sharing<wbr>Profile<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Profile for gallery sharing to subscription or tenant{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Resource tags{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource location{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_nodejs">
<a href="#provisioningstate_nodejs" style="color: inherit; text-decoration: inherit;">provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state, which only appears in the response.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of this Shared Image Gallery resource. This property is updatable.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="identifier_nodejs">
<a href="#identifier_nodejs" style="color: inherit; text-decoration: inherit;">identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#galleryidentifierresponse">Gallery<wbr>Identifier<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the gallery unique name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sharingprofile_nodejs">
<a href="#sharingprofile_nodejs" style="color: inherit; text-decoration: inherit;">sharing<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofileresponse">Sharing<wbr>Profile<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Profile for gallery sharing to subscription or tenant{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Resource tags{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource location{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioning_state_python">
<a href="#provisioning_state_python" style="color: inherit; text-decoration: inherit;">provisioning_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provisioning state, which only appears in the response.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of this Shared Image Gallery resource. This property is updatable.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="identifier_python">
<a href="#identifier_python" style="color: inherit; text-decoration: inherit;">identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#galleryidentifierresponse">Gallery<wbr>Identifier<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Describes the gallery unique name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sharing_profile_python">
<a href="#sharing_profile_python" style="color: inherit; text-decoration: inherit;">sharing_<wbr>profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofileresponse">Sharing<wbr>Profile<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Profile for gallery sharing to subscription or tenant{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}Resource tags{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="galleryidentifierresponse">Gallery<wbr>Identifier<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="uniquename_csharp">
<a href="#uniquename_csharp" style="color: inherit; text-decoration: inherit;">Unique<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique name of the Shared Image Gallery. This name is generated automatically by Azure.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="uniquename_go">
<a href="#uniquename_go" style="color: inherit; text-decoration: inherit;">Unique<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique name of the Shared Image Gallery. This name is generated automatically by Azure.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="uniquename_nodejs">
<a href="#uniquename_nodejs" style="color: inherit; text-decoration: inherit;">unique<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique name of the Shared Image Gallery. This name is generated automatically by Azure.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="unique_name_python">
<a href="#unique_name_python" style="color: inherit; text-decoration: inherit;">unique_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique name of the Shared Image Gallery. This name is generated automatically by Azure.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="sharingprofilegroupresponse">Sharing<wbr>Profile<wbr>Group<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ids_csharp">
<a href="#ids_csharp" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of subscription/tenant ids the gallery is aimed to be shared to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the type of sharing group. <br><br> Possible values are: <br><br> **Subscriptions** <br><br> **AADTenants**{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ids_go">
<a href="#ids_go" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of subscription/tenant ids the gallery is aimed to be shared to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the type of sharing group. <br><br> Possible values are: <br><br> **Subscriptions** <br><br> **AADTenants**{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ids_nodejs">
<a href="#ids_nodejs" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of subscription/tenant ids the gallery is aimed to be shared to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the type of sharing group. <br><br> Possible values are: <br><br> **Subscriptions** <br><br> **AADTenants**{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ids_python">
<a href="#ids_python" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of subscription/tenant ids the gallery is aimed to be shared to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the type of sharing group. <br><br> Possible values are: <br><br> **Subscriptions** <br><br> **AADTenants**{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="sharingprofileresponse">Sharing<wbr>Profile<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="groups_csharp">
<a href="#groups_csharp" style="color: inherit; text-decoration: inherit;">Groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofilegroupresponse">List&lt;Pulumi.<wbr>Azure<wbr>Native.<wbr>Compute.<wbr>Inputs.<wbr>Sharing<wbr>Profile<wbr>Group<wbr>Response<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of sharing profile groups.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="permissions_csharp">
<a href="#permissions_csharp" style="color: inherit; text-decoration: inherit;">Permissions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the permission of sharing gallery. <br><br> Possible values are: <br><br> **Private** <br><br> **Groups**{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="groups_go">
<a href="#groups_go" style="color: inherit; text-decoration: inherit;">Groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofilegroupresponse">[]Sharing<wbr>Profile<wbr>Group<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}A list of sharing profile groups.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="permissions_go">
<a href="#permissions_go" style="color: inherit; text-decoration: inherit;">Permissions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the permission of sharing gallery. <br><br> Possible values are: <br><br> **Private** <br><br> **Groups**{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="groups_nodejs">
<a href="#groups_nodejs" style="color: inherit; text-decoration: inherit;">groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofilegroupresponse">Sharing<wbr>Profile<wbr>Group<wbr>Response[]</a></span>
    </dt>
    <dd>{{% md %}}A list of sharing profile groups.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="permissions_nodejs">
<a href="#permissions_nodejs" style="color: inherit; text-decoration: inherit;">permissions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the permission of sharing gallery. <br><br> Possible values are: <br><br> **Private** <br><br> **Groups**{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="groups_python">
<a href="#groups_python" style="color: inherit; text-decoration: inherit;">groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#sharingprofilegroupresponse">Sequence[Sharing<wbr>Profile<wbr>Group<wbr>Response<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}A list of sharing profile groups.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="permissions_python">
<a href="#permissions_python" style="color: inherit; text-decoration: inherit;">permissions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}This property allows you to specify the permission of sharing gallery. <br><br> Possible values are: <br><br> **Private** <br><br> **Groups**{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

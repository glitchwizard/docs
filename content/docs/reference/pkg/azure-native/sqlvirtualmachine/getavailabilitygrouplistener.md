
---
title: "getAvailabilityGroupListener"
title_tag: "azure-native.sqlvirtualmachine.getAvailabilityGroupListener"
meta_desc: "Documentation for the azure-native.sqlvirtualmachine.getAvailabilityGroupListener function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

A SQL Server availability group listener.
API Version: 2017-03-01-preview.




## Using getAvailabilityGroupListener {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getAvailabilityGroupListener<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetAvailabilityGroupListenerArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetAvailabilityGroupListenerResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_availability_group_listener(</span><span class="nx">availability_group_listener_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">sql_virtual_machine_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetAvailabilityGroupListenerResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupAvailabilityGroupListener<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">LookupAvailabilityGroupListenerArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupAvailabilityGroupListenerResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupAvailabilityGroupListener` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetAvailabilityGroupListener </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetAvailabilityGroupListenerResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetAvailabilityGroupListenerArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="availabilitygrouplistenername_csharp">
<a href="#availabilitygrouplistenername_csharp" style="color: inherit; text-decoration: inherit;">Availability<wbr>Group<wbr>Listener<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the availability group listener.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sqlvirtualmachinegroupname_csharp">
<a href="#sqlvirtualmachinegroupname_csharp" style="color: inherit; text-decoration: inherit;">Sql<wbr>Virtual<wbr>Machine<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the SQL virtual machine group.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="availabilitygrouplistenername_go">
<a href="#availabilitygrouplistenername_go" style="color: inherit; text-decoration: inherit;">Availability<wbr>Group<wbr>Listener<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the availability group listener.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sqlvirtualmachinegroupname_go">
<a href="#sqlvirtualmachinegroupname_go" style="color: inherit; text-decoration: inherit;">Sql<wbr>Virtual<wbr>Machine<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the SQL virtual machine group.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="availabilitygrouplistenername_nodejs">
<a href="#availabilitygrouplistenername_nodejs" style="color: inherit; text-decoration: inherit;">availability<wbr>Group<wbr>Listener<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the availability group listener.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sqlvirtualmachinegroupname_nodejs">
<a href="#sqlvirtualmachinegroupname_nodejs" style="color: inherit; text-decoration: inherit;">sql<wbr>Virtual<wbr>Machine<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the SQL virtual machine group.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="availability_group_listener_name_python">
<a href="#availability_group_listener_name_python" style="color: inherit; text-decoration: inherit;">availability_<wbr>group_<wbr>listener_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the availability group listener.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sql_virtual_machine_group_name_python">
<a href="#sql_virtual_machine_group_name_python" style="color: inherit; text-decoration: inherit;">sql_<wbr>virtual_<wbr>machine_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the SQL virtual machine group.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getAvailabilityGroupListener Result {#result}

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
        <span id="provisioningstate_csharp">
<a href="#provisioningstate_csharp" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Provisioning state to track the async operation status.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilitygroupname_csharp">
<a href="#availabilitygroupname_csharp" style="color: inherit; text-decoration: inherit;">Availability<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the availability group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="createdefaultavailabilitygroupifnotexist_csharp">
<a href="#createdefaultavailabilitygroupifnotexist_csharp" style="color: inherit; text-decoration: inherit;">Create<wbr>Default<wbr>Availability<wbr>Group<wbr>If<wbr>Not<wbr>Exist</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Create a default availability group if it does not exist.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="loadbalancerconfigurations_csharp">
<a href="#loadbalancerconfigurations_csharp" style="color: inherit; text-decoration: inherit;">Load<wbr>Balancer<wbr>Configurations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#loadbalancerconfigurationresponse">List&lt;Pulumi.<wbr>Azure<wbr>Native.<wbr>Sql<wbr>Virtual<wbr>Machine.<wbr>Outputs.<wbr>Load<wbr>Balancer<wbr>Configuration<wbr>Response&gt;</a></span>
    </dt>
    <dd>{{% md %}}List of load balancer configurations for an availability group listener.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="port_csharp">
<a href="#port_csharp" style="color: inherit; text-decoration: inherit;">Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Listener port.{{% /md %}}</dd></dl>
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
        <span id="provisioningstate_go">
<a href="#provisioningstate_go" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Provisioning state to track the async operation status.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilitygroupname_go">
<a href="#availabilitygroupname_go" style="color: inherit; text-decoration: inherit;">Availability<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the availability group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="createdefaultavailabilitygroupifnotexist_go">
<a href="#createdefaultavailabilitygroupifnotexist_go" style="color: inherit; text-decoration: inherit;">Create<wbr>Default<wbr>Availability<wbr>Group<wbr>If<wbr>Not<wbr>Exist</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Create a default availability group if it does not exist.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="loadbalancerconfigurations_go">
<a href="#loadbalancerconfigurations_go" style="color: inherit; text-decoration: inherit;">Load<wbr>Balancer<wbr>Configurations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#loadbalancerconfigurationresponse">[]Load<wbr>Balancer<wbr>Configuration<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}List of load balancer configurations for an availability group listener.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="port_go">
<a href="#port_go" style="color: inherit; text-decoration: inherit;">Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Listener port.{{% /md %}}</dd></dl>
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
        <span id="provisioningstate_nodejs">
<a href="#provisioningstate_nodejs" style="color: inherit; text-decoration: inherit;">provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Provisioning state to track the async operation status.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilitygroupname_nodejs">
<a href="#availabilitygroupname_nodejs" style="color: inherit; text-decoration: inherit;">availability<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the availability group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="createdefaultavailabilitygroupifnotexist_nodejs">
<a href="#createdefaultavailabilitygroupifnotexist_nodejs" style="color: inherit; text-decoration: inherit;">create<wbr>Default<wbr>Availability<wbr>Group<wbr>If<wbr>Not<wbr>Exist</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Create a default availability group if it does not exist.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="loadbalancerconfigurations_nodejs">
<a href="#loadbalancerconfigurations_nodejs" style="color: inherit; text-decoration: inherit;">load<wbr>Balancer<wbr>Configurations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#loadbalancerconfigurationresponse">Load<wbr>Balancer<wbr>Configuration<wbr>Response[]</a></span>
    </dt>
    <dd>{{% md %}}List of load balancer configurations for an availability group listener.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="port_nodejs">
<a href="#port_nodejs" style="color: inherit; text-decoration: inherit;">port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Listener port.{{% /md %}}</dd></dl>
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
        <span id="provisioning_state_python">
<a href="#provisioning_state_python" style="color: inherit; text-decoration: inherit;">provisioning_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Provisioning state to track the async operation status.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availability_group_name_python">
<a href="#availability_group_name_python" style="color: inherit; text-decoration: inherit;">availability_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the availability group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="create_default_availability_group_if_not_exist_python">
<a href="#create_default_availability_group_if_not_exist_python" style="color: inherit; text-decoration: inherit;">create_<wbr>default_<wbr>availability_<wbr>group_<wbr>if_<wbr>not_<wbr>exist</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Create a default availability group if it does not exist.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="load_balancer_configurations_python">
<a href="#load_balancer_configurations_python" style="color: inherit; text-decoration: inherit;">load_<wbr>balancer_<wbr>configurations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#loadbalancerconfigurationresponse">Sequence[Load<wbr>Balancer<wbr>Configuration<wbr>Response]</a></span>
    </dt>
    <dd>{{% md %}}List of load balancer configurations for an availability group listener.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="port_python">
<a href="#port_python" style="color: inherit; text-decoration: inherit;">port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Listener port.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="loadbalancerconfigurationresponse">Load<wbr>Balancer<wbr>Configuration<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="loadbalancerresourceid_csharp">
<a href="#loadbalancerresourceid_csharp" style="color: inherit; text-decoration: inherit;">Load<wbr>Balancer<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource id of the load balancer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="privateipaddress_csharp">
<a href="#privateipaddress_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateipaddressresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Sql<wbr>Virtual<wbr>Machine.<wbr>Inputs.<wbr>Private<wbr>IPAddress<wbr>Response<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Private IP address.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="probeport_csharp">
<a href="#probeport_csharp" style="color: inherit; text-decoration: inherit;">Probe<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Probe port.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipaddressresourceid_csharp">
<a href="#publicipaddressresourceid_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Address<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource id of the public IP.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sqlvirtualmachineinstances_csharp">
<a href="#sqlvirtualmachineinstances_csharp" style="color: inherit; text-decoration: inherit;">Sql<wbr>Virtual<wbr>Machine<wbr>Instances</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of the SQL virtual machine instance resource id's that are enrolled into the availability group listener.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="loadbalancerresourceid_go">
<a href="#loadbalancerresourceid_go" style="color: inherit; text-decoration: inherit;">Load<wbr>Balancer<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource id of the load balancer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="privateipaddress_go">
<a href="#privateipaddress_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateipaddressresponse">Private<wbr>IPAddress<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Private IP address.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="probeport_go">
<a href="#probeport_go" style="color: inherit; text-decoration: inherit;">Probe<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Probe port.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipaddressresourceid_go">
<a href="#publicipaddressresourceid_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Address<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource id of the public IP.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sqlvirtualmachineinstances_go">
<a href="#sqlvirtualmachineinstances_go" style="color: inherit; text-decoration: inherit;">Sql<wbr>Virtual<wbr>Machine<wbr>Instances</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of the SQL virtual machine instance resource id's that are enrolled into the availability group listener.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="loadbalancerresourceid_nodejs">
<a href="#loadbalancerresourceid_nodejs" style="color: inherit; text-decoration: inherit;">load<wbr>Balancer<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource id of the load balancer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="privateipaddress_nodejs">
<a href="#privateipaddress_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateipaddressresponse">Private<wbr>IPAddress<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Private IP address.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="probeport_nodejs">
<a href="#probeport_nodejs" style="color: inherit; text-decoration: inherit;">probe<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Probe port.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipaddressresourceid_nodejs">
<a href="#publicipaddressresourceid_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Ip<wbr>Address<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource id of the public IP.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sqlvirtualmachineinstances_nodejs">
<a href="#sqlvirtualmachineinstances_nodejs" style="color: inherit; text-decoration: inherit;">sql<wbr>Virtual<wbr>Machine<wbr>Instances</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of the SQL virtual machine instance resource id's that are enrolled into the availability group listener.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="load_balancer_resource_id_python">
<a href="#load_balancer_resource_id_python" style="color: inherit; text-decoration: inherit;">load_<wbr>balancer_<wbr>resource_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource id of the load balancer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="private_ip_address_python">
<a href="#private_ip_address_python" style="color: inherit; text-decoration: inherit;">private_<wbr>ip_<wbr>address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateipaddressresponse">Private<wbr>IPAddress<wbr>Response<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Private IP address.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="probe_port_python">
<a href="#probe_port_python" style="color: inherit; text-decoration: inherit;">probe_<wbr>port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Probe port.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="public_ip_address_resource_id_python">
<a href="#public_ip_address_resource_id_python" style="color: inherit; text-decoration: inherit;">public_<wbr>ip_<wbr>address_<wbr>resource_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource id of the public IP.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sql_virtual_machine_instances_python">
<a href="#sql_virtual_machine_instances_python" style="color: inherit; text-decoration: inherit;">sql_<wbr>virtual_<wbr>machine_<wbr>instances</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}List of the SQL virtual machine instance resource id's that are enrolled into the availability group listener.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="privateipaddressresponse">Private<wbr>IPAddress<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ipaddress_csharp">
<a href="#ipaddress_csharp" style="color: inherit; text-decoration: inherit;">Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Private IP address bound to the availability group listener.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subnetresourceid_csharp">
<a href="#subnetresourceid_csharp" style="color: inherit; text-decoration: inherit;">Subnet<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnet used to include private IP.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ipaddress_go">
<a href="#ipaddress_go" style="color: inherit; text-decoration: inherit;">Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Private IP address bound to the availability group listener.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subnetresourceid_go">
<a href="#subnetresourceid_go" style="color: inherit; text-decoration: inherit;">Subnet<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnet used to include private IP.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ipaddress_nodejs">
<a href="#ipaddress_nodejs" style="color: inherit; text-decoration: inherit;">ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Private IP address bound to the availability group listener.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subnetresourceid_nodejs">
<a href="#subnetresourceid_nodejs" style="color: inherit; text-decoration: inherit;">subnet<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnet used to include private IP.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="ip_address_python">
<a href="#ip_address_python" style="color: inherit; text-decoration: inherit;">ip_<wbr>address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Private IP address bound to the availability group listener.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subnet_resource_id_python">
<a href="#subnet_resource_id_python" style="color: inherit; text-decoration: inherit;">subnet_<wbr>resource_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Subnet used to include private IP.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>



---
title: "getSignalRPrivateEndpointConnection"
title_tag: "azure-native.signalrservice.getSignalRPrivateEndpointConnection"
meta_desc: "Documentation for the azure-native.signalrservice.getSignalRPrivateEndpointConnection function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

A private endpoint connection to SignalR resource
API Version: 2020-05-01.




## Using getSignalRPrivateEndpointConnection {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getSignalRPrivateEndpointConnection<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetSignalRPrivateEndpointConnectionArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetSignalRPrivateEndpointConnectionResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_signal_r_private_endpoint_connection(</span><span class="nx">private_endpoint_connection_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                             <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                             <span class="nx">resource_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetSignalRPrivateEndpointConnectionResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupSignalRPrivateEndpointConnection<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupSignalRPrivateEndpointConnectionArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupSignalRPrivateEndpointConnectionResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupSignalRPrivateEndpointConnection` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetSignalRPrivateEndpointConnection </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetSignalRPrivateEndpointConnectionResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetSignalRPrivateEndpointConnectionArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="privateendpointconnectionname_csharp">
<a href="#privateendpointconnectionname_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Endpoint<wbr>Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the private endpoint connection associated with the SignalR resource.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcename_csharp">
<a href="#resourcename_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the SignalR resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="privateendpointconnectionname_go">
<a href="#privateendpointconnectionname_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Endpoint<wbr>Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the private endpoint connection associated with the SignalR resource.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcename_go">
<a href="#resourcename_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the SignalR resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="privateendpointconnectionname_nodejs">
<a href="#privateendpointconnectionname_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Endpoint<wbr>Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the private endpoint connection associated with the SignalR resource.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcename_nodejs">
<a href="#resourcename_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the SignalR resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="private_endpoint_connection_name_python">
<a href="#private_endpoint_connection_name_python" style="color: inherit; text-decoration: inherit;">private_<wbr>endpoint_<wbr>connection_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the private endpoint connection associated with the SignalR resource.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_name_python">
<a href="#resource_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the SignalR resource.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getSignalRPrivateEndpointConnection Result {#result}

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
    <dd>{{% md %}}Fully qualified resource Id for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_csharp">
<a href="#provisioningstate_csharp" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource - e.g. "Microsoft.SignalRService/SignalR"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateendpoint_csharp">
<a href="#privateendpoint_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateendpointresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Signal<wbr>RService.<wbr>Outputs.<wbr>Private<wbr>Endpoint<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Private endpoint associated with the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkserviceconnectionstate_csharp">
<a href="#privatelinkserviceconnectionstate_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Link<wbr>Service<wbr>Connection<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privatelinkserviceconnectionstateresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Signal<wbr>RService.<wbr>Outputs.<wbr>Private<wbr>Link<wbr>Service<wbr>Connection<wbr>State<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Connection state{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Fully qualified resource Id for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_go">
<a href="#provisioningstate_go" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource - e.g. "Microsoft.SignalRService/SignalR"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateendpoint_go">
<a href="#privateendpoint_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateendpointresponse">Private<wbr>Endpoint<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Private endpoint associated with the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkserviceconnectionstate_go">
<a href="#privatelinkserviceconnectionstate_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Link<wbr>Service<wbr>Connection<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privatelinkserviceconnectionstateresponse">Private<wbr>Link<wbr>Service<wbr>Connection<wbr>State<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Connection state{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Fully qualified resource Id for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_nodejs">
<a href="#provisioningstate_nodejs" style="color: inherit; text-decoration: inherit;">provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource - e.g. "Microsoft.SignalRService/SignalR"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateendpoint_nodejs">
<a href="#privateendpoint_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateendpointresponse">Private<wbr>Endpoint<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Private endpoint associated with the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkserviceconnectionstate_nodejs">
<a href="#privatelinkserviceconnectionstate_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Link<wbr>Service<wbr>Connection<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privatelinkserviceconnectionstateresponse">Private<wbr>Link<wbr>Service<wbr>Connection<wbr>State<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Connection state{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Fully qualified resource Id for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioning_state_python">
<a href="#provisioning_state_python" style="color: inherit; text-decoration: inherit;">provisioning_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the resource - e.g. "Microsoft.SignalRService/SignalR"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="private_endpoint_python">
<a href="#private_endpoint_python" style="color: inherit; text-decoration: inherit;">private_<wbr>endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privateendpointresponse">Private<wbr>Endpoint<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Private endpoint associated with the private endpoint connection{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="private_link_service_connection_state_python">
<a href="#private_link_service_connection_state_python" style="color: inherit; text-decoration: inherit;">private_<wbr>link_<wbr>service_<wbr>connection_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#privatelinkserviceconnectionstateresponse">Private<wbr>Link<wbr>Service<wbr>Connection<wbr>State<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Connection state{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="privateendpointresponse">Private<wbr>Endpoint<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full qualified Id of the private endpoint{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full qualified Id of the private endpoint{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full qualified Id of the private endpoint{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Full qualified Id of the private endpoint{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="privatelinkserviceconnectionstateresponse">Private<wbr>Link<wbr>Service<wbr>Connection<wbr>State<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="actionsrequired_csharp">
<a href="#actionsrequired_csharp" style="color: inherit; text-decoration: inherit;">Actions<wbr>Required</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A message indicating if changes on the service provider require any updates on the consumer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The reason for approval/rejection of the connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_csharp">
<a href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Indicates whether the connection has been Approved/Rejected/Removed by the owner of the service.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="actionsrequired_go">
<a href="#actionsrequired_go" style="color: inherit; text-decoration: inherit;">Actions<wbr>Required</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A message indicating if changes on the service provider require any updates on the consumer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The reason for approval/rejection of the connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_go">
<a href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Indicates whether the connection has been Approved/Rejected/Removed by the owner of the service.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="actionsrequired_nodejs">
<a href="#actionsrequired_nodejs" style="color: inherit; text-decoration: inherit;">actions<wbr>Required</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A message indicating if changes on the service provider require any updates on the consumer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The reason for approval/rejection of the connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_nodejs">
<a href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Indicates whether the connection has been Approved/Rejected/Removed by the owner of the service.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="actions_required_python">
<a href="#actions_required_python" style="color: inherit; text-decoration: inherit;">actions_<wbr>required</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A message indicating if changes on the service provider require any updates on the consumer.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The reason for approval/rejection of the connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_python">
<a href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Indicates whether the connection has been Approved/Rejected/Removed by the owner of the service.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

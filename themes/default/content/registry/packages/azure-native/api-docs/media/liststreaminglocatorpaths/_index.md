
---
title: "listStreamingLocatorPaths"
title_tag: "azure-native.media.listStreamingLocatorPaths"
meta_desc: "Documentation for the azure-native.media.listStreamingLocatorPaths function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Class of response for listPaths action
API Version: 2020-05-01.




## Using listStreamingLocatorPaths {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>listStreamingLocatorPaths<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">ListStreamingLocatorPathsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">ListStreamingLocatorPathsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>list_streaming_locator_paths(</span><span class="nx">account_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">streaming_locator_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> ListStreamingLocatorPathsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>ListStreamingLocatorPaths<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">ListStreamingLocatorPathsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">ListStreamingLocatorPathsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `ListStreamingLocatorPaths` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">ListStreamingLocatorPaths </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">ListStreamingLocatorPathsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">ListStreamingLocatorPathsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accountname_csharp">
<a href="#accountname_csharp" style="color: inherit; text-decoration: inherit;">Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Media Services account name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the Azure subscription.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streaminglocatorname_csharp">
<a href="#streaminglocatorname_csharp" style="color: inherit; text-decoration: inherit;">Streaming<wbr>Locator<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Streaming Locator name.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accountname_go">
<a href="#accountname_go" style="color: inherit; text-decoration: inherit;">Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Media Services account name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the Azure subscription.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streaminglocatorname_go">
<a href="#streaminglocatorname_go" style="color: inherit; text-decoration: inherit;">Streaming<wbr>Locator<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Streaming Locator name.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accountname_nodejs">
<a href="#accountname_nodejs" style="color: inherit; text-decoration: inherit;">account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Media Services account name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the Azure subscription.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streaminglocatorname_nodejs">
<a href="#streaminglocatorname_nodejs" style="color: inherit; text-decoration: inherit;">streaming<wbr>Locator<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Streaming Locator name.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="account_name_python">
<a href="#account_name_python" style="color: inherit; text-decoration: inherit;">account_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Media Services account name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the Azure subscription.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streaming_locator_name_python">
<a href="#streaming_locator_name_python" style="color: inherit; text-decoration: inherit;">streaming_<wbr>locator_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Streaming Locator name.{{% /md %}}</dd></dl>
{{% /choosable %}}




## listStreamingLocatorPaths Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="downloadpaths_csharp">
<a href="#downloadpaths_csharp" style="color: inherit; text-decoration: inherit;">Download<wbr>Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Download Paths supported by current Streaming Locator{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="streamingpaths_csharp">
<a href="#streamingpaths_csharp" style="color: inherit; text-decoration: inherit;">Streaming<wbr>Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#streamingpathresponse">List&lt;Pulumi.<wbr>Azure<wbr>Native.<wbr>Media.<wbr>Outputs.<wbr>Streaming<wbr>Path<wbr>Response&gt;</a></span>
    </dt>
    <dd>{{% md %}}Streaming Paths supported by current Streaming Locator{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="downloadpaths_go">
<a href="#downloadpaths_go" style="color: inherit; text-decoration: inherit;">Download<wbr>Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Download Paths supported by current Streaming Locator{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="streamingpaths_go">
<a href="#streamingpaths_go" style="color: inherit; text-decoration: inherit;">Streaming<wbr>Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#streamingpathresponse">[]Streaming<wbr>Path<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Streaming Paths supported by current Streaming Locator{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="downloadpaths_nodejs">
<a href="#downloadpaths_nodejs" style="color: inherit; text-decoration: inherit;">download<wbr>Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Download Paths supported by current Streaming Locator{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="streamingpaths_nodejs">
<a href="#streamingpaths_nodejs" style="color: inherit; text-decoration: inherit;">streaming<wbr>Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#streamingpathresponse">Streaming<wbr>Path<wbr>Response[]</a></span>
    </dt>
    <dd>{{% md %}}Streaming Paths supported by current Streaming Locator{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="download_paths_python">
<a href="#download_paths_python" style="color: inherit; text-decoration: inherit;">download_<wbr>paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Download Paths supported by current Streaming Locator{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="streaming_paths_python">
<a href="#streaming_paths_python" style="color: inherit; text-decoration: inherit;">streaming_<wbr>paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#streamingpathresponse">Sequence[Streaming<wbr>Path<wbr>Response]</a></span>
    </dt>
    <dd>{{% md %}}Streaming Paths supported by current Streaming Locator{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="streamingpathresponse">Streaming<wbr>Path<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="encryptionscheme_csharp">
<a href="#encryptionscheme_csharp" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Scheme</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Encryption scheme{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streamingprotocol_csharp">
<a href="#streamingprotocol_csharp" style="color: inherit; text-decoration: inherit;">Streaming<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Streaming protocol{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="paths_csharp">
<a href="#paths_csharp" style="color: inherit; text-decoration: inherit;">Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Streaming paths for each protocol and encryptionScheme pair{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="encryptionscheme_go">
<a href="#encryptionscheme_go" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Scheme</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Encryption scheme{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streamingprotocol_go">
<a href="#streamingprotocol_go" style="color: inherit; text-decoration: inherit;">Streaming<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Streaming protocol{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="paths_go">
<a href="#paths_go" style="color: inherit; text-decoration: inherit;">Paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Streaming paths for each protocol and encryptionScheme pair{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="encryptionscheme_nodejs">
<a href="#encryptionscheme_nodejs" style="color: inherit; text-decoration: inherit;">encryption<wbr>Scheme</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Encryption scheme{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streamingprotocol_nodejs">
<a href="#streamingprotocol_nodejs" style="color: inherit; text-decoration: inherit;">streaming<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Streaming protocol{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="paths_nodejs">
<a href="#paths_nodejs" style="color: inherit; text-decoration: inherit;">paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Streaming paths for each protocol and encryptionScheme pair{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="encryption_scheme_python">
<a href="#encryption_scheme_python" style="color: inherit; text-decoration: inherit;">encryption_<wbr>scheme</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Encryption scheme{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="streaming_protocol_python">
<a href="#streaming_protocol_python" style="color: inherit; text-decoration: inherit;">streaming_<wbr>protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Streaming protocol{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="paths_python">
<a href="#paths_python" style="color: inherit; text-decoration: inherit;">paths</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Streaming paths for each protocol and encryptionScheme pair{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

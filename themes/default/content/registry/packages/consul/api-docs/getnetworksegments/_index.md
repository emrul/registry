
---
title: "getNetworkSegments"
title_tag: "consul.getNetworkSegments"
meta_desc: "Documentation for the consul.getNetworkSegments function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

> **NOTE:** This feature requires [Consul Enterprise](https://www.consul.io/docs/enterprise/index.html).

The `consul_network_segment` data source can be used to retrieve the network
segments defined in the configuration.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Consul = Pulumi.Consul;

class MyStack : Stack
{
    public MyStack()
    {
        var segmentsNetworkSegments = Output.Create(Consul.GetNetworkSegments.InvokeAsync());
        this.Segments = segmentsNetworkSegments.Apply(segmentsNetworkSegments => segmentsNetworkSegments.Segments);
    }

    [Output("segments")]
    public Output<string> Segments { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-consul/sdk/v3/go/consul"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		segmentsNetworkSegments, err := consul.GetNetworkSegments(ctx, nil, nil)
		if err != nil {
			return err
		}
		ctx.Export("segments", segmentsNetworkSegments.Segments)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_consul as consul

segments_network_segments = consul.get_network_segments()
pulumi.export("segments", segments_network_segments.segments)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as consul from "@pulumi/consul";

const segmentsNetworkSegments = consul.getNetworkSegments({});
export const segments = segmentsNetworkSegments.then(segmentsNetworkSegments => segmentsNetworkSegments.segments);
```


{{< /example >}}





{{% /examples %}}




## Using getNetworkSegments {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getNetworkSegments<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetNetworkSegmentsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetNetworkSegmentsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_network_segments(</span><span class="nx">datacenter</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">token</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetNetworkSegmentsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetNetworkSegments<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetNetworkSegmentsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetNetworkSegmentsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetNetworkSegments` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetNetworkSegments </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetNetworkSegmentsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetNetworkSegmentsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="datacenter_csharp">
<a href="#datacenter_csharp" style="color: inherit; text-decoration: inherit;">Datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The datacenter to use. This overrides the
agent's default datacenter and the datacenter in the provider setup.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="token_csharp">
<a href="#token_csharp" style="color: inherit; text-decoration: inherit;">Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ACL token to use. This overrides the
token that the agent provides by default.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="datacenter_go">
<a href="#datacenter_go" style="color: inherit; text-decoration: inherit;">Datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The datacenter to use. This overrides the
agent's default datacenter and the datacenter in the provider setup.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="token_go">
<a href="#token_go" style="color: inherit; text-decoration: inherit;">Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ACL token to use. This overrides the
token that the agent provides by default.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="datacenter_nodejs">
<a href="#datacenter_nodejs" style="color: inherit; text-decoration: inherit;">datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The datacenter to use. This overrides the
agent's default datacenter and the datacenter in the provider setup.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="token_nodejs">
<a href="#token_nodejs" style="color: inherit; text-decoration: inherit;">token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ACL token to use. This overrides the
token that the agent provides by default.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="datacenter_python">
<a href="#datacenter_python" style="color: inherit; text-decoration: inherit;">datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The datacenter to use. This overrides the
agent's default datacenter and the datacenter in the provider setup.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="token_python">
<a href="#token_python" style="color: inherit; text-decoration: inherit;">token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ACL token to use. This overrides the
token that the agent provides by default.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getNetworkSegments Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="datacenter_csharp">
<a href="#datacenter_csharp" style="color: inherit; text-decoration: inherit;">Datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The datacenter the segments are being read from.
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
        <span id="segments_csharp">
<a href="#segments_csharp" style="color: inherit; text-decoration: inherit;">Segments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The list of network segments.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="token_csharp">
<a href="#token_csharp" style="color: inherit; text-decoration: inherit;">Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="datacenter_go">
<a href="#datacenter_go" style="color: inherit; text-decoration: inherit;">Datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The datacenter the segments are being read from.
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
        <span id="segments_go">
<a href="#segments_go" style="color: inherit; text-decoration: inherit;">Segments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The list of network segments.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="token_go">
<a href="#token_go" style="color: inherit; text-decoration: inherit;">Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="datacenter_nodejs">
<a href="#datacenter_nodejs" style="color: inherit; text-decoration: inherit;">datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The datacenter the segments are being read from.
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
        <span id="segments_nodejs">
<a href="#segments_nodejs" style="color: inherit; text-decoration: inherit;">segments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The list of network segments.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="token_nodejs">
<a href="#token_nodejs" style="color: inherit; text-decoration: inherit;">token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="datacenter_python">
<a href="#datacenter_python" style="color: inherit; text-decoration: inherit;">datacenter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The datacenter the segments are being read from.
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
        <span id="segments_python">
<a href="#segments_python" style="color: inherit; text-decoration: inherit;">segments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The list of network segments.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="token_python">
<a href="#token_python" style="color: inherit; text-decoration: inherit;">token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-consul">https://github.com/pulumi/pulumi-consul</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`consul` Terraform Provider](https://github.com/hashicorp/terraform-provider-consul).{{% /md %}}</dd>
</dl>

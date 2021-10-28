
---
title: "getNodes"
title_tag: "cloudamqp.getNodes"
meta_desc: "Documentation for the cloudamqp.getNodes function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to retrieve information about the node(s) created by CloudAMQP instance.
## Argument reference

* `instance_id` - (Required) The CloudAMQP instance identifier.

## Attributes reference

All attributes reference are computed

* `id`    - The identifier for this resource.
* `nodes` - An array of node information. Each `nodes` block consists of the fields documented below.

***

The `nodes` block consist of

* `hostname`          - Hostname assigned to the node.
* `name`              - Name of the node.
* `running`           - Is the node running?
* `rabbitmq_version`  - Currently configured Rabbit MQ version on the node.
* `erlang_version`    - Currently used Erlanbg version on the node.
* `hipe`              - Enable or disable High-performance Erlang.
* `configured`        - Is the node configured?

## Dependency

This data source depends on CloudAMQP instance identifier, `cloudamqp_instance.instance.id`.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using CloudAmqp = Pulumi.CloudAmqp;

class MyStack : Stack
{
    public MyStack()
    {
        var nodes = Output.Create(CloudAmqp.GetNodes.InvokeAsync(new CloudAmqp.GetNodesArgs
        {
            InstanceId = cloudamqp_instance.Instance.Id,
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-cloudamqp/sdk/v3/go/cloudamqp"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := cloudamqp.GetNodes(ctx, &cloudamqp.GetNodesArgs{
			InstanceId: cloudamqp_instance.Instance.Id,
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
import pulumi_cloudamqp as cloudamqp

nodes = cloudamqp.get_nodes(instance_id=cloudamqp_instance["instance"]["id"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as cloudamqp from "@pulumi/cloudamqp";

const nodes = cloudamqp.getNodes({
    instanceId: cloudamqp_instance.instance.id,
});
```


{{< /example >}}





{{% /examples %}}




## Using getNodes {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getNodes<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetNodesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetNodesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_nodes(</span><span class="nx">instance_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetNodesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetNodes<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetNodesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetNodesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetNodes` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetNodes </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetNodesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetNodesArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instanceid_csharp">
<a href="#instanceid_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instanceid_go">
<a href="#instanceid_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instanceid_nodejs">
<a href="#instanceid_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instance_id_python">
<a href="#instance_id_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getNodes Result {#result}

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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instanceid_csharp">
<a href="#instanceid_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nodes_csharp">
<a href="#nodes_csharp" style="color: inherit; text-decoration: inherit;">Nodes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getnodesnode">List&lt;Pulumi.<wbr>Cloud<wbr>Amqp.<wbr>Outputs.<wbr>Get<wbr>Nodes<wbr>Node&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instanceid_go">
<a href="#instanceid_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nodes_go">
<a href="#nodes_go" style="color: inherit; text-decoration: inherit;">Nodes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getnodesnode">[]Get<wbr>Nodes<wbr>Node</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instanceid_nodejs">
<a href="#instanceid_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nodes_nodejs">
<a href="#nodes_nodejs" style="color: inherit; text-decoration: inherit;">nodes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getnodesnode">Get<wbr>Nodes<wbr>Node[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instance_id_python">
<a href="#instance_id_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nodes_python">
<a href="#nodes_python" style="color: inherit; text-decoration: inherit;">nodes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getnodesnode">Sequence[Get<wbr>Nodes<wbr>Node]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getnodesnode">Get<wbr>Nodes<wbr>Node</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configured_csharp">
<a href="#configured_csharp" style="color: inherit; text-decoration: inherit;">Configured</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="erlangversion_csharp">
<a href="#erlangversion_csharp" style="color: inherit; text-decoration: inherit;">Erlang<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hipe_csharp">
<a href="#hipe_csharp" style="color: inherit; text-decoration: inherit;">Hipe</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hostname_csharp">
<a href="#hostname_csharp" style="color: inherit; text-decoration: inherit;">Hostname</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rabbitmqversion_csharp">
<a href="#rabbitmqversion_csharp" style="color: inherit; text-decoration: inherit;">Rabbitmq<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="running_csharp">
<a href="#running_csharp" style="color: inherit; text-decoration: inherit;">Running</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configured_go">
<a href="#configured_go" style="color: inherit; text-decoration: inherit;">Configured</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="erlangversion_go">
<a href="#erlangversion_go" style="color: inherit; text-decoration: inherit;">Erlang<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hipe_go">
<a href="#hipe_go" style="color: inherit; text-decoration: inherit;">Hipe</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hostname_go">
<a href="#hostname_go" style="color: inherit; text-decoration: inherit;">Hostname</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rabbitmqversion_go">
<a href="#rabbitmqversion_go" style="color: inherit; text-decoration: inherit;">Rabbitmq<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="running_go">
<a href="#running_go" style="color: inherit; text-decoration: inherit;">Running</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configured_nodejs">
<a href="#configured_nodejs" style="color: inherit; text-decoration: inherit;">configured</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="erlangversion_nodejs">
<a href="#erlangversion_nodejs" style="color: inherit; text-decoration: inherit;">erlang<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hipe_nodejs">
<a href="#hipe_nodejs" style="color: inherit; text-decoration: inherit;">hipe</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hostname_nodejs">
<a href="#hostname_nodejs" style="color: inherit; text-decoration: inherit;">hostname</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rabbitmqversion_nodejs">
<a href="#rabbitmqversion_nodejs" style="color: inherit; text-decoration: inherit;">rabbitmq<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="running_nodejs">
<a href="#running_nodejs" style="color: inherit; text-decoration: inherit;">running</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configured_python">
<a href="#configured_python" style="color: inherit; text-decoration: inherit;">configured</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="erlang_version_python">
<a href="#erlang_version_python" style="color: inherit; text-decoration: inherit;">erlang_<wbr>version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hipe_python">
<a href="#hipe_python" style="color: inherit; text-decoration: inherit;">hipe</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="hostname_python">
<a href="#hostname_python" style="color: inherit; text-decoration: inherit;">hostname</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rabbitmq_version_python">
<a href="#rabbitmq_version_python" style="color: inherit; text-decoration: inherit;">rabbitmq_<wbr>version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="running_python">
<a href="#running_python" style="color: inherit; text-decoration: inherit;">running</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-cloudamqp">https://github.com/pulumi/pulumi-cloudamqp</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`cloudamqp` Terraform Provider](https://github.com/cloudamqp/terraform-provider-cloudamqp).{{% /md %}}</dd>
</dl>


---
title: "getBrokerNodes"
title_tag: "aws.msk.getBrokerNodes"
meta_desc: "Documentation for the aws.msk.getBrokerNodes function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Get information on an Amazon MSK Broker Nodes.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Aws.Msk.GetBrokerNodes.InvokeAsync(new Aws.Msk.GetBrokerNodesArgs
        {
            ClusterArn = aws_msk_cluster.Example.Arn,
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/msk"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := msk.GetBrokerNodes(ctx, &msk.GetBrokerNodesArgs{
			ClusterArn: aws_msk_cluster.Example.Arn,
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

example = aws.msk.get_broker_nodes(cluster_arn=aws_msk_cluster["example"]["arn"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = aws.msk.getBrokerNodes({
    clusterArn: aws_msk_cluster.example.arn,
});
```


{{< /example >}}





{{% /examples %}}




## Using getBrokerNodes {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getBrokerNodes<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetBrokerNodesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetBrokerNodesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_broker_nodes(</span><span class="nx">cluster_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetBrokerNodesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetBrokerNodes<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetBrokerNodesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetBrokerNodesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetBrokerNodes` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetBrokerNodes </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetBrokerNodesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetBrokerNodesArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clusterarn_csharp">
<a href="#clusterarn_csharp" style="color: inherit; text-decoration: inherit;">Cluster<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the cluster the nodes belong to.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clusterarn_go">
<a href="#clusterarn_go" style="color: inherit; text-decoration: inherit;">Cluster<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the cluster the nodes belong to.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clusterarn_nodejs">
<a href="#clusterarn_nodejs" style="color: inherit; text-decoration: inherit;">cluster<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the cluster the nodes belong to.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="cluster_arn_python">
<a href="#cluster_arn_python" style="color: inherit; text-decoration: inherit;">cluster_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the cluster the nodes belong to.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getBrokerNodes Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="clusterarn_csharp">
<a href="#clusterarn_csharp" style="color: inherit; text-decoration: inherit;">Cluster<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="nodeinfolists_csharp">
<a href="#nodeinfolists_csharp" style="color: inherit; text-decoration: inherit;">Node<wbr>Info<wbr>Lists</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getbrokernodesnodeinfolist">List&lt;Get<wbr>Broker<wbr>Nodes<wbr>Node<wbr>Info<wbr>List&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="clusterarn_go">
<a href="#clusterarn_go" style="color: inherit; text-decoration: inherit;">Cluster<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="nodeinfolists_go">
<a href="#nodeinfolists_go" style="color: inherit; text-decoration: inherit;">Node<wbr>Info<wbr>Lists</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getbrokernodesnodeinfolist">[]Get<wbr>Broker<wbr>Nodes<wbr>Node<wbr>Info<wbr>List</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="clusterarn_nodejs">
<a href="#clusterarn_nodejs" style="color: inherit; text-decoration: inherit;">cluster<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="nodeinfolists_nodejs">
<a href="#nodeinfolists_nodejs" style="color: inherit; text-decoration: inherit;">node<wbr>Info<wbr>Lists</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getbrokernodesnodeinfolist">Get<wbr>Broker<wbr>Nodes<wbr>Node<wbr>Info<wbr>List[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="cluster_arn_python">
<a href="#cluster_arn_python" style="color: inherit; text-decoration: inherit;">cluster_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="node_info_lists_python">
<a href="#node_info_lists_python" style="color: inherit; text-decoration: inherit;">node_<wbr>info_<wbr>lists</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getbrokernodesnodeinfolist">Sequence[Get<wbr>Broker<wbr>Nodes<wbr>Node<wbr>Info<wbr>List]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getbrokernodesnodeinfolist">Get<wbr>Broker<wbr>Nodes<wbr>Node<wbr>Info<wbr>List</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attachedeniid_csharp">
<a href="#attachedeniid_csharp" style="color: inherit; text-decoration: inherit;">Attached<wbr>Eni<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The attached elastic network interface of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="brokerid_csharp">
<a href="#brokerid_csharp" style="color: inherit; text-decoration: inherit;">Broker<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">double</span>
    </dt>
    <dd>{{% md %}}The ID of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="clientsubnet_csharp">
<a href="#clientsubnet_csharp" style="color: inherit; text-decoration: inherit;">Client<wbr>Subnet</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The client subnet to which this broker node belongs
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="clientvpcipaddress_csharp">
<a href="#clientvpcipaddress_csharp" style="color: inherit; text-decoration: inherit;">Client<wbr>Vpc<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The client virtual private cloud (VPC) IP address
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="endpoints_csharp">
<a href="#endpoints_csharp" style="color: inherit; text-decoration: inherit;">Endpoints</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Set of endpoints for accessing the broker. This does not include ports
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="nodearn_csharp">
<a href="#nodearn_csharp" style="color: inherit; text-decoration: inherit;">Node<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the node
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attachedeniid_go">
<a href="#attachedeniid_go" style="color: inherit; text-decoration: inherit;">Attached<wbr>Eni<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The attached elastic network interface of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="brokerid_go">
<a href="#brokerid_go" style="color: inherit; text-decoration: inherit;">Broker<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float64</span>
    </dt>
    <dd>{{% md %}}The ID of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="clientsubnet_go">
<a href="#clientsubnet_go" style="color: inherit; text-decoration: inherit;">Client<wbr>Subnet</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The client subnet to which this broker node belongs
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="clientvpcipaddress_go">
<a href="#clientvpcipaddress_go" style="color: inherit; text-decoration: inherit;">Client<wbr>Vpc<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The client virtual private cloud (VPC) IP address
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="endpoints_go">
<a href="#endpoints_go" style="color: inherit; text-decoration: inherit;">Endpoints</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Set of endpoints for accessing the broker. This does not include ports
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="nodearn_go">
<a href="#nodearn_go" style="color: inherit; text-decoration: inherit;">Node<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the node
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attachedeniid_nodejs">
<a href="#attachedeniid_nodejs" style="color: inherit; text-decoration: inherit;">attached<wbr>Eni<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The attached elastic network interface of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="brokerid_nodejs">
<a href="#brokerid_nodejs" style="color: inherit; text-decoration: inherit;">broker<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="clientsubnet_nodejs">
<a href="#clientsubnet_nodejs" style="color: inherit; text-decoration: inherit;">client<wbr>Subnet</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The client subnet to which this broker node belongs
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="clientvpcipaddress_nodejs">
<a href="#clientvpcipaddress_nodejs" style="color: inherit; text-decoration: inherit;">client<wbr>Vpc<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The client virtual private cloud (VPC) IP address
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="endpoints_nodejs">
<a href="#endpoints_nodejs" style="color: inherit; text-decoration: inherit;">endpoints</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Set of endpoints for accessing the broker. This does not include ports
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="nodearn_nodejs">
<a href="#nodearn_nodejs" style="color: inherit; text-decoration: inherit;">node<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the node
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attached_eni_id_python">
<a href="#attached_eni_id_python" style="color: inherit; text-decoration: inherit;">attached_<wbr>eni_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The attached elastic network interface of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="broker_id_python">
<a href="#broker_id_python" style="color: inherit; text-decoration: inherit;">broker_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The ID of the broker
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="client_subnet_python">
<a href="#client_subnet_python" style="color: inherit; text-decoration: inherit;">client_<wbr>subnet</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The client subnet to which this broker node belongs
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="client_vpc_ip_address_python">
<a href="#client_vpc_ip_address_python" style="color: inherit; text-decoration: inherit;">client_<wbr>vpc_<wbr>ip_<wbr>address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The client virtual private cloud (VPC) IP address
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="endpoints_python">
<a href="#endpoints_python" style="color: inherit; text-decoration: inherit;">endpoints</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Set of endpoints for accessing the broker. This does not include ports
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="node_arn_python">
<a href="#node_arn_python" style="color: inherit; text-decoration: inherit;">node_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the node
{{% /md %}}</dd></dl>
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

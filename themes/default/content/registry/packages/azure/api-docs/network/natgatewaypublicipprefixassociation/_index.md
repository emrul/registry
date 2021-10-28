
---
title: "NatGatewayPublicIpPrefixAssociation"
title_tag: "azure.network.NatGatewayPublicIpPrefixAssociation"
meta_desc: "Documentation for the azure.network.NatGatewayPublicIpPrefixAssociation resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Manages the association between a Nat Gateway and a Public IP Prefix.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Azure = Pulumi.Azure;

class MyStack : Stack
{
    public MyStack()
    {
        var exampleResourceGroup = new Azure.Core.ResourceGroup("exampleResourceGroup", new Azure.Core.ResourceGroupArgs
        {
            Location = "West Europe",
        });
        var examplePublicIpPrefix = new Azure.Network.PublicIpPrefix("examplePublicIpPrefix", new Azure.Network.PublicIpPrefixArgs
        {
            Location = exampleResourceGroup.Location,
            ResourceGroupName = exampleResourceGroup.Name,
            PrefixLength = 30,
            Zones = 
            {
                "1",
            },
        });
        var exampleNatGateway = new Azure.Network.NatGateway("exampleNatGateway", new Azure.Network.NatGatewayArgs
        {
            Location = exampleResourceGroup.Location,
            ResourceGroupName = exampleResourceGroup.Name,
            SkuName = "Standard",
        });
        var exampleNatGatewayPublicIpPrefixAssociation = new Azure.Network.NatGatewayPublicIpPrefixAssociation("exampleNatGatewayPublicIpPrefixAssociation", new Azure.Network.NatGatewayPublicIpPrefixAssociationArgs
        {
            NatGatewayId = exampleNatGateway.Id,
            PublicIpPrefixId = examplePublicIpPrefix.Id,
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-azure/sdk/v4/go/azure/core"
	"github.com/pulumi/pulumi-azure/sdk/v4/go/azure/network"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		exampleResourceGroup, err := core.NewResourceGroup(ctx, "exampleResourceGroup", &core.ResourceGroupArgs{
			Location: pulumi.String("West Europe"),
		})
		if err != nil {
			return err
		}
		examplePublicIpPrefix, err := network.NewPublicIpPrefix(ctx, "examplePublicIpPrefix", &network.PublicIpPrefixArgs{
			Location:          exampleResourceGroup.Location,
			ResourceGroupName: exampleResourceGroup.Name,
			PrefixLength:      pulumi.Int(30),
			Zones: pulumi.String{
				"1",
			},
		})
		if err != nil {
			return err
		}
		exampleNatGateway, err := network.NewNatGateway(ctx, "exampleNatGateway", &network.NatGatewayArgs{
			Location:          exampleResourceGroup.Location,
			ResourceGroupName: exampleResourceGroup.Name,
			SkuName:           pulumi.String("Standard"),
		})
		if err != nil {
			return err
		}
		_, err = network.NewNatGatewayPublicIpPrefixAssociation(ctx, "exampleNatGatewayPublicIpPrefixAssociation", &network.NatGatewayPublicIpPrefixAssociationArgs{
			NatGatewayId:     exampleNatGateway.ID(),
			PublicIpPrefixId: examplePublicIpPrefix.ID(),
		})
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
import pulumi_azure as azure

example_resource_group = azure.core.ResourceGroup("exampleResourceGroup", location="West Europe")
example_public_ip_prefix = azure.network.PublicIpPrefix("examplePublicIpPrefix",
    location=example_resource_group.location,
    resource_group_name=example_resource_group.name,
    prefix_length=30,
    zones=["1"])
example_nat_gateway = azure.network.NatGateway("exampleNatGateway",
    location=example_resource_group.location,
    resource_group_name=example_resource_group.name,
    sku_name="Standard")
example_nat_gateway_public_ip_prefix_association = azure.network.NatGatewayPublicIpPrefixAssociation("exampleNatGatewayPublicIpPrefixAssociation",
    nat_gateway_id=example_nat_gateway.id,
    public_ip_prefix_id=example_public_ip_prefix.id)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const exampleResourceGroup = new azure.core.ResourceGroup("exampleResourceGroup", {location: "West Europe"});
const examplePublicIpPrefix = new azure.network.PublicIpPrefix("examplePublicIpPrefix", {
    location: exampleResourceGroup.location,
    resourceGroupName: exampleResourceGroup.name,
    prefixLength: 30,
    zones: ["1"],
});
const exampleNatGateway = new azure.network.NatGateway("exampleNatGateway", {
    location: exampleResourceGroup.location,
    resourceGroupName: exampleResourceGroup.name,
    skuName: "Standard",
});
const exampleNatGatewayPublicIpPrefixAssociation = new azure.network.NatGatewayPublicIpPrefixAssociation("exampleNatGatewayPublicIpPrefixAssociation", {
    natGatewayId: exampleNatGateway.id,
    publicIpPrefixId: examplePublicIpPrefix.id,
});
```


{{< /example >}}





{{% /examples %}}




## Create a NatGatewayPublicIpPrefixAssociation Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">NatGatewayPublicIpPrefixAssociation</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">NatGatewayPublicIpPrefixAssociation</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                        <span class="nx">nat_gateway_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                        <span class="nx">public_ip_prefix_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">NatGatewayPublicIpPrefixAssociation</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                        <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span><span class="p">,</span>
                                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewNatGatewayPublicIpPrefixAssociation</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">NatGatewayPublicIpPrefixAssociation</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">NatGatewayPublicIpPrefixAssociation</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties"><dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>Context object for the current deployment.</dd><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NatGatewayPublicIpPrefixAssociationArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## NatGatewayPublicIpPrefixAssociation Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The NatGatewayPublicIpPrefixAssociation resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="natgatewayid_csharp">
<a href="#natgatewayid_csharp" style="color: inherit; text-decoration: inherit;">Nat<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="publicipprefixid_csharp">
<a href="#publicipprefixid_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="natgatewayid_go">
<a href="#natgatewayid_go" style="color: inherit; text-decoration: inherit;">Nat<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="publicipprefixid_go">
<a href="#publicipprefixid_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="natgatewayid_nodejs">
<a href="#natgatewayid_nodejs" style="color: inherit; text-decoration: inherit;">nat<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="publicipprefixid_nodejs">
<a href="#publicipprefixid_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Ip<wbr>Prefix<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="nat_gateway_id_python">
<a href="#nat_gateway_id_python" style="color: inherit; text-decoration: inherit;">nat_<wbr>gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="public_ip_prefix_id_python">
<a href="#public_ip_prefix_id_python" style="color: inherit; text-decoration: inherit;">public_<wbr>ip_<wbr>prefix_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the NatGatewayPublicIpPrefixAssociation resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing NatGatewayPublicIpPrefixAssociation Resource {#look-up}

Get an existing NatGatewayPublicIpPrefixAssociation resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">NatGatewayPublicIpPrefixAssociationState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">NatGatewayPublicIpPrefixAssociation</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">nat_gateway_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">public_ip_prefix_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> NatGatewayPublicIpPrefixAssociation</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetNatGatewayPublicIpPrefixAssociation<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">NatGatewayPublicIpPrefixAssociationState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">NatGatewayPublicIpPrefixAssociation</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">NatGatewayPublicIpPrefixAssociation</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">NatGatewayPublicIpPrefixAssociationState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_natgatewayid_csharp">
<a href="#state_natgatewayid_csharp" style="color: inherit; text-decoration: inherit;">Nat<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_publicipprefixid_csharp">
<a href="#state_publicipprefixid_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_natgatewayid_go">
<a href="#state_natgatewayid_go" style="color: inherit; text-decoration: inherit;">Nat<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_publicipprefixid_go">
<a href="#state_publicipprefixid_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_natgatewayid_nodejs">
<a href="#state_natgatewayid_nodejs" style="color: inherit; text-decoration: inherit;">nat<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_publicipprefixid_nodejs">
<a href="#state_publicipprefixid_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Ip<wbr>Prefix<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_nat_gateway_id_python">
<a href="#state_nat_gateway_id_python" style="color: inherit; text-decoration: inherit;">nat_<wbr>gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the Nat Gateway. Changing this forces a new resource to be created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_public_ip_prefix_id_python">
<a href="#state_public_ip_prefix_id_python" style="color: inherit; text-decoration: inherit;">public_<wbr>ip_<wbr>prefix_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the Public IP Prefix which this Nat Gateway which should be connected to. Changing this forces a new resource to be created.
{{% /md %}}</dd></dl>
{{% /choosable %}}





## Import


Associations between Nat Gateway and Public IP Prefixes can be imported using the `resource id`, e.g.

```sh
 $ pulumi import azure:network/natGatewayPublicIpPrefixAssociation:NatGatewayPublicIpPrefixAssociation example "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/group1/providers/Microsoft.Network/natGateways/gateway1|/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/mygroup1/providers/Microsoft.Network/publicIPPrefixes/myPublicIpPrefix1"
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure">https://github.com/pulumi/pulumi-azure</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`azurerm` Terraform Provider](https://github.com/hashicorp/terraform-provider-azurerm).{{% /md %}}</dd>
</dl>

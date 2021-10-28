
---
title: "InstanceAttachment"
title_tag: "alicloud.ots.InstanceAttachment"
meta_desc: "Documentation for the alicloud.ots.InstanceAttachment resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This resource will help you to bind a VPC to an OTS instance.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using AliCloud = Pulumi.AliCloud;

class MyStack : Stack
{
    public MyStack()
    {
        // Create an OTS instance
        var fooInstance = new AliCloud.Ots.Instance("fooInstance", new AliCloud.Ots.InstanceArgs
        {
            Description = "for table",
            AccessedBy = "Vpc",
            Tags = 
            {
                { "Created", "TF" },
                { "For", "Building table" },
            },
        });
        var fooZones = Output.Create(AliCloud.GetZones.InvokeAsync(new AliCloud.GetZonesArgs
        {
            AvailableResourceCreation = "VSwitch",
        }));
        var fooNetwork = new AliCloud.Vpc.Network("fooNetwork", new AliCloud.Vpc.NetworkArgs
        {
            CidrBlock = "172.16.0.0/16",
        });
        var fooSwitch = new AliCloud.Vpc.Switch("fooSwitch", new AliCloud.Vpc.SwitchArgs
        {
            VpcId = fooNetwork.Id,
            VswitchName = "for-ots-instance",
            CidrBlock = "172.16.1.0/24",
            ZoneId = fooZones.Apply(fooZones => fooZones.Zones[0].Id),
        });
        var fooInstanceAttachment = new AliCloud.Ots.InstanceAttachment("fooInstanceAttachment", new AliCloud.Ots.InstanceAttachmentArgs
        {
            InstanceName = fooInstance.Name,
            VpcName = "attachment1",
            VswitchId = fooSwitch.Id,
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud"
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/ots"
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/vpc"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		fooInstance, err := ots.NewInstance(ctx, "fooInstance", &ots.InstanceArgs{
			Description: pulumi.String("for table"),
			AccessedBy:  pulumi.String("Vpc"),
			Tags: pulumi.StringMap{
				"Created": pulumi.String("TF"),
				"For":     pulumi.String("Building table"),
			},
		})
		if err != nil {
			return err
		}
		opt0 := "VSwitch"
		fooZones, err := alicloud.GetZones(ctx, &alicloud.GetZonesArgs{
			AvailableResourceCreation: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		fooNetwork, err := vpc.NewNetwork(ctx, "fooNetwork", &vpc.NetworkArgs{
			CidrBlock: pulumi.String("172.16.0.0/16"),
		})
		if err != nil {
			return err
		}
		fooSwitch, err := vpc.NewSwitch(ctx, "fooSwitch", &vpc.SwitchArgs{
			VpcId:       fooNetwork.ID(),
			VswitchName: pulumi.String("for-ots-instance"),
			CidrBlock:   pulumi.String("172.16.1.0/24"),
			ZoneId:      pulumi.String(fooZones.Zones[0].Id),
		})
		if err != nil {
			return err
		}
		_, err = ots.NewInstanceAttachment(ctx, "fooInstanceAttachment", &ots.InstanceAttachmentArgs{
			InstanceName: fooInstance.Name,
			VpcName:      pulumi.String("attachment1"),
			VswitchId:    fooSwitch.ID(),
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
import pulumi_alicloud as alicloud

# Create an OTS instance
foo_instance = alicloud.ots.Instance("fooInstance",
    description="for table",
    accessed_by="Vpc",
    tags={
        "Created": "TF",
        "For": "Building table",
    })
foo_zones = alicloud.get_zones(available_resource_creation="VSwitch")
foo_network = alicloud.vpc.Network("fooNetwork", cidr_block="172.16.0.0/16")
foo_switch = alicloud.vpc.Switch("fooSwitch",
    vpc_id=foo_network.id,
    vswitch_name="for-ots-instance",
    cidr_block="172.16.1.0/24",
    zone_id=foo_zones.zones[0].id)
foo_instance_attachment = alicloud.ots.InstanceAttachment("fooInstanceAttachment",
    instance_name=foo_instance.name,
    vpc_name="attachment1",
    vswitch_id=foo_switch.id)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

// Create an OTS instance
const fooInstance = new alicloud.ots.Instance("fooInstance", {
    description: "for table",
    accessedBy: "Vpc",
    tags: {
        Created: "TF",
        For: "Building table",
    },
});
const fooZones = alicloud.getZones({
    availableResourceCreation: "VSwitch",
});
const fooNetwork = new alicloud.vpc.Network("fooNetwork", {cidrBlock: "172.16.0.0/16"});
const fooSwitch = new alicloud.vpc.Switch("fooSwitch", {
    vpcId: fooNetwork.id,
    vswitchName: "for-ots-instance",
    cidrBlock: "172.16.1.0/24",
    zoneId: fooZones.then(fooZones => fooZones.zones[0].id),
});
const fooInstanceAttachment = new alicloud.ots.InstanceAttachment("fooInstanceAttachment", {
    instanceName: fooInstance.name,
    vpcName: "attachment1",
    vswitchId: fooSwitch.id,
});
```


{{< /example >}}





{{% /examples %}}




## Create a InstanceAttachment Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">InstanceAttachment</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">InstanceAttachmentArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">InstanceAttachment</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                       <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                       <span class="nx">instance_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">vpc_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">vswitch_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">InstanceAttachment</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                       <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">InstanceAttachmentArgs</a></span><span class="p">,</span>
                       <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewInstanceAttachment</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">InstanceAttachmentArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">InstanceAttachment</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">InstanceAttachment</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">InstanceAttachmentArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">InstanceAttachmentArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InstanceAttachmentArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InstanceAttachmentArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InstanceAttachmentArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## InstanceAttachment Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The InstanceAttachment resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instancename_csharp">
<a href="#instancename_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vpcname_csharp">
<a href="#vpcname_csharp" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vswitchid_csharp">
<a href="#vswitchid_csharp" style="color: inherit; text-decoration: inherit;">Vswitch<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instancename_go">
<a href="#instancename_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vpcname_go">
<a href="#vpcname_go" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vswitchid_go">
<a href="#vswitchid_go" style="color: inherit; text-decoration: inherit;">Vswitch<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instancename_nodejs">
<a href="#instancename_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vpcname_nodejs">
<a href="#vpcname_nodejs" style="color: inherit; text-decoration: inherit;">vpc<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vswitchid_nodejs">
<a href="#vswitchid_nodejs" style="color: inherit; text-decoration: inherit;">vswitch<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instance_name_python">
<a href="#instance_name_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vpc_name_python">
<a href="#vpc_name_python" style="color: inherit; text-decoration: inherit;">vpc_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="vswitch_id_python">
<a href="#vswitch_id_python" style="color: inherit; text-decoration: inherit;">vswitch_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the InstanceAttachment resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vpcid_csharp">
<a href="#vpcid_csharp" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vpcid_go">
<a href="#vpcid_go" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vpcid_nodejs">
<a href="#vpcid_nodejs" style="color: inherit; text-decoration: inherit;">vpc<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vpc_id_python">
<a href="#vpc_id_python" style="color: inherit; text-decoration: inherit;">vpc_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing InstanceAttachment Resource {#look-up}

Get an existing InstanceAttachment resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">InstanceAttachmentState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">InstanceAttachment</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">instance_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">vpc_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">vpc_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">vswitch_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> InstanceAttachment</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetInstanceAttachment<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">InstanceAttachmentState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">InstanceAttachment</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">InstanceAttachment</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">InstanceAttachmentState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_instancename_csharp">
<a href="#state_instancename_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpcid_csharp">
<a href="#state_vpcid_csharp" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpcname_csharp">
<a href="#state_vpcname_csharp" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vswitchid_csharp">
<a href="#state_vswitchid_csharp" style="color: inherit; text-decoration: inherit;">Vswitch<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_instancename_go">
<a href="#state_instancename_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpcid_go">
<a href="#state_vpcid_go" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpcname_go">
<a href="#state_vpcname_go" style="color: inherit; text-decoration: inherit;">Vpc<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vswitchid_go">
<a href="#state_vswitchid_go" style="color: inherit; text-decoration: inherit;">Vswitch<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_instancename_nodejs">
<a href="#state_instancename_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpcid_nodejs">
<a href="#state_vpcid_nodejs" style="color: inherit; text-decoration: inherit;">vpc<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpcname_nodejs">
<a href="#state_vpcname_nodejs" style="color: inherit; text-decoration: inherit;">vpc<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vswitchid_nodejs">
<a href="#state_vswitchid_nodejs" style="color: inherit; text-decoration: inherit;">vswitch<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_instance_name_python">
<a href="#state_instance_name_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the OTS instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpc_id_python">
<a href="#state_vpc_id_python" style="color: inherit; text-decoration: inherit;">vpc_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vpc_name_python">
<a href="#state_vpc_name_python" style="color: inherit; text-decoration: inherit;">vpc_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of attaching VPC to instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vswitch_id_python">
<a href="#state_vswitch_id_python" style="color: inherit; text-decoration: inherit;">vswitch_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of attaching VSwitch to instance.
{{% /md %}}</dd></dl>
{{% /choosable %}}







<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`alicloud` Terraform Provider](https://github.com/aliyun/terraform-provider-alicloud).{{% /md %}}</dd>
</dl>

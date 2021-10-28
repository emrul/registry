
---
title: "getDedicatedHost"
title_tag: "aws.ec2.getDedicatedHost"
meta_desc: "Documentation for the aws.ec2.getDedicatedHost function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to get information about an EC2 Dedicated Host.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Filter Example


{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var test = Output.Create(Aws.Ec2.GetDedicatedHost.InvokeAsync(new Aws.Ec2.GetDedicatedHostArgs
        {
            Filters = 
            {
                new Aws.Ec2.Inputs.GetDedicatedHostFilterArgs
                {
                    Name = "instance-type",
                    Values = 
                    {
                        "c5.18xlarge",
                    },
                },
            },
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/ec2"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := ec2.LookupDedicatedHost(ctx, &ec2.LookupDedicatedHostArgs{
			Filters: []ec2.GetDedicatedHostFilter{
				ec2.GetDedicatedHostFilter{
					Name: "instance-type",
					Values: []string{
						"c5.18xlarge",
					},
				},
			},
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

test = aws.ec2.get_dedicated_host(filters=[aws.ec2.GetDedicatedHostFilterArgs(
    name="instance-type",
    values=["c5.18xlarge"],
)])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const test = pulumi.output(aws.ec2.getDedicatedHost({
    filters: [{
        name: "instance-type",
        values: ["c5.18xlarge"],
    }],
}));
```


{{< /example >}}





{{% /examples %}}




## Using getDedicatedHost {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getDedicatedHost<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetDedicatedHostArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetDedicatedHostResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_dedicated_host(</span><span class="nx">filters</span><span class="p">:</span> <span class="nx">Optional[Sequence[GetDedicatedHostFilter]]</span> = None<span class="p">,</span>
                       <span class="nx">host_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
                       <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetDedicatedHostResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupDedicatedHost<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupDedicatedHostArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupDedicatedHostResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupDedicatedHost` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetDedicatedHost </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetDedicatedHostResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetDedicatedHostArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">List&lt;Get<wbr>Dedicated<wbr>Host<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}Configuration block. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hostid_csharp">
<a href="#hostid_csharp" style="color: inherit; text-decoration: inherit;">Host<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Dedicated Host.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">[]Get<wbr>Dedicated<wbr>Host<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}Configuration block. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hostid_go">
<a href="#hostid_go" style="color: inherit; text-decoration: inherit;">Host<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Dedicated Host.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">Get<wbr>Dedicated<wbr>Host<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hostid_nodejs">
<a href="#hostid_nodejs" style="color: inherit; text-decoration: inherit;">host<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Dedicated Host.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">Sequence[Get<wbr>Dedicated<wbr>Host<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="host_id_python">
<a href="#host_id_python" style="color: inherit; text-decoration: inherit;">host_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the Dedicated Host.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getDedicatedHost Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_csharp">
<a href="#arn_csharp" style="color: inherit; text-decoration: inherit;">Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="autoplacement_csharp">
<a href="#autoplacement_csharp" style="color: inherit; text-decoration: inherit;">Auto<wbr>Placement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether auto-placement is on or off.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzone_csharp">
<a href="#availabilityzone_csharp" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Availability Zone of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cores_csharp">
<a href="#cores_csharp" style="color: inherit; text-decoration: inherit;">Cores</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of cores on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostid_csharp">
<a href="#hostid_csharp" style="color: inherit; text-decoration: inherit;">Host<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostrecovery_csharp">
<a href="#hostrecovery_csharp" style="color: inherit; text-decoration: inherit;">Host<wbr>Recovery</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Indicates whether host recovery is enabled or disabled for the Dedicated Host.
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
        <span id="instancefamily_csharp">
<a href="#instancefamily_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Family</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The instance family supported by the Dedicated Host. For example, "m5".
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instancetype_csharp">
<a href="#instancetype_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The instance type supported by the Dedicated Host. For example, "m5.large". If the host supports multiple instance types, no instanceType is returned.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_csharp">
<a href="#ownerid_csharp" style="color: inherit; text-decoration: inherit;">Owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS account that owns the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sockets_csharp">
<a href="#sockets_csharp" style="color: inherit; text-decoration: inherit;">Sockets</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of sockets on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="totalvcpus_csharp">
<a href="#totalvcpus_csharp" style="color: inherit; text-decoration: inherit;">Total<wbr>Vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The total number of vCPUs on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">List&lt;Get<wbr>Dedicated<wbr>Host<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_go">
<a href="#arn_go" style="color: inherit; text-decoration: inherit;">Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="autoplacement_go">
<a href="#autoplacement_go" style="color: inherit; text-decoration: inherit;">Auto<wbr>Placement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether auto-placement is on or off.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzone_go">
<a href="#availabilityzone_go" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Availability Zone of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cores_go">
<a href="#cores_go" style="color: inherit; text-decoration: inherit;">Cores</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of cores on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostid_go">
<a href="#hostid_go" style="color: inherit; text-decoration: inherit;">Host<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostrecovery_go">
<a href="#hostrecovery_go" style="color: inherit; text-decoration: inherit;">Host<wbr>Recovery</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Indicates whether host recovery is enabled or disabled for the Dedicated Host.
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
        <span id="instancefamily_go">
<a href="#instancefamily_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Family</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The instance family supported by the Dedicated Host. For example, "m5".
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instancetype_go">
<a href="#instancetype_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The instance type supported by the Dedicated Host. For example, "m5.large". If the host supports multiple instance types, no instanceType is returned.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_go">
<a href="#ownerid_go" style="color: inherit; text-decoration: inherit;">Owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS account that owns the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sockets_go">
<a href="#sockets_go" style="color: inherit; text-decoration: inherit;">Sockets</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of sockets on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="totalvcpus_go">
<a href="#totalvcpus_go" style="color: inherit; text-decoration: inherit;">Total<wbr>Vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The total number of vCPUs on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">[]Get<wbr>Dedicated<wbr>Host<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_nodejs">
<a href="#arn_nodejs" style="color: inherit; text-decoration: inherit;">arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="autoplacement_nodejs">
<a href="#autoplacement_nodejs" style="color: inherit; text-decoration: inherit;">auto<wbr>Placement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether auto-placement is on or off.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzone_nodejs">
<a href="#availabilityzone_nodejs" style="color: inherit; text-decoration: inherit;">availability<wbr>Zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Availability Zone of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cores_nodejs">
<a href="#cores_nodejs" style="color: inherit; text-decoration: inherit;">cores</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The number of cores on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostid_nodejs">
<a href="#hostid_nodejs" style="color: inherit; text-decoration: inherit;">host<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostrecovery_nodejs">
<a href="#hostrecovery_nodejs" style="color: inherit; text-decoration: inherit;">host<wbr>Recovery</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Indicates whether host recovery is enabled or disabled for the Dedicated Host.
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
        <span id="instancefamily_nodejs">
<a href="#instancefamily_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Family</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The instance family supported by the Dedicated Host. For example, "m5".
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instancetype_nodejs">
<a href="#instancetype_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The instance type supported by the Dedicated Host. For example, "m5.large". If the host supports multiple instance types, no instanceType is returned.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_nodejs">
<a href="#ownerid_nodejs" style="color: inherit; text-decoration: inherit;">owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS account that owns the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sockets_nodejs">
<a href="#sockets_nodejs" style="color: inherit; text-decoration: inherit;">sockets</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The number of sockets on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="totalvcpus_nodejs">
<a href="#totalvcpus_nodejs" style="color: inherit; text-decoration: inherit;">total<wbr>Vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The total number of vCPUs on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">Get<wbr>Dedicated<wbr>Host<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_python">
<a href="#arn_python" style="color: inherit; text-decoration: inherit;">arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="auto_placement_python">
<a href="#auto_placement_python" style="color: inherit; text-decoration: inherit;">auto_<wbr>placement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Whether auto-placement is on or off.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availability_zone_python">
<a href="#availability_zone_python" style="color: inherit; text-decoration: inherit;">availability_<wbr>zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Availability Zone of the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cores_python">
<a href="#cores_python" style="color: inherit; text-decoration: inherit;">cores</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of cores on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="host_id_python">
<a href="#host_id_python" style="color: inherit; text-decoration: inherit;">host_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="host_recovery_python">
<a href="#host_recovery_python" style="color: inherit; text-decoration: inherit;">host_<wbr>recovery</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Indicates whether host recovery is enabled or disabled for the Dedicated Host.
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
        <span id="instance_family_python">
<a href="#instance_family_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>family</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The instance family supported by the Dedicated Host. For example, "m5".
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="instance_type_python">
<a href="#instance_type_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The instance type supported by the Dedicated Host. For example, "m5.large". If the host supports multiple instance types, no instanceType is returned.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="owner_id_python">
<a href="#owner_id_python" style="color: inherit; text-decoration: inherit;">owner_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS account that owns the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sockets_python">
<a href="#sockets_python" style="color: inherit; text-decoration: inherit;">sockets</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of sockets on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="total_vcpus_python">
<a href="#total_vcpus_python" style="color: inherit; text-decoration: inherit;">total_<wbr>vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The total number of vCPUs on the Dedicated Host.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdedicatedhostfilter">Sequence[Get<wbr>Dedicated<wbr>Host<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getdedicatedhostfilter">Get<wbr>Dedicated<wbr>Host<wbr>Filter</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the field to filter by, as defined by [the underlying AWS API](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeHosts.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_csharp">
<a href="#values_csharp" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given field. A host will be selected if any one of the given values matches.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the field to filter by, as defined by [the underlying AWS API](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeHosts.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_go">
<a href="#values_go" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given field. A host will be selected if any one of the given values matches.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the field to filter by, as defined by [the underlying AWS API](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeHosts.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_nodejs">
<a href="#values_nodejs" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given field. A host will be selected if any one of the given values matches.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the field to filter by, as defined by [the underlying AWS API](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeHosts.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_python">
<a href="#values_python" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given field. A host will be selected if any one of the given values matches.
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

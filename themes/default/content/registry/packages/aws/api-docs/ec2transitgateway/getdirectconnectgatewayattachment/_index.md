
---
title: "getDirectConnectGatewayAttachment"
title_tag: "aws.ec2transitgateway.getDirectConnectGatewayAttachment"
meta_desc: "Documentation for the aws.ec2transitgateway.getDirectConnectGatewayAttachment function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Get information on an EC2 Transit Gateway's attachment to a Direct Connect Gateway.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### By Transit Gateway and Direct Connect Gateway Identifiers


{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Aws.Ec2TransitGateway.GetDirectConnectGatewayAttachment.InvokeAsync(new Aws.Ec2TransitGateway.GetDirectConnectGatewayAttachmentArgs
        {
            TransitGatewayId = aws_ec2_transit_gateway.Example.Id,
            DxGatewayId = aws_dx_gateway.Example.Id,
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/ec2transitgateway"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := aws_ec2_transit_gateway.Example.Id
		opt1 := aws_dx_gateway.Example.Id
		_, err := ec2transitgateway.GetDirectConnectGatewayAttachment(ctx, &ec2transitgateway.GetDirectConnectGatewayAttachmentArgs{
			TransitGatewayId: &opt0,
			DxGatewayId:      &opt1,
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

example = aws.ec2transitgateway.get_direct_connect_gateway_attachment(transit_gateway_id=aws_ec2_transit_gateway["example"]["id"],
    dx_gateway_id=aws_dx_gateway["example"]["id"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = aws.ec2transitgateway.getDirectConnectGatewayAttachment({
    transitGatewayId: aws_ec2_transit_gateway.example.id,
    dxGatewayId: aws_dx_gateway.example.id,
});
```


{{< /example >}}





{{% /examples %}}




## Using getDirectConnectGatewayAttachment {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getDirectConnectGatewayAttachment<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetDirectConnectGatewayAttachmentArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetDirectConnectGatewayAttachmentResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_direct_connect_gateway_attachment(</span><span class="nx">dx_gateway_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                          <span class="nx">filters</span><span class="p">:</span> <span class="nx">Optional[Sequence[GetDirectConnectGatewayAttachmentFilter]]</span> = None<span class="p">,</span>
                                          <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
                                          <span class="nx">transit_gateway_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetDirectConnectGatewayAttachmentResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetDirectConnectGatewayAttachment<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetDirectConnectGatewayAttachmentArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetDirectConnectGatewayAttachmentResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetDirectConnectGatewayAttachment` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetDirectConnectGatewayAttachment </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetDirectConnectGatewayAttachmentResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetDirectConnectGatewayAttachmentArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="dxgatewayid_csharp">
<a href="#dxgatewayid_csharp" style="color: inherit; text-decoration: inherit;">Dx<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Identifier of the Direct Connect Gateway.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">List&lt;Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) for filtering. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}A map of tags, each pair of which must exactly match a pair on the desired Transit Gateway Direct Connect Gateway Attachment.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="transitgatewayid_csharp">
<a href="#transitgatewayid_csharp" style="color: inherit; text-decoration: inherit;">Transit<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Identifier of the EC2 Transit Gateway.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="dxgatewayid_go">
<a href="#dxgatewayid_go" style="color: inherit; text-decoration: inherit;">Dx<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Identifier of the Direct Connect Gateway.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">[]Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) for filtering. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A map of tags, each pair of which must exactly match a pair on the desired Transit Gateway Direct Connect Gateway Attachment.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="transitgatewayid_go">
<a href="#transitgatewayid_go" style="color: inherit; text-decoration: inherit;">Transit<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Identifier of the EC2 Transit Gateway.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="dxgatewayid_nodejs">
<a href="#dxgatewayid_nodejs" style="color: inherit; text-decoration: inherit;">dx<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Identifier of the Direct Connect Gateway.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) for filtering. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A map of tags, each pair of which must exactly match a pair on the desired Transit Gateway Direct Connect Gateway Attachment.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="transitgatewayid_nodejs">
<a href="#transitgatewayid_nodejs" style="color: inherit; text-decoration: inherit;">transit<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Identifier of the EC2 Transit Gateway.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="dx_gateway_id_python">
<a href="#dx_gateway_id_python" style="color: inherit; text-decoration: inherit;">dx_<wbr>gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Identifier of the Direct Connect Gateway.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">Sequence[Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) for filtering. Detailed below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}A map of tags, each pair of which must exactly match a pair on the desired Transit Gateway Direct Connect Gateway Attachment.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="transit_gateway_id_python">
<a href="#transit_gateway_id_python" style="color: inherit; text-decoration: inherit;">transit_<wbr>gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Identifier of the EC2 Transit Gateway.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getDirectConnectGatewayAttachment Result {#result}

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
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Key-value tags for the EC2 Transit Gateway Attachment
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dxgatewayid_csharp">
<a href="#dxgatewayid_csharp" style="color: inherit; text-decoration: inherit;">Dx<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">List&lt;Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transitgatewayid_csharp">
<a href="#transitgatewayid_csharp" style="color: inherit; text-decoration: inherit;">Transit<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
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
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Key-value tags for the EC2 Transit Gateway Attachment
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dxgatewayid_go">
<a href="#dxgatewayid_go" style="color: inherit; text-decoration: inherit;">Dx<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">[]Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transitgatewayid_go">
<a href="#transitgatewayid_go" style="color: inherit; text-decoration: inherit;">Transit<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
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
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Key-value tags for the EC2 Transit Gateway Attachment
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dxgatewayid_nodejs">
<a href="#dxgatewayid_nodejs" style="color: inherit; text-decoration: inherit;">dx<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transitgatewayid_nodejs">
<a href="#transitgatewayid_nodejs" style="color: inherit; text-decoration: inherit;">transit<wbr>Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
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
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}Key-value tags for the EC2 Transit Gateway Attachment
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dx_gateway_id_python">
<a href="#dx_gateway_id_python" style="color: inherit; text-decoration: inherit;">dx_<wbr>gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdirectconnectgatewayattachmentfilter">Sequence[Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transit_gateway_id_python">
<a href="#transit_gateway_id_python" style="color: inherit; text-decoration: inherit;">transit_<wbr>gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getdirectconnectgatewayattachmentfilter">Get<wbr>Direct<wbr>Connect<wbr>Gateway<wbr>Attachment<wbr>Filter</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the filter field. Valid values can be found in the [EC2 DescribeTransitGatewayAttachments API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeTransitGatewayAttachments.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_csharp">
<a href="#values_csharp" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given filter field. Results will be selected if any given value matches.
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
    <dd>{{% md %}}The name of the filter field. Valid values can be found in the [EC2 DescribeTransitGatewayAttachments API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeTransitGatewayAttachments.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_go">
<a href="#values_go" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given filter field. Results will be selected if any given value matches.
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
    <dd>{{% md %}}The name of the filter field. Valid values can be found in the [EC2 DescribeTransitGatewayAttachments API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeTransitGatewayAttachments.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_nodejs">
<a href="#values_nodejs" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given filter field. Results will be selected if any given value matches.
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
    <dd>{{% md %}}The name of the filter field. Valid values can be found in the [EC2 DescribeTransitGatewayAttachments API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeTransitGatewayAttachments.html).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_python">
<a href="#values_python" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Set of values that are accepted for the given filter field. Results will be selected if any given value matches.
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

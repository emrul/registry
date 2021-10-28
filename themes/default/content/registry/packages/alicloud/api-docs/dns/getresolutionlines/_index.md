
---
title: "getResolutionLines"
title_tag: "alicloud.dns.getResolutionLines"
meta_desc: "Documentation for the alicloud.dns.getResolutionLines function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This data source provides a list of DNS Resolution Lines in an Alibaba Cloud account according to the specified filters.

> **NOTE:** Available in 1.60.0.


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
        var resolutionLinesDs = Output.Create(AliCloud.Dns.GetResolutionLines.InvokeAsync(new AliCloud.Dns.GetResolutionLinesArgs
        {
            LineCodes = 
            {
                "cn_unicom_shanxi",
            },
            OutputFile = "support_lines.txt",
        }));
        this.FirstLineCode = resolutionLinesDs.Apply(resolutionLinesDs => resolutionLinesDs.Lines[0].LineCode);
    }

    [Output("firstLineCode")]
    public Output<string> FirstLineCode { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/dns"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "support_lines.txt"
		resolutionLinesDs, err := dns.GetResolutionLines(ctx, &dns.GetResolutionLinesArgs{
			LineCodes: []string{
				"cn_unicom_shanxi",
			},
			OutputFile: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("firstLineCode", resolutionLinesDs.Lines[0].LineCode)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_alicloud as alicloud

resolution_lines_ds = alicloud.dns.get_resolution_lines(line_codes=["cn_unicom_shanxi"],
    output_file="support_lines.txt")
pulumi.export("firstLineCode", resolution_lines_ds.lines[0].line_code)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const resolutionLinesDs = pulumi.output(alicloud.dns.getResolutionLines({
    lineCodes: ["cn_unicom_shanxi"],
    outputFile: "support_lines.txt",
}, { async: true }));

export const firstLineCode = resolutionLinesDs.lines[0].lineCode;
```


{{< /example >}}





{{% /examples %}}




## Using getResolutionLines {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getResolutionLines<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetResolutionLinesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetResolutionLinesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_resolution_lines(</span><span class="nx">domain_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">lang</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">line_codes</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                         <span class="nx">line_display_names</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                         <span class="nx">line_names</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                         <span class="nx">output_file</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">user_client_ip</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetResolutionLinesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetResolutionLines<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetResolutionLinesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetResolutionLinesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetResolutionLines` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetResolutionLines </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetResolutionLinesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetResolutionLinesArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domainname_csharp">
<a href="#domainname_csharp" style="color: inherit; text-decoration: inherit;">Domain<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Domain Name.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lang_csharp">
<a href="#lang_csharp" style="color: inherit; text-decoration: inherit;">Lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}language.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linecodes_csharp">
<a href="#linecodes_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of lines codes.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linedisplaynames_csharp">
<a href="#linedisplaynames_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linenames_csharp">
<a href="#linenames_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="userclientip_csharp">
<a href="#userclientip_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Client<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ip of user client.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domainname_go">
<a href="#domainname_go" style="color: inherit; text-decoration: inherit;">Domain<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Domain Name.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lang_go">
<a href="#lang_go" style="color: inherit; text-decoration: inherit;">Lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}language.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linecodes_go">
<a href="#linecodes_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of lines codes.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linedisplaynames_go">
<a href="#linedisplaynames_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linenames_go">
<a href="#linenames_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="userclientip_go">
<a href="#userclientip_go" style="color: inherit; text-decoration: inherit;">User<wbr>Client<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ip of user client.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domainname_nodejs">
<a href="#domainname_nodejs" style="color: inherit; text-decoration: inherit;">domain<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Domain Name.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lang_nodejs">
<a href="#lang_nodejs" style="color: inherit; text-decoration: inherit;">lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}language.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linecodes_nodejs">
<a href="#linecodes_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of lines codes.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linedisplaynames_nodejs">
<a href="#linedisplaynames_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="linenames_nodejs">
<a href="#linenames_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="userclientip_nodejs">
<a href="#userclientip_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Client<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ip of user client.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domain_name_python">
<a href="#domain_name_python" style="color: inherit; text-decoration: inherit;">domain_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Domain Name.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lang_python">
<a href="#lang_python" style="color: inherit; text-decoration: inherit;">lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}language.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="line_codes_python">
<a href="#line_codes_python" style="color: inherit; text-decoration: inherit;">line_<wbr>codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of lines codes.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="line_display_names_python">
<a href="#line_display_names_python" style="color: inherit; text-decoration: inherit;">line_<wbr>display_<wbr>names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="line_names_python">
<a href="#line_names_python" style="color: inherit; text-decoration: inherit;">line_<wbr>names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="user_client_ip_python">
<a href="#user_client_ip_python" style="color: inherit; text-decoration: inherit;">user_<wbr>client_<wbr>ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ip of user client.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getResolutionLines Result {#result}

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
        <span id="linecodes_csharp">
<a href="#linecodes_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Line code.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="linedisplaynames_csharp">
<a href="#linedisplaynames_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lines_csharp">
<a href="#lines_csharp" style="color: inherit; text-decoration: inherit;">Lines</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getresolutionlinesline">List&lt;Pulumi.<wbr>Ali<wbr>Cloud.<wbr>Dns.<wbr>Outputs.<wbr>Get<wbr>Resolution<wbr>Lines<wbr>Line&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of cloud resolution line. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domainname_csharp">
<a href="#domainname_csharp" style="color: inherit; text-decoration: inherit;">Domain<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lang_csharp">
<a href="#lang_csharp" style="color: inherit; text-decoration: inherit;">Lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="linenames_csharp">
<a href="#linenames_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userclientip_csharp">
<a href="#userclientip_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Client<wbr>Ip</a>
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
        <span id="linecodes_go">
<a href="#linecodes_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Line code.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="linedisplaynames_go">
<a href="#linedisplaynames_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lines_go">
<a href="#lines_go" style="color: inherit; text-decoration: inherit;">Lines</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getresolutionlinesline">[]Get<wbr>Resolution<wbr>Lines<wbr>Line</a></span>
    </dt>
    <dd>{{% md %}}A list of cloud resolution line. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domainname_go">
<a href="#domainname_go" style="color: inherit; text-decoration: inherit;">Domain<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lang_go">
<a href="#lang_go" style="color: inherit; text-decoration: inherit;">Lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="linenames_go">
<a href="#linenames_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userclientip_go">
<a href="#userclientip_go" style="color: inherit; text-decoration: inherit;">User<wbr>Client<wbr>Ip</a>
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
        <span id="linecodes_nodejs">
<a href="#linecodes_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Line code.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="linedisplaynames_nodejs">
<a href="#linedisplaynames_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lines_nodejs">
<a href="#lines_nodejs" style="color: inherit; text-decoration: inherit;">lines</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getresolutionlinesline">Get<wbr>Resolution<wbr>Lines<wbr>Line[]</a></span>
    </dt>
    <dd>{{% md %}}A list of cloud resolution line. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domainname_nodejs">
<a href="#domainname_nodejs" style="color: inherit; text-decoration: inherit;">domain<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lang_nodejs">
<a href="#lang_nodejs" style="color: inherit; text-decoration: inherit;">lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="linenames_nodejs">
<a href="#linenames_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userclientip_nodejs">
<a href="#userclientip_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Client<wbr>Ip</a>
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
        <span id="line_codes_python">
<a href="#line_codes_python" style="color: inherit; text-decoration: inherit;">line_<wbr>codes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Line code.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="line_display_names_python">
<a href="#line_display_names_python" style="color: inherit; text-decoration: inherit;">line_<wbr>display_<wbr>names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of line display names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lines_python">
<a href="#lines_python" style="color: inherit; text-decoration: inherit;">lines</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getresolutionlinesline">Sequence[Get<wbr>Resolution<wbr>Lines<wbr>Line]</a></span>
    </dt>
    <dd>{{% md %}}A list of cloud resolution line. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domain_name_python">
<a href="#domain_name_python" style="color: inherit; text-decoration: inherit;">domain_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lang_python">
<a href="#lang_python" style="color: inherit; text-decoration: inherit;">lang</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="line_names_python">
<a href="#line_names_python" style="color: inherit; text-decoration: inherit;">line_<wbr>names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="user_client_ip_python">
<a href="#user_client_ip_python" style="color: inherit; text-decoration: inherit;">user_<wbr>client_<wbr>ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getresolutionlinesline">Get<wbr>Resolution<wbr>Lines<wbr>Line</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="linecode_csharp">
<a href="#linecode_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Code</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linedisplayname_csharp">
<a href="#linedisplayname_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Line display name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linename_csharp">
<a href="#linename_csharp" style="color: inherit; text-decoration: inherit;">Line<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Line name.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="linecode_go">
<a href="#linecode_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Code</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linedisplayname_go">
<a href="#linedisplayname_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Line display name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linename_go">
<a href="#linename_go" style="color: inherit; text-decoration: inherit;">Line<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Line name.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="linecode_nodejs">
<a href="#linecode_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Code</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linedisplayname_nodejs">
<a href="#linedisplayname_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Line display name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linename_nodejs">
<a href="#linename_nodejs" style="color: inherit; text-decoration: inherit;">line<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Line name.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="line_code_python">
<a href="#line_code_python" style="color: inherit; text-decoration: inherit;">line_<wbr>code</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="line_display_name_python">
<a href="#line_display_name_python" style="color: inherit; text-decoration: inherit;">line_<wbr>display_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Line display name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="line_name_python">
<a href="#line_name_python" style="color: inherit; text-decoration: inherit;">line_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Line name.
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

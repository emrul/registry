
---
title: "AppSecReputationProfile"
title_tag: "akamai.AppSecReputationProfile"
meta_desc: "Documentation for the akamai.AppSecReputationProfile resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use the `akamai.AppSecReputationProfile` resource to create or modify a reputation profile for a specific security configuration.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using System.IO;
using Pulumi;
using Akamai = Pulumi.Akamai;

class MyStack : Stack
{
    public MyStack()
    {
        var configuration = Output.Create(Akamai.GetAppSecConfiguration.InvokeAsync(new Akamai.GetAppSecConfigurationArgs
        {
            Name = @var.Security_configuration,
        }));
        // USE CASE: user wants to create a reputation profile for a given configuration and version, using a JSON definition
        var reputationProfile = new Akamai.AppSecReputationProfile("reputationProfile", new Akamai.AppSecReputationProfileArgs
        {
            ConfigId = configuration.Apply(configuration => configuration.ConfigId),
            ReputationProfile = File.ReadAllText($"{path.Module}/reputation_profile.json"),
        });
        this.ReputationProfileId = akamai_appsec_reputation_profile.Reputation_profile_id;
    }

    [Output("reputationProfileId")]
    public Output<string> ReputationProfileId { get; set; }
}
```


{{< /example >}}


{{< example go >}}

Coming soon!

{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_akamai as akamai

configuration = akamai.get_app_sec_configuration(name=var["security_configuration"])
# USE CASE: user wants to create a reputation profile for a given configuration and version, using a JSON definition
reputation_profile = akamai.AppSecReputationProfile("reputationProfile",
    config_id=configuration.config_id,
    reputation_profile=(lambda path: open(path).read())(f"{path['module']}/reputation_profile.json"))
pulumi.export("reputationProfileId", akamai_appsec_reputation_profile["reputation_profile_id"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as akamai from "@pulumi/akamai";
import * from "fs";

const configuration = akamai.getAppSecConfiguration({
    name: _var.security_configuration,
});
// USE CASE: user wants to create a reputation profile for a given configuration and version, using a JSON definition
const reputationProfile = new akamai.AppSecReputationProfile("reputationProfile", {
    configId: configuration.then(configuration => configuration.configId),
    reputationProfile: fs.readFileSync(`${path.module}/reputation_profile.json`),
});
export const reputationProfileId = akamai_appsec_reputation_profile.reputation_profile_id;
```


{{< /example >}}





{{% /examples %}}




## Create a AppSecReputationProfile Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">AppSecReputationProfile</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">AppSecReputationProfileArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">AppSecReputationProfile</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                            <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                            <span class="nx">config_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                            <span class="nx">reputation_profile</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">AppSecReputationProfile</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                            <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">AppSecReputationProfileArgs</a></span><span class="p">,</span>
                            <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewAppSecReputationProfile</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">AppSecReputationProfileArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">AppSecReputationProfile</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">AppSecReputationProfile</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">AppSecReputationProfileArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">AppSecReputationProfileArgs</a></span>
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
        <span class="property-type"><a href="#inputs">AppSecReputationProfileArgs</a></span>
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
        <span class="property-type"><a href="#inputs">AppSecReputationProfileArgs</a></span>
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
        <span class="property-type"><a href="#inputs">AppSecReputationProfileArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## AppSecReputationProfile Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The AppSecReputationProfile resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configid_csharp">
<a href="#configid_csharp" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="reputationprofile_csharp">
<a href="#reputationprofile_csharp" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configid_go">
<a href="#configid_go" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="reputationprofile_go">
<a href="#reputationprofile_go" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configid_nodejs">
<a href="#configid_nodejs" style="color: inherit; text-decoration: inherit;">config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="reputationprofile_nodejs">
<a href="#reputationprofile_nodejs" style="color: inherit; text-decoration: inherit;">reputation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="config_id_python">
<a href="#config_id_python" style="color: inherit; text-decoration: inherit;">config_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="reputation_profile_python">
<a href="#reputation_profile_python" style="color: inherit; text-decoration: inherit;">reputation_<wbr>profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the AppSecReputationProfile resource produces the following output properties:



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
        <span id="reputationprofileid_csharp">
<a href="#reputationprofileid_csharp" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
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
        <span id="reputationprofileid_go">
<a href="#reputationprofileid_go" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
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
        <span id="reputationprofileid_nodejs">
<a href="#reputationprofileid_nodejs" style="color: inherit; text-decoration: inherit;">reputation<wbr>Profile<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
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
        <span id="reputation_profile_id_python">
<a href="#reputation_profile_id_python" style="color: inherit; text-decoration: inherit;">reputation_<wbr>profile_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing AppSecReputationProfile Resource {#look-up}

Get an existing AppSecReputationProfile resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">AppSecReputationProfileState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">AppSecReputationProfile</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">config_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
        <span class="nx">reputation_profile</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">reputation_profile_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">) -&gt;</span> AppSecReputationProfile</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetAppSecReputationProfile<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">AppSecReputationProfileState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">AppSecReputationProfile</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">AppSecReputationProfile</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">AppSecReputationProfileState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_configid_csharp">
<a href="#state_configid_csharp" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputationprofile_csharp">
<a href="#state_reputationprofile_csharp" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputationprofileid_csharp">
<a href="#state_reputationprofileid_csharp" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_configid_go">
<a href="#state_configid_go" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputationprofile_go">
<a href="#state_reputationprofile_go" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputationprofileid_go">
<a href="#state_reputationprofileid_go" style="color: inherit; text-decoration: inherit;">Reputation<wbr>Profile<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_configid_nodejs">
<a href="#state_configid_nodejs" style="color: inherit; text-decoration: inherit;">config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputationprofile_nodejs">
<a href="#state_reputationprofile_nodejs" style="color: inherit; text-decoration: inherit;">reputation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputationprofileid_nodejs">
<a href="#state_reputationprofileid_nodejs" style="color: inherit; text-decoration: inherit;">reputation<wbr>Profile<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_config_id_python">
<a href="#state_config_id_python" style="color: inherit; text-decoration: inherit;">config_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputation_profile_python">
<a href="#state_reputation_profile_python" style="color: inherit; text-decoration: inherit;">reputation_<wbr>profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a file containing a JSON-formatted definition of the reputation profile. ([format](https://developer.akamai.com/api/cloud_security/application_security/v1.html#postreputationprofiles))
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_reputation_profile_id_python">
<a href="#state_reputation_profile_id_python" style="color: inherit; text-decoration: inherit;">reputation_<wbr>profile_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the newly created or modified reputation profile.
{{% /md %}}</dd></dl>
{{% /choosable %}}







<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-akamai">https://github.com/pulumi/pulumi-akamai</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`akamai` Terraform Provider](https://github.com/akamai/terraform-provider-akamai).{{% /md %}}</dd>
</dl>

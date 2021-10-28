
---
title: "ClusterCapacityProviderAssociations"
title_tag: "aws-native.ecs.ClusterCapacityProviderAssociations"
meta_desc: "Documentation for the aws-native.ecs.ClusterCapacityProviderAssociations resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Associate a set of ECS Capacity Providers with a specified ECS Cluster


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var config = new Config();
        var clusterName = config.Require("clusterName");
        var clusterCPAssociation = new AwsNative.ECS.ClusterCapacityProviderAssociations("clusterCPAssociation", new AwsNative.ECS.ClusterCapacityProviderAssociationsArgs
        {
            Cluster = clusterName,
            CapacityProviders = 
            {
                "FARGATE",
                "FARGATE_SPOT",
            },
            DefaultCapacityProviderStrategy = 
            {
                new AwsNative.ECS.Inputs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs
                {
                    Base = 2,
                    Weight = 1,
                    CapacityProvider = "FARGATE",
                },
                new AwsNative.ECS.Inputs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs
                {
                    Base = 0,
                    Weight = 1,
                    CapacityProvider = "FARGATE_SPOT",
                },
            },
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/ecs"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi/config"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		cfg := config.New(ctx, "")
		clusterName := cfg.Require("clusterName")
		_, err := ecs.NewClusterCapacityProviderAssociations(ctx, "clusterCPAssociation", &ecs.ClusterCapacityProviderAssociationsArgs{
			Cluster: pulumi.String(clusterName),
			CapacityProviders: pulumi.StringArray{
				pulumi.String("FARGATE"),
				pulumi.String("FARGATE_SPOT"),
			},
			DefaultCapacityProviderStrategy: ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArray{
				&ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs{
					Base:             pulumi.Int(2),
					Weight:           pulumi.Int(1),
					CapacityProvider: pulumi.String("FARGATE"),
				},
				&ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs{
					Base:             pulumi.Int(0),
					Weight:           pulumi.Int(1),
					CapacityProvider: pulumi.String("FARGATE_SPOT"),
				},
			},
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
import pulumi_aws_native as aws_native

config = pulumi.Config()
cluster_name = config.require("clusterName")
cluster_cpassociation = aws_native.ecs.ClusterCapacityProviderAssociations("clusterCPAssociation",
    cluster=cluster_name,
    capacity_providers=[
        "FARGATE",
        "FARGATE_SPOT",
    ],
    default_capacity_provider_strategy=[
        aws_native.ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs(
            base=2,
            weight=1,
            capacity_provider="FARGATE",
        ),
        aws_native.ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs(
            base=0,
            weight=1,
            capacity_provider="FARGATE_SPOT",
        ),
    ])

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const config = new pulumi.Config();
const clusterName = config.require("clusterName");
const clusterCPAssociation = new aws_native.ecs.ClusterCapacityProviderAssociations("clusterCPAssociation", {
    cluster: clusterName,
    capacityProviders: [
        "FARGATE",
        "FARGATE_SPOT",
    ],
    defaultCapacityProviderStrategy: [
        {
            base: 2,
            weight: 1,
            capacityProvider: "FARGATE",
        },
        {
            base: 0,
            weight: 1,
            capacityProvider: "FARGATE_SPOT",
        },
    ],
});

```


{{< /example >}}




### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var config = new Config();
        var clusterName = config.Require("clusterName");
        var clusterCPAssociation = new AwsNative.ECS.ClusterCapacityProviderAssociations("clusterCPAssociation", new AwsNative.ECS.ClusterCapacityProviderAssociationsArgs
        {
            Cluster = clusterName,
            CapacityProviders = 
            {
                "FARGATE",
                "FARGATE_SPOT",
            },
            DefaultCapacityProviderStrategy = 
            {
                new AwsNative.ECS.Inputs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs
                {
                    Base = 2,
                    Weight = 1,
                    CapacityProvider = "FARGATE",
                },
                new AwsNative.ECS.Inputs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs
                {
                    Base = 0,
                    Weight = 1,
                    CapacityProvider = "FARGATE_SPOT",
                },
            },
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/ecs"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi/config"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		cfg := config.New(ctx, "")
		clusterName := cfg.Require("clusterName")
		_, err := ecs.NewClusterCapacityProviderAssociations(ctx, "clusterCPAssociation", &ecs.ClusterCapacityProviderAssociationsArgs{
			Cluster: pulumi.String(clusterName),
			CapacityProviders: pulumi.StringArray{
				pulumi.String("FARGATE"),
				pulumi.String("FARGATE_SPOT"),
			},
			DefaultCapacityProviderStrategy: ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArray{
				&ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs{
					Base:             pulumi.Int(2),
					Weight:           pulumi.Int(1),
					CapacityProvider: pulumi.String("FARGATE"),
				},
				&ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs{
					Base:             pulumi.Int(0),
					Weight:           pulumi.Int(1),
					CapacityProvider: pulumi.String("FARGATE_SPOT"),
				},
			},
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
import pulumi_aws_native as aws_native

config = pulumi.Config()
cluster_name = config.require("clusterName")
cluster_cpassociation = aws_native.ecs.ClusterCapacityProviderAssociations("clusterCPAssociation",
    cluster=cluster_name,
    capacity_providers=[
        "FARGATE",
        "FARGATE_SPOT",
    ],
    default_capacity_provider_strategy=[
        aws_native.ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs(
            base=2,
            weight=1,
            capacity_provider="FARGATE",
        ),
        aws_native.ecs.ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs(
            base=0,
            weight=1,
            capacity_provider="FARGATE_SPOT",
        ),
    ])

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const config = new pulumi.Config();
const clusterName = config.require("clusterName");
const clusterCPAssociation = new aws_native.ecs.ClusterCapacityProviderAssociations("clusterCPAssociation", {
    cluster: clusterName,
    capacityProviders: [
        "FARGATE",
        "FARGATE_SPOT",
    ],
    defaultCapacityProviderStrategy: [
        {
            base: 2,
            weight: 1,
            capacityProvider: "FARGATE",
        },
        {
            base: 0,
            weight: 1,
            capacityProvider: "FARGATE_SPOT",
        },
    ],
});

```


{{< /example >}}





{{% /examples %}}




## Create a ClusterCapacityProviderAssociations Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">ClusterCapacityProviderAssociations</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">ClusterCapacityProviderAssociations</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                        <span class="nx">capacity_providers</span><span class="p">:</span> <span class="nx">Optional[Sequence[Union[ClusterCapacityProviderAssociationsCapacityProvider, str]]]</span> = None<span class="p">,</span>
                                        <span class="nx">cluster</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                        <span class="nx">default_capacity_provider_strategy</span><span class="p">:</span> <span class="nx">Optional[Sequence[ClusterCapacityProviderAssociationsCapacityProviderStrategyArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">ClusterCapacityProviderAssociations</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                        <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span><span class="p">,</span>
                                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewClusterCapacityProviderAssociations</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">ClusterCapacityProviderAssociations</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">ClusterCapacityProviderAssociations</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ClusterCapacityProviderAssociationsArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## ClusterCapacityProviderAssociations Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The ClusterCapacityProviderAssociations resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacityproviders_csharp">
<a href="#capacityproviders_csharp" style="color: inherit; text-decoration: inherit;">Capacity<wbr>Providers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;Union&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>ECS.<wbr>Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider, string&gt;&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="cluster_csharp">
<a href="#cluster_csharp" style="color: inherit; text-decoration: inherit;">Cluster</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="defaultcapacityproviderstrategy_csharp">
<a href="#defaultcapacityproviderstrategy_csharp" style="color: inherit; text-decoration: inherit;">Default<wbr>Capacity<wbr>Provider<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityproviderstrategy">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>ECS.<wbr>Inputs.<wbr>Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider<wbr>Strategy<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacityproviders_go">
<a href="#capacityproviders_go" style="color: inherit; text-decoration: inherit;">Capacity<wbr>Providers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="cluster_go">
<a href="#cluster_go" style="color: inherit; text-decoration: inherit;">Cluster</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="defaultcapacityproviderstrategy_go">
<a href="#defaultcapacityproviderstrategy_go" style="color: inherit; text-decoration: inherit;">Default<wbr>Capacity<wbr>Provider<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityproviderstrategy">[]Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider<wbr>Strategy<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacityproviders_nodejs">
<a href="#capacityproviders_nodejs" style="color: inherit; text-decoration: inherit;">capacity<wbr>Providers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">(Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider | string)[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="cluster_nodejs">
<a href="#cluster_nodejs" style="color: inherit; text-decoration: inherit;">cluster</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="defaultcapacityproviderstrategy_nodejs">
<a href="#defaultcapacityproviderstrategy_nodejs" style="color: inherit; text-decoration: inherit;">default<wbr>Capacity<wbr>Provider<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityproviderstrategy">Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider<wbr>Strategy<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacity_providers_python">
<a href="#capacity_providers_python" style="color: inherit; text-decoration: inherit;">capacity_<wbr>providers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[Union[Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider, str]]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="cluster_python">
<a href="#cluster_python" style="color: inherit; text-decoration: inherit;">cluster</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="default_capacity_provider_strategy_python">
<a href="#default_capacity_provider_strategy_python" style="color: inherit; text-decoration: inherit;">default_<wbr>capacity_<wbr>provider_<wbr>strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityproviderstrategy">Sequence[Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider<wbr>Strategy<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the ClusterCapacityProviderAssociations resource produces the following output properties:



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







## Supporting Types



<h4 id="clustercapacityproviderassociationscapacityprovider">Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Fargate</dt>
    <dd>FARGATE</dd><dt>Fargate<wbr>Spot</dt>
    <dd>FARGATE_SPOT</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider<wbr>Fargate</dt>
    <dd>FARGATE</dd><dt>Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider<wbr>Fargate<wbr>Spot</dt>
    <dd>FARGATE_SPOT</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Fargate</dt>
    <dd>FARGATE</dd><dt>Fargate<wbr>Spot</dt>
    <dd>FARGATE_SPOT</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>FARGATE</dt>
    <dd>FARGATE</dd><dt>FARGATE_SPOT</dt>
    <dd>FARGATE_SPOT</dd></dl>
{{% /choosable %}}

<h4 id="clustercapacityproviderassociationscapacityproviderstrategy">Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider<wbr>Strategy</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacityprovider_csharp">
<a href="#capacityprovider_csharp" style="color: inherit; text-decoration: inherit;">Capacity<wbr>Provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityprovider">Pulumi.<wbr>Aws<wbr>Native.<wbr>ECS.<wbr>Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider</a> | string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="base_csharp">
<a href="#base_csharp" style="color: inherit; text-decoration: inherit;">Base</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="weight_csharp">
<a href="#weight_csharp" style="color: inherit; text-decoration: inherit;">Weight</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacityprovider_go">
<a href="#capacityprovider_go" style="color: inherit; text-decoration: inherit;">Capacity<wbr>Provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityprovider">Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider</a> | string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="base_go">
<a href="#base_go" style="color: inherit; text-decoration: inherit;">Base</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="weight_go">
<a href="#weight_go" style="color: inherit; text-decoration: inherit;">Weight</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacityprovider_nodejs">
<a href="#capacityprovider_nodejs" style="color: inherit; text-decoration: inherit;">capacity<wbr>Provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityprovider">Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider</a> | string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="base_nodejs">
<a href="#base_nodejs" style="color: inherit; text-decoration: inherit;">base</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="weight_nodejs">
<a href="#weight_nodejs" style="color: inherit; text-decoration: inherit;">weight</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="capacity_provider_python">
<a href="#capacity_provider_python" style="color: inherit; text-decoration: inherit;">capacity_<wbr>provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustercapacityproviderassociationscapacityprovider">Cluster<wbr>Capacity<wbr>Provider<wbr>Associations<wbr>Capacity<wbr>Provider</a> | str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="base_python">
<a href="#base_python" style="color: inherit; text-decoration: inherit;">base</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="weight_python">
<a href="#weight_python" style="color: inherit; text-decoration: inherit;">weight</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

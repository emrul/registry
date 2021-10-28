
---
title: "Subscription"
title_tag: "google-native.pubsublite/v1.Subscription"
meta_desc: "Documentation for the google-native.pubsublite/v1.Subscription resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Creates a new subscription.




## Create a Subscription Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Subscription</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">SubscriptionArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Subscription</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                 <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                 <span class="nx">delivery_config</span><span class="p">:</span> <span class="nx">Optional[DeliveryConfigArgs]</span> = None<span class="p">,</span>
                 <span class="nx">location</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                 <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                 <span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                 <span class="nx">skip_backlog</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                 <span class="nx">subscription_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                 <span class="nx">topic</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Subscription</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                 <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">SubscriptionArgs</a></span><span class="p">,</span>
                 <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewSubscription</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">SubscriptionArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Subscription</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Subscription</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">SubscriptionArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">SubscriptionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">SubscriptionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">SubscriptionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">SubscriptionArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Subscription Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Subscription resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="subscriptionid_csharp">
<a href="#subscriptionid_csharp" style="color: inherit; text-decoration: inherit;">Subscription<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliveryconfig_csharp">
<a href="#deliveryconfig_csharp" style="color: inherit; text-decoration: inherit;">Delivery<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfig">Pulumi.<wbr>Google<wbr>Native.<wbr>Pubsublite.<wbr>V1.<wbr>Inputs.<wbr>Delivery<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings for this subscription's message delivery.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subscription. Structured like: projects/{project_number}/locations/{location}/subscriptions/{subscription_id}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="skipbacklog_csharp">
<a href="#skipbacklog_csharp" style="color: inherit; text-decoration: inherit;">Skip<wbr>Backlog</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topic_csharp">
<a href="#topic_csharp" style="color: inherit; text-decoration: inherit;">Topic</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the topic this subscription is attached to. Structured like: projects/{project_number}/locations/{location}/topics/{topic_id}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="subscriptionid_go">
<a href="#subscriptionid_go" style="color: inherit; text-decoration: inherit;">Subscription<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliveryconfig_go">
<a href="#deliveryconfig_go" style="color: inherit; text-decoration: inherit;">Delivery<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfig">Delivery<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings for this subscription's message delivery.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subscription. Structured like: projects/{project_number}/locations/{location}/subscriptions/{subscription_id}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="skipbacklog_go">
<a href="#skipbacklog_go" style="color: inherit; text-decoration: inherit;">Skip<wbr>Backlog</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topic_go">
<a href="#topic_go" style="color: inherit; text-decoration: inherit;">Topic</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the topic this subscription is attached to. Structured like: projects/{project_number}/locations/{location}/topics/{topic_id}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="subscriptionid_nodejs">
<a href="#subscriptionid_nodejs" style="color: inherit; text-decoration: inherit;">subscription<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliveryconfig_nodejs">
<a href="#deliveryconfig_nodejs" style="color: inherit; text-decoration: inherit;">delivery<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfig">Delivery<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings for this subscription's message delivery.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subscription. Structured like: projects/{project_number}/locations/{location}/subscriptions/{subscription_id}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="skipbacklog_nodejs">
<a href="#skipbacklog_nodejs" style="color: inherit; text-decoration: inherit;">skip<wbr>Backlog</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topic_nodejs">
<a href="#topic_nodejs" style="color: inherit; text-decoration: inherit;">topic</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the topic this subscription is attached to. Structured like: projects/{project_number}/locations/{location}/topics/{topic_id}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="subscription_id_python">
<a href="#subscription_id_python" style="color: inherit; text-decoration: inherit;">subscription_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="delivery_config_python">
<a href="#delivery_config_python" style="color: inherit; text-decoration: inherit;">delivery_<wbr>config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfig">Delivery<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings for this subscription's message delivery.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the subscription. Structured like: projects/{project_number}/locations/{location}/subscriptions/{subscription_id}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="skip_backlog_python">
<a href="#skip_backlog_python" style="color: inherit; text-decoration: inherit;">skip_<wbr>backlog</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topic_python">
<a href="#topic_python" style="color: inherit; text-decoration: inherit;">topic</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the topic this subscription is attached to. Structured like: projects/{project_number}/locations/{location}/topics/{topic_id}{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Subscription resource produces the following output properties:



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



<h4 id="deliveryconfig">Delivery<wbr>Config</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="deliveryrequirement_csharp">
<a href="#deliveryrequirement_csharp" style="color: inherit; text-decoration: inherit;">Delivery<wbr>Requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfigdeliveryrequirement">Pulumi.<wbr>Google<wbr>Native.<wbr>Pubsublite.<wbr>V1.<wbr>Delivery<wbr>Config<wbr>Delivery<wbr>Requirement</a></span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="deliveryrequirement_go">
<a href="#deliveryrequirement_go" style="color: inherit; text-decoration: inherit;">Delivery<wbr>Requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfigdeliveryrequirement">Delivery<wbr>Config<wbr>Delivery<wbr>Requirement</a></span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="deliveryrequirement_nodejs">
<a href="#deliveryrequirement_nodejs" style="color: inherit; text-decoration: inherit;">delivery<wbr>Requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfigdeliveryrequirement">Delivery<wbr>Config<wbr>Delivery<wbr>Requirement</a></span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="delivery_requirement_python">
<a href="#delivery_requirement_python" style="color: inherit; text-decoration: inherit;">delivery_<wbr>requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliveryconfigdeliveryrequirement">Delivery<wbr>Config<wbr>Delivery<wbr>Requirement</a></span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="deliveryconfigdeliveryrequirement">Delivery<wbr>Config<wbr>Delivery<wbr>Requirement</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Delivery<wbr>Requirement<wbr>Unspecified</dt>
    <dd>DELIVERY_REQUIREMENT_UNSPECIFIED{{% md %}}Default value. This value is unused.{{% /md %}}</dd><dt>Deliver<wbr>Immediately</dt>
    <dd>DELIVER_IMMEDIATELY{{% md %}}The server does not wait for a published message to be successfully written to storage before delivering it to subscribers.{{% /md %}}</dd><dt>Deliver<wbr>After<wbr>Stored</dt>
    <dd>DELIVER_AFTER_STORED{{% md %}}The server will not deliver a published message to subscribers until the message has been successfully written to storage. This will result in higher end-to-end latency, but consistent delivery.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Delivery<wbr>Config<wbr>Delivery<wbr>Requirement<wbr>Delivery<wbr>Requirement<wbr>Unspecified</dt>
    <dd>DELIVERY_REQUIREMENT_UNSPECIFIED{{% md %}}Default value. This value is unused.{{% /md %}}</dd><dt>Delivery<wbr>Config<wbr>Delivery<wbr>Requirement<wbr>Deliver<wbr>Immediately</dt>
    <dd>DELIVER_IMMEDIATELY{{% md %}}The server does not wait for a published message to be successfully written to storage before delivering it to subscribers.{{% /md %}}</dd><dt>Delivery<wbr>Config<wbr>Delivery<wbr>Requirement<wbr>Deliver<wbr>After<wbr>Stored</dt>
    <dd>DELIVER_AFTER_STORED{{% md %}}The server will not deliver a published message to subscribers until the message has been successfully written to storage. This will result in higher end-to-end latency, but consistent delivery.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Delivery<wbr>Requirement<wbr>Unspecified</dt>
    <dd>DELIVERY_REQUIREMENT_UNSPECIFIED{{% md %}}Default value. This value is unused.{{% /md %}}</dd><dt>Deliver<wbr>Immediately</dt>
    <dd>DELIVER_IMMEDIATELY{{% md %}}The server does not wait for a published message to be successfully written to storage before delivering it to subscribers.{{% /md %}}</dd><dt>Deliver<wbr>After<wbr>Stored</dt>
    <dd>DELIVER_AFTER_STORED{{% md %}}The server will not deliver a published message to subscribers until the message has been successfully written to storage. This will result in higher end-to-end latency, but consistent delivery.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>DELIVERY_REQUIREMENT_UNSPECIFIED</dt>
    <dd>DELIVERY_REQUIREMENT_UNSPECIFIED{{% md %}}Default value. This value is unused.{{% /md %}}</dd><dt>DELIVER_IMMEDIATELY</dt>
    <dd>DELIVER_IMMEDIATELY{{% md %}}The server does not wait for a published message to be successfully written to storage before delivering it to subscribers.{{% /md %}}</dd><dt>DELIVER_AFTER_STORED</dt>
    <dd>DELIVER_AFTER_STORED{{% md %}}The server will not deliver a published message to subscribers until the message has been successfully written to storage. This will result in higher end-to-end latency, but consistent delivery.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="deliveryconfigresponse">Delivery<wbr>Config<wbr>Response</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="deliveryrequirement_csharp">
<a href="#deliveryrequirement_csharp" style="color: inherit; text-decoration: inherit;">Delivery<wbr>Requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="deliveryrequirement_go">
<a href="#deliveryrequirement_go" style="color: inherit; text-decoration: inherit;">Delivery<wbr>Requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="deliveryrequirement_nodejs">
<a href="#deliveryrequirement_nodejs" style="color: inherit; text-decoration: inherit;">delivery<wbr>Requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="delivery_requirement_python">
<a href="#delivery_requirement_python" style="color: inherit; text-decoration: inherit;">delivery_<wbr>requirement</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The DeliveryRequirement for this subscription.{{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

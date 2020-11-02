---
title: "Module s3control"
title_tag: "Module s3control | Package @pulumi/aws | Node.js SDK"
linktitle: "s3control"
meta_desc: "Explore members of the s3control module in the @pulumi/aws package."
git_sha: "bfaec7a64d2c6e86da46a4f8671eca2edc1002a8"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "aws" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#Bucket"><span class="symbol resource"></span>Bucket</a></li>
    <li><a href="#BucketLifecycleConfiguration"><span class="symbol resource"></span>BucketLifecycleConfiguration</a></li>
    <li><a href="#BucketPolicy"><span class="symbol resource"></span>BucketPolicy</a></li>
</ul>


<h3>Others</h3>
<ul class="api">
    <li><a href="#BucketArgs"><span class="symbol api"></span>BucketArgs</a></li>
    <li><a href="#BucketLifecycleConfigurationArgs"><span class="symbol api"></span>BucketLifecycleConfigurationArgs</a></li>
    <li><a href="#BucketLifecycleConfigurationState"><span class="symbol api"></span>BucketLifecycleConfigurationState</a></li>
    <li><a href="#BucketPolicyArgs"><span class="symbol api"></span>BucketPolicyArgs</a></li>
    <li><a href="#BucketPolicyState"><span class="symbol api"></span>BucketPolicyState</a></li>
    <li><a href="#BucketState"><span class="symbol api"></span>BucketState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Bucket" data-link-title="Bucket">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L24">
        Resource <strong>Bucket</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Bucket</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Provides a resource to manage an S3 Control Bucket.

> This functionality is for managing [S3 on Outposts](https://docs.aws.amazon.com/AmazonS3/latest/dev/S3onOutposts.html). To manage S3 Buckets in an AWS Partition, see the [`aws.s3.Bucket` resource](https://www.terraform.io/docs/providers/aws/r/s3_bucket.html).

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = new aws.s3control.Bucket("example", {
    bucket: "example",
    outpostId: data.aws_outposts_outpost.example.id,
});
```

<h4 class="pdoc-member-header" id="Bucket-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L75"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Bucket(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#BucketArgs'>BucketArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Bucket resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Bucket-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L34">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#BucketState'>BucketState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Bucket'>Bucket</a></code></pre>


Get an existing Bucket resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Bucket-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L24">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Bucket-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L45">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Bucket</code></pre>


Returns true if the given object is an instance of Bucket.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Bucket-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L55">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>arn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="Bucket-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L59">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>bucket: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the bucket.

<h4 class="pdoc-member-header" id="Bucket-creationDate">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L63">property <b>creationDate</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>creationDate: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

UTC creation date in [RFC3339 format](https://tools.ietf.org/html/rfc3339#section-5.8).

<h4 class="pdoc-member-header" id="Bucket-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L24">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Bucket-outpostId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L67">property <b>outpostId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>outpostId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Identifier of the Outpost to contain this bucket.

<h4 class="pdoc-member-header" id="Bucket-publicAccessBlockEnabled">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L71">property <b>publicAccessBlockEnabled</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>publicAccessBlockEnabled: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>&gt;;</code></pre>

Boolean whether Public Access Block is enabled.

<h4 class="pdoc-member-header" id="Bucket-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L75">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>tags: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>} | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Key-value map of resource tags.

<h4 class="pdoc-member-header" id="Bucket-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L24">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-module-header" id="BucketLifecycleConfiguration" data-link-title="BucketLifecycleConfiguration">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L10">
        Resource <strong>BucketLifecycleConfiguration</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>BucketLifecycleConfiguration</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>
<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L45"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> BucketLifecycleConfiguration(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#BucketLifecycleConfigurationArgs'>BucketLifecycleConfigurationArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a BucketLifecycleConfiguration resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L20">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#BucketLifecycleConfigurationState'>BucketLifecycleConfigurationState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#BucketLifecycleConfiguration'>BucketLifecycleConfiguration</a></code></pre>


Get an existing BucketLifecycleConfiguration resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L10">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L31">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is BucketLifecycleConfiguration</code></pre>


Returns true if the given object is an instance of BucketLifecycleConfiguration.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L41">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>bucket: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L10">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-rules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L45">property <b>rules</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>rules: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/aws/types/output/#BucketLifecycleConfigurationRule'>BucketLifecycleConfigurationRule</a>[]&gt;;</code></pre>

Configuration block(s) containing lifecycle rules for the bucket.

<h4 class="pdoc-member-header" id="BucketLifecycleConfiguration-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L10">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-module-header" id="BucketPolicy" data-link-title="BucketPolicy">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L36">
        Resource <strong>BucketPolicy</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>BucketPolicy</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Provides a resource to manage an S3 Control Bucket Policy.

> This functionality is for managing [S3 on Outposts](https://docs.aws.amazon.com/AmazonS3/latest/dev/S3onOutposts.html). To manage S3 Bucket Policies in an AWS Partition, see the [`aws.s3.BucketPolicy` resource](https://www.terraform.io/docs/providers/aws/r/s3_bucket_policy.html).

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = new aws.s3control.BucketPolicy("example", {
    bucket: aws_s3control_bucket.example.arn,
    policy: JSON.stringify({
        Id: "testBucketPolicy",
        Statement: [{
            Action: "s3-outposts:PutBucketLifecycleConfiguration",
            Effect: "Deny",
            Principal: {
                AWS: "*",
            },
            Resource: aws_s3control_bucket.example.arn,
            Sid: "statement1",
        }],
        Version: "2012-10-17",
    }),
});
```

<h4 class="pdoc-member-header" id="BucketPolicy-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L68"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> BucketPolicy(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#BucketPolicyArgs'>BucketPolicyArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a BucketPolicy resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="BucketPolicy-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L46">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#BucketPolicyState'>BucketPolicyState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#BucketPolicy'>BucketPolicy</a></code></pre>


Get an existing BucketPolicy resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="BucketPolicy-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L36">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="BucketPolicy-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L57">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is BucketPolicy</code></pre>


Returns true if the given object is an instance of BucketPolicy.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="BucketPolicy-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L67">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>bucket: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="BucketPolicy-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L36">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="BucketPolicy-policy">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L68">property <b>policy</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>policy: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>
<h4 class="pdoc-member-header" id="BucketPolicy-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L36">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.



<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="BucketArgs" data-link-title="BucketArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L154">
        interface <strong>BucketArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BucketArgs</span></code></pre>

The set of arguments for constructing a Bucket resource.

<h4 class="pdoc-member-header" id="BucketArgs-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L158">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>bucket: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the bucket.

<h4 class="pdoc-member-header" id="BucketArgs-outpostId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L162">property <b>outpostId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>outpostId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Identifier of the Outpost to contain this bucket.

<h4 class="pdoc-member-header" id="BucketArgs-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L166">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

Key-value map of resource tags.

<h3 class="pdoc-module-header" id="BucketLifecycleConfigurationArgs" data-link-title="BucketLifecycleConfigurationArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L100">
        interface <strong>BucketLifecycleConfigurationArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BucketLifecycleConfigurationArgs</span></code></pre>

The set of arguments for constructing a BucketLifecycleConfiguration resource.

<h4 class="pdoc-member-header" id="BucketLifecycleConfigurationArgs-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L104">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>bucket: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="BucketLifecycleConfigurationArgs-rules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L108">property <b>rules</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>rules: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/aws/types/input/#BucketLifecycleConfigurationRule'>BucketLifecycleConfigurationRule</a>&gt;[]&gt;;</code></pre>

Configuration block(s) containing lifecycle rules for the bucket.

<h3 class="pdoc-module-header" id="BucketLifecycleConfigurationState" data-link-title="BucketLifecycleConfigurationState">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L86">
        interface <strong>BucketLifecycleConfigurationState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BucketLifecycleConfigurationState</span></code></pre>

Input properties used for looking up and filtering BucketLifecycleConfiguration resources.

<h4 class="pdoc-member-header" id="BucketLifecycleConfigurationState-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L90">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>bucket?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="BucketLifecycleConfigurationState-rules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketLifecycleConfiguration.ts#L94">property <b>rules</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>rules?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/aws/types/input/#BucketLifecycleConfigurationRule'>BucketLifecycleConfigurationRule</a>&gt;[]&gt;;</code></pre>

Configuration block(s) containing lifecycle rules for the bucket.

<h3 class="pdoc-module-header" id="BucketPolicyArgs" data-link-title="BucketPolicyArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L120">
        interface <strong>BucketPolicyArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BucketPolicyArgs</span></code></pre>

The set of arguments for constructing a BucketPolicy resource.

<h4 class="pdoc-member-header" id="BucketPolicyArgs-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L124">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>bucket: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="BucketPolicyArgs-policy">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L125">property <b>policy</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>policy: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>
<h3 class="pdoc-module-header" id="BucketPolicyState" data-link-title="BucketPolicyState">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L109">
        interface <strong>BucketPolicyState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BucketPolicyState</span></code></pre>

Input properties used for looking up and filtering BucketPolicy resources.

<h4 class="pdoc-member-header" id="BucketPolicyState-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L113">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>bucket?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="BucketPolicyState-policy">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucketPolicy.ts#L114">property <b>policy</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>policy?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>
<h3 class="pdoc-module-header" id="BucketState" data-link-title="BucketState">
    <a href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L124">
        interface <strong>BucketState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BucketState</span></code></pre>

Input properties used for looking up and filtering Bucket resources.

<h4 class="pdoc-member-header" id="BucketState-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L128">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Amazon Resource Name (ARN) of the bucket.

<h4 class="pdoc-member-header" id="BucketState-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L132">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>bucket?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the bucket.

<h4 class="pdoc-member-header" id="BucketState-creationDate">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L136">property <b>creationDate</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>creationDate?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

UTC creation date in [RFC3339 format](https://tools.ietf.org/html/rfc3339#section-5.8).

<h4 class="pdoc-member-header" id="BucketState-outpostId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L140">property <b>outpostId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>outpostId?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Identifier of the Outpost to contain this bucket.

<h4 class="pdoc-member-header" id="BucketState-publicAccessBlockEnabled">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L144">property <b>publicAccessBlockEnabled</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>publicAccessBlockEnabled?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>&gt;;</code></pre>

Boolean whether Public Access Block is enabled.

<h4 class="pdoc-member-header" id="BucketState-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/bfaec7a64d2c6e86da46a4f8671eca2edc1002a8/sdk/nodejs/s3control/bucket.ts#L148">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

Key-value map of resource tags.

---
title: "Module build"
title_tag: "Module build | Package @pulumi/azuredevops | Node.js SDK"
linktitle: "build"
meta_desc: "Explore members of the build module in the @pulumi/azuredevops package."
git_sha: "5a2704baa4eadd2446006775047639ffb3cd5575"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "azuredevops" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#BuildDefinition"><span class="symbol resource"></span>BuildDefinition</a></li>
</ul>


<h3>Others</h3>
<ul class="api">
    <li><a href="#BuildDefinitionArgs"><span class="symbol api"></span>BuildDefinitionArgs</a></li>
    <li><a href="#BuildDefinitionState"><span class="symbol api"></span>BuildDefinitionState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="BuildDefinition" data-link-title="BuildDefinition">
    <a href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L104">
        Resource <strong>BuildDefinition</strong>
    </a>
</h3>

<div class="note note-deprecated">
<i class="fas fa-exclamation-triangle pr-2"></i><strong>DEPRECATED</strong>
azuredevops.build.BuildDefinition has been deprecated in favor of azuredevops.BuildDefinition
</div>
<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>BuildDefinition</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Manages a Build Definition within Azure DevOps.

#### Example Usage
##### Tfs
```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azuredevops from "@pulumi/azuredevops";

const project = new azuredevops.Project("project", {
    visibility: "private",
    versionControl: "Git",
    workItemTemplate: "Agile",
});
const repository = new azuredevops.Git("repository", {
    projectId: project.id,
    initialization: {
        initType: "Clean",
    },
});
const vars = new azuredevops.VariableGroup("vars", {
    projectId: project.id,
    description: "Managed by Terraform",
    allowAccess: true,
    variables: [{
        name: "FOO",
        value: "BAR",
    }],
});
const build = new azuredevops.BuildDefinition("build", {
    projectId: project.id,
    path: "\\ExampleFolder",
    ciTrigger: {
        useYaml: true,
    },
    repository: {
        repoType: "TfsGit",
        repoId: repository.id,
        branchName: repository.defaultBranch,
        ymlPath: "azure-pipelines.yml",
    },
    variableGroups: [vars.id],
    variables: [
        {
            name: "PipelineVariable",
            value: "Go Microsoft!",
        },
        {
            name: "PipelineSecret",
            secretValue: "ZGV2cw",
            isSecret: true,
        },
    ],
});
```
##### GitHub Enterprise
```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azuredevops from "@pulumi/azuredevops";

const sampleDotnetcoreAppRelease = new azuredevops.BuildDefinition("sampleDotnetcoreAppRelease", {
    projectId: azuredevops_project.project.id,
    path: "\\ExampleFolder",
    ciTrigger: {
        useYaml: true,
    },
    repository: {
        repoType: "GitHubEnterprise",
        repoId: "<GitHub Org>/<Repo Name>",
        githubEnterpriseUrl: "https://github.company.com",
        branchName: "master",
        ymlPath: "azure-pipelines.yml",
        serviceConnectionId: "...",
    },
});
```
#### Relevant Links

- [Azure DevOps Service REST API 5.1 - Build Definitions](https://docs.microsoft.com/en-us/rest/api/azure/devops/build/definitions?view=azure-devops-rest-5.1)

#### Import

Azure DevOps Build Definitions can be imported using the project name/definitions Id or by the project Guid/definitions Id, e.g.

```sh
 $ pulumi import azuredevops:Build/buildDefinition:BuildDefinition build "Test Project"/10
```

 or

```sh
 $ pulumi import azuredevops:Build/buildDefinition:BuildDefinition build 00000000-0000-0000-0000-000000000000/0
```

<h4 class="pdoc-member-header" id="BuildDefinition-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L172"> <b>constructor</b></a>
</h4>

<div class="note note-deprecated">
<i class="fas fa-exclamation-triangle pr-2"></i><strong>DEPRECATED</strong>
azuredevops.build.BuildDefinition has been deprecated in favor of azuredevops.BuildDefinition
</div>

<div class="note note-deprecated">
<i class="fas fa-exclamation-triangle pr-2"></i><strong>DEPRECATED</strong>
azuredevops.build.BuildDefinition has been deprecated in favor of azuredevops.BuildDefinition
</div>
<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> BuildDefinition(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#BuildDefinitionArgs'>BuildDefinitionArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>

<h4 class="pdoc-member-header" id="BuildDefinition-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L114">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#BuildDefinitionState'>BuildDefinitionState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#BuildDefinition'>BuildDefinition</a></code></pre>


Get an existing BuildDefinition resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="BuildDefinition-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L104">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="BuildDefinition-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L126">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is BuildDefinition</code></pre>


Returns true if the given object is an instance of BuildDefinition.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="BuildDefinition-agentPoolName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L136">property <b>agentPoolName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>agentPoolName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

The agent pool that should execute the build.

<h4 class="pdoc-member-header" id="BuildDefinition-ciTrigger">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L140">property <b>ciTrigger</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>ciTrigger: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/output/#BuildDefinitionCiTrigger'>BuildDefinitionCiTrigger</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Continuous Integration trigger.

<h4 class="pdoc-member-header" id="BuildDefinition-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L104">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="BuildDefinition-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L144">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the build definition.

<h4 class="pdoc-member-header" id="BuildDefinition-path">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L148">property <b>path</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>path: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

The folder path of the build definition.

<h4 class="pdoc-member-header" id="BuildDefinition-projectId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L152">property <b>projectId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>projectId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The project ID or project name.

<h4 class="pdoc-member-header" id="BuildDefinition-pullRequestTrigger">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L156">property <b>pullRequestTrigger</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>pullRequestTrigger: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/output/#BuildDefinitionPullRequestTrigger'>BuildDefinitionPullRequestTrigger</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Pull Request Integration Integration trigger.

<h4 class="pdoc-member-header" id="BuildDefinition-repository">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L160">property <b>repository</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>repository: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/output/#BuildDefinitionRepository'>BuildDefinitionRepository</a>&gt;;</code></pre>

A `repository` block as documented below.

<h4 class="pdoc-member-header" id="BuildDefinition-revision">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L164">property <b>revision</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>revision: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The revision of the build definition

<h4 class="pdoc-member-header" id="BuildDefinition-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L104">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h4 class="pdoc-member-header" id="BuildDefinition-variableGroups">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L168">property <b>variableGroups</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>variableGroups: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

A list of variable group IDs (integers) to link to the build definition.

<h4 class="pdoc-member-header" id="BuildDefinition-variables">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L172">property <b>variables</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>variables: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/output/#BuildDefinitionVariable'>BuildDefinitionVariable</a>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

A list of `variable` blocks, as documented below.



<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="BuildDefinitionArgs" data-link-title="BuildDefinitionArgs">
    <a href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L278">
        interface <strong>BuildDefinitionArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BuildDefinitionArgs</span></code></pre>

The set of arguments for constructing a BuildDefinition resource.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-agentPoolName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L282">property <b>agentPoolName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>agentPoolName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The agent pool that should execute the build.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-ciTrigger">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L286">property <b>ciTrigger</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ciTrigger?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionCiTrigger'>BuildDefinitionCiTrigger</a>&gt;;</code></pre>

Continuous Integration trigger.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L290">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the build definition.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-path">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L294">property <b>path</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>path?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The folder path of the build definition.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-projectId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L298">property <b>projectId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>projectId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The project ID or project name.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-pullRequestTrigger">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L302">property <b>pullRequestTrigger</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>pullRequestTrigger?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionPullRequestTrigger'>BuildDefinitionPullRequestTrigger</a>&gt;;</code></pre>

Pull Request Integration Integration trigger.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-repository">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L306">property <b>repository</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>repository: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionRepository'>BuildDefinitionRepository</a>&gt;;</code></pre>

A `repository` block as documented below.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-variableGroups">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L310">property <b>variableGroups</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>variableGroups?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;[]&gt;;</code></pre>

A list of variable group IDs (integers) to link to the build definition.

<h4 class="pdoc-member-header" id="BuildDefinitionArgs-variables">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L314">property <b>variables</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>variables?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionVariable'>BuildDefinitionVariable</a>&gt;[]&gt;;</code></pre>

A list of `variable` blocks, as documented below.

<h3 class="pdoc-module-header" id="BuildDefinitionState" data-link-title="BuildDefinitionState">
    <a href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L232">
        interface <strong>BuildDefinitionState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>BuildDefinitionState</span></code></pre>

Input properties used for looking up and filtering BuildDefinition resources.

<h4 class="pdoc-member-header" id="BuildDefinitionState-agentPoolName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L236">property <b>agentPoolName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>agentPoolName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The agent pool that should execute the build.

<h4 class="pdoc-member-header" id="BuildDefinitionState-ciTrigger">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L240">property <b>ciTrigger</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ciTrigger?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionCiTrigger'>BuildDefinitionCiTrigger</a>&gt;;</code></pre>

Continuous Integration trigger.

<h4 class="pdoc-member-header" id="BuildDefinitionState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L244">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the build definition.

<h4 class="pdoc-member-header" id="BuildDefinitionState-path">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L248">property <b>path</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>path?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The folder path of the build definition.

<h4 class="pdoc-member-header" id="BuildDefinitionState-projectId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L252">property <b>projectId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>projectId?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The project ID or project name.

<h4 class="pdoc-member-header" id="BuildDefinitionState-pullRequestTrigger">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L256">property <b>pullRequestTrigger</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>pullRequestTrigger?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionPullRequestTrigger'>BuildDefinitionPullRequestTrigger</a>&gt;;</code></pre>

Pull Request Integration Integration trigger.

<h4 class="pdoc-member-header" id="BuildDefinitionState-repository">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L260">property <b>repository</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>repository?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionRepository'>BuildDefinitionRepository</a>&gt;;</code></pre>

A `repository` block as documented below.

<h4 class="pdoc-member-header" id="BuildDefinitionState-revision">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L264">property <b>revision</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>revision?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The revision of the build definition

<h4 class="pdoc-member-header" id="BuildDefinitionState-variableGroups">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L268">property <b>variableGroups</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>variableGroups?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;[]&gt;;</code></pre>

A list of variable group IDs (integers) to link to the build definition.

<h4 class="pdoc-member-header" id="BuildDefinitionState-variables">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azuredevops/blob/5a2704baa4eadd2446006775047639ffb3cd5575/sdk/nodejs/build/buildDefinition.ts#L272">property <b>variables</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>variables?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/azuredevops/types/input/#BuildDefinitionVariable'>BuildDefinitionVariable</a>&gt;[]&gt;;</code></pre>

A list of `variable` blocks, as documented below.

# @batch

<!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! Instead, edit the notebook w/the location & name as this file. -->

The `@batch` decorator sends a step for execution on the [AWS Batch](https://aws.amazon.com/batch/) compute layer. For more information, see [Executing Tasks Remotely](/scaling/remote-tasks/introduction).


<DocSection type="decorator" name="batch" module="metaflow" show_import="True" heading_level="3" link="https://github.com/Netflix/metaflow/tree/master/metaflow/plugins/aws/batch/batch_decorator.py#L30">
<SigArgSection>
<SigArg name="..." />
</SigArgSection>
<Description summary="Specifies that this step should execute on [AWS Batch](https://aws.amazon.com/batch/)." />
<ParamSection name="Parameters">
	<Parameter name="cpu" type="int" desc="Number of CPUs required for this step. Defaults to 1. If `@resources` is\nalso present, the maximum value from all decorators is used." />
	<Parameter name="gpu" type="int" desc="Number of GPUs required for this step. Defaults to 0. If `@resources` is\nalso present, the maximum value from all decorators is used." />
	<Parameter name="memory" type="int" desc="Memory size (in MB) required for this step. Defaults to 4096 (4GB). If\n`@resources` is also present, the maximum value from all decorators is\nused." />
	<Parameter name="image" type="string" desc="Docker image to use when launching on AWS Batch. If not specified, a\ndefault Docker image mapping to the current version of Python is used." />
	<Parameter name="queue" type="string" desc="AWS Batch Job Queue to submit the job to. Defaults to the one\nspecified by the configuration variable `METAFLOW_BATCH_JOB_QUEUE`." />
	<Parameter name="iam_role" type="string" desc="AWS IAM role that AWS Batch container uses to access AWS cloud resources.\nDefaults to the one specified by the configuration variable `METAFLOW_ECS_S3_ACCESS_IAM_ROLE`." />
	<Parameter name="execution_role" type="string" desc="AWS IAM role that AWS Batch can use [to trigger AWS Fargate tasks]\n(https://docs.aws.amazon.com/batch/latest/userguide/execution-IAM-role.html).\nDefaults to the one determined by the configuration variable\n`METAFLOW_ECS_FARGATE_EXECUTION_ROLE`." />
	<Parameter name="shared_memory" type="int" desc="The value for the size (in MiB) of the /dev/shm volume for this step.\nThis parameter maps to the `--shm-size` option in Docker." />
	<Parameter name="max_swap" type="int" desc="The total amount of swap memory (in MiB) a container can use for this\nstep. This parameter is translated to the `--memory-swap` option in\nDocker where the value is the sum of the container memory plus the\n`max_swap` value." />
	<Parameter name="swappiness" type="int" desc="This allows you to tune memory swappiness behavior for this step.\nA swappiness value of 0 causes swapping not to happen unless absolutely\nnecessary. A swappiness value of 100 causes pages to be swapped very\naggressively. Accepted values are whole numbers between 0 and 100." />
</ParamSection>
</DocSection>

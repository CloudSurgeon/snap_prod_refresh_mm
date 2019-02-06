
# Snapshot the dSources and Refresh the VDBs

#### Table of Contents
1.  [Description](#description)
2.  [Options](#options)
3.  [Example Config File](#example)
4.  [Contribute](#contribute)
    *   [Code of conduct](#code-of-conduct)
    *   [Community Guidelines](#community-guidelines)
    *   [Contributor Agreement](#contributor-agreement)
5.  [Reporting Issues](#reporting-issues)
6.  [Statement of Support](#statement-of-support)
7.  [License](#license)

## <a id="description"></a>Description
This script/binary will wait for an engine to be ready, and then snapshot the dSources and then refresh the VDBs.

Currently only works for UnixHost with passwordless SSH. 

## <a id="options"></a>Options for the script
	Application Options:
  	-e, --ddp_hostname=  The hostname or IP address of the Delphix Dynamic Data Platform [$DELPHIX_DDP_HOSTNAME]
  	-u, --username=      The username used to authenticate to the Delphix Engine [$DELPHIX_USER]
  	-p, --password=      The password used to authenticate to the Delphix Engine [$DELPHIX_PASS]
  	-v, --debug          Turn on debugging. -vvv for the most verbose debugging [$DELPHIX_DEBUG]
        --skip-validate  Don't validate TLS certificate of Delphix Engine [$DELPHIX_SKIP_VALIDATE]
  	-c, --config=        Optional INI config file to pass in for the variables
        --dsource=       The name of the dSource to snapsync [$DELPHIX_DSOURCE]
        --vdb=           The name of the VDB to snapsync [$DELPHIX_VDB]

## <a id="example"></a>Example config file
	ddp_hostname = delphixengine
	username = delphix_admin
	password = landshark
	skip-validate = 1
	dsource = "Patients Prod"
	vdb = "Patients Masked Master"

## <a id="contribute"></a>Contribute

1.  Fork the project.
2.  Make your bug fix or new feature.
3.  Add tests for your code.
4.  Send a pull request.

Contributions must be signed as `User Name <user@email.com>`. Make sure to [set up Git with user name and email address](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup). Bug fixes should branch from the current stable branch. New features should be based on the `master` branch.

#### <a id="code-of-conduct"></a>Code of Conduct

This project operates under the [Delphix Code of Conduct](https://delphix.github.io/code-of-conduct.html). By participating in this project you agree to abide by its terms.

#### <a id="contributor-agreement"></a>Contributor Agreement

All contributors are required to sign the Delphix Contributor agreement prior to contributing code to an open source repository. This process is handled automatically by [cla-assistant](https://cla-assistant.io/). Simply open a pull request and a bot will automatically check to see if you have signed the latest agreement. If not, you will be prompted to do so as part of the pull request process.


## <a id="reporting_issues"></a>Reporting Issues

Issues should be reported [here](https://github.com/delphix/automation-framework-demo/issues).

## <a id="statement-of-support"></a>Statement of Support

This software is provided as-is, without warranty of any kind or commercial support through Delphix. See the associated license for additional details. Questions, issues, feature requests, and contributions should be directed to the community as outlined in the [Delphix Community Guidelines](https://delphix.github.io/community-guidelines.html).

## <a id="license"></a>License

This is code is licensed under the Apache License 2.0. Full license is available [here](./LICENSE).


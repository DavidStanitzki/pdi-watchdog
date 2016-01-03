PDI Watchdog is a combination of [PDI](http://community.pentaho.com/projects/data-integration/) Jobs for implementing a watchdog feature. The main inspiration is to abort Jobs and Transformations automatically after a specified interval and restart on errors for a designated number of times.

## Features

* Start transformation/jobs stored on filesystem
* Start transformation/jobs stored in repository
* Retry on error counter
* Abort after timeout

## Supported Versions

* Pentaho Data Integration 4.4 (and later)

I have not tested earlier versions. They might work but without warranty.

### Installation

If you work on a local filesystem you should use the jobs stored in 'filesystem' folder. If you work with a repository you should use 'repository' folder.

Save the jobs whereever you want on your filesystem or repository. You can call them with kitchen.bat/kitchen.sh

### Configuration

#### Parameters

* watchdog.interval (check interval in seconds)
	* Default: 1
* watchdog.retry.count (retry count on error)
	* Default: 3
* watchdog.retry.timeout (timeout on retry in seconds)
	* Default: 3
* watchdog.timeout (job execution timeout in seconds)
	* Default: 3600
* watchdog.transformation.dir (only if you call a transformation; transformation directory in repository or filesystem; no ending '/' or '\' required)
* watchdog.transformation.name (only if you call a transformation; transformation name in repository or filesystem; file extension required if you work on filesystem)
* watchdog.job.dir (only if you call a job; job directory in repository or filesystem; no ending '/' or '\' required)
* watchdog.job.name (only if you call a job; job name in repository or filesystem; file extension required if you work on filesystem)
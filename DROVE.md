==============DROVE================

Container orch.

benefits
-to have very simple packaging and deployment structures 
-in phonepe we package all our apps as containers


Previous use - Mesos (container Orch.)
-originally made for job scheduler (is a specialized component that sits on top of the Mesos master to decide 
which tasks should run, where they should run, and when they should run, based on available resources offered 
by Mesos.)
-Managed by Apache


Mesos + Marathon, used for container orch. 

Drove supports two types - Applications & Tasks

types of Drove:
    =Application-   set of instances or the surface they are runing on it 
    =Instances-     container running on the cluster that belongs to an application
    =Task-          same as instnaces but runs for a shorter period
    =Resource-      control 2 types or resources(CPU & Memory) 
    =Operation-     what ever activities you are doing on the cluster
    =Controller-    responsible for commanding the executor to take up an application/start or stop or killl an instances.Resources are present here
    =Executor-      responsible for the execution of cluster on the local machine



_______Application_______
has a .json file called specification thast has info -name, version, which image to put in which contianer

_______Operations_______
commands that you sent to the cluster (CREATE, DESTROY, START_INSTANCES, STOP_INSTANCES, REPLACE_INSTANCE) 
basiclaly called the senddown to the executors

_______Instances_______
Instance are randomly generated and start with AI-<uuid> 
logs are available in /drove/drove-executor/<appid>/<Instanceid>
logs are moved to log backup just like mesos


_______Tasks_______
-runs certain process daily and creates the logs 


*Architecture*
(Console/Rosey/Nixy) ---------> Controller ------Zookeeper------Executor/Executor/Executor.


# Points
- When we reqyest spoit isntance
- WE might not get the instance immediately
- WE might get it when the capacity is available in AWS
- The spare resources are provided as spot instances
- It can give upto 90% discount price
- These instances can also be taken up. They will provide 2 minute warning and instance will be terminated.
- Stateless workloads. non time sensitive workloads can be run on spot instances
- Can be used with autoscaling groups.


# Strategies
- We can try at different times of the day for requestin spot insstances
- WE can try with different instancce_types.
- WE can try in different AZ or region.

# use cases
- non time sensitive, big data, CICD etc.

# anti pattern
- If workload is critical or statefu lworkloads cannot be run

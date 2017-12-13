# Data-Science-Cisco-Project

Cisco created a test network (the “Testbed”) which represented a small section of the network architecture used by large companies to facilitate communication between their users.

The network architecture includes nodes called “leaves” [using NCS 5011 machines] and nodes called “spines” [using both NCS 5011 and NCS 5508 machines]. Leaves are generally found at the edges of a network. Data from outside the network enters at a leaf, is routed through a spine, and is then directed to the leaf nearest to the data’s ultimate destination.

The Testbed has 8 leaves (labeled leaf1 through leaf8 in the diagram) and 4 spines (labeled spine1 through spine4 in the diagram) for a total of 12 machines for which telemetry is collected and failure can be simulated. The network also contains two machines of type NCS 5508 that are a different type of spine, labeled DR01 and DR02. Although some telemetry data from these machines is available, no failures of these two machines occur during the tests.

A machine “failure” in the Testbed is simulated by a machine deleting the list of nearby nodeswhich allows a machine to send on data. Deletion is done with a “Border Gateway Protocol Clear” or “bgpclear” command to that machine. When that command is executed, data sent to that machine cannot be sent on until that machine has re-identified its neighbors and repopulated the bgp file. In the meantime, network traffic will be re-routed through other, nearby machines. A failure in one machine is therefore marked by a sharp but temporary reduction in data traffic through it, and a comparable increase in data traffic elsewhere in the network.

Our initial goal was to describe distinct visual or other patterns in the data that characterize each type of file, upon manual inspection.

Final goal was to automate the classification process using machine learning, so that a new time series of telemetry data could be classified in a completely automated manner as containing no event, or one or more of the above failure events.

Eventually, the aim was to forecast failures before they occur.

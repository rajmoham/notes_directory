- Distribute data amongst multiple systems/servers

# How it works?
Hash-ring -> an abstract ring with fixed number of points

Database servers are distributed across that hash ring.

1. Hash the data to get a key.
2. Find the point in the hash ring which equates to the key.
3. Move clockwise until a database server node is hit.
4. The data is then stored in this database server.

<img src="https://substackcdn.com/image/fetch/$s_!AP4x!,w_1200,h_600,c_fill,f_jpg,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F97b32e34-1236-4124-a6b1-46feb0ed498f_800x640.png"/>
# Scalability
### Adding/removing a DB server
When adding/removing a new server, there will only be a certain range of data that needs to be transferred from a single other database.
This avoids mass redistribution.

# Virtual Nodes
To ensure that there is no disproportional distribution of data, there can be virtual nodes (DB nodes which represent which DB server data will be stored in.)

<img src="https://www.researchgate.net/publication/318474318/figure/fig2/AS:658881982263296@1534101114101/A-ring-based-hash-space-for-3-servers-each-with-4-virtual-nodes.png" />

# Variants
### Rendezvous Hashing

### Jump Consistent Hashing
# Source
[https://youtu.be/vccwdhfqIrI?si=TFQ3C4l1fGWDjwlN&t=181](https://youtu.be/vccwdhfqIrI?si=TFQ3C4l1fGWDjwlN&t=181)



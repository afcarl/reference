# Architecture

## Emergent

Build working software and produce an "as built" diagram. 

## Evolutionary



## Intentional 

Plan everything in advance of building anything.

# Testing aka Quality

## Types or tools for testing and quality

Layers of testing:
- Linting and static code analysis
- Unit testing
- Contract Testing -- Use a provider/consumer model to write request/response unit tests from one side to a mock of the other. Then use the mock to actually test that other side.
- Integration Testing
- End to End (system) tests.
- Health Monitoring -- event driven checks, e.g. decreasing code coverage, increasing response times, increasing build times etc.
- External Acceptance Tests -- Add hoc end to end testing performed outside of the development group. If this is performed by actual expected users, it may be considered beta testing. If it is testing in the security dimension, it may be considered pen testing.

Dimensions of specialized testing:
- Security
- Reliability / Resiliency over time 
- Performance / Speed
- Scale / Load
- Availability, may be tested separately for a baseline and then examined in other dimensions above.

# MD ^^ / reformat vv

+ Content-Addressable Storage + 

aka + content addressable memory + Typically refers to hardware implementations.
aka + associative memory + 
aka + associative storage +
aka | associative array |

A mechanism for storing information so that it can be retrieved based on its content rather than its storage location.

> | git | is a good example, using a | SHA-1 | hash of the data


+ CORBA + 

An object oriented interface design that provides standard bindings to major languages and provides an interface to permit diverse systems to communicate.

> This seems to be, in effect, a standardized way to implement APIs.

#distrbuted_computing

+ DCOM + Distributed Computing Object Model.

Microsoft proprietary competitor to | CORBA |.


+ DDObjects +

Similar to | CORBA |, a means of providing distributed computing and a generalized API for projects within the Delphi (Object Pascal) framework.

+ Design by contract +

aka + contract programming +

The application of preconditions (client obligations, supplier benefits), post conditions (client benefits, supplier obligations) and invariants (general laws or rules for contracts) to service/software design. Strangely this is trademarked by Eiffel Software.


+ dereference +

aka + dereferencing +
aka + indirecting +

An operation on a |pointer| that returns a value equivalent to the value stored at the pointer's address.


+ ICMP +

Internet Control Message Protocol

A supporting protocol to IP that sends control and diagnostic messages.

#distributed_computing


+ RPC +

Remote Procedure Call

A request-response protocol facilitating running subprocesses in an alternative address space (e.g. on another computer via a network) so that code is essentially the same irrespective of its being local, on remote A, remote B etc.

1. Client calls the client stub. This is a local procedure call.
2. Client stub _marshalls_ the parameters into a message that is provided to the system.
3. Clinet OS sends message to server.
4. OS on Server passes packets to the server stub.
5. Server stub unmarshalls parameters from message.
6. Server stub calls server procedure, with response traversing the same path back.

+ Source Network Address Translation +

aka + SNAT +

The method of modifying the Source IP address on incoming packets to a network to ensure that a desired egress IP is identified by all responding servers.

Do not confuse with an essentially nonsense term of Secure Network Address Translation which generally uses Source NAT and claims that the particular implementation is Secure by virtue of some (typically) proprietary mechanism. The security of the implementation should be evaluated in terms of general network primitives, including Source NAT but necessarily other protocols and methods for routing based on them that have a specific security claim to make. For example, using Source NAT in combination with specific additional technology at the point of egress may offer concrete security improvements. However, in this case Source NAT is necessary, but neither sufficient for nor equivalent to an additional form of NAT that is inherently secure. 


+ Tuple space +

A |content-addressable memory| implementation of distributed computing, providing tuples taht can be accessed concurrently. Data is pushed to the space by producers, and then consumers retrieve the data.

+ JavaSpaces + is an implementation of a tuple space in | Java |.

+ Pointer + an object that contains a memory address pointing to another location in memory containing a value of interest. It is a *reference* to the value in the register pointed to. A strict definition of a pointer would require that the interface permit pointer arithmetic - manipulation of the address locations. The most common syntax for a pointer is `&p`. 

Pointers may be |dereferenced| - typically using the notation `p = *x` - which means the pointer takes the address of `x`. 

# Lamdera
split.lambdera.app

Elm in unusual domain
concordium builds a next-generation-blockchain
oak - smart contracts

elm concepts - purity / immutability translated to other domain


# CSS Domain
compile-to-css
styled-components, sass etc - css semantics
no reation to css - style-elements

if only I had a faster horse / better CSS framework

# App dev domain

Frontend
Encoding
Transport
Decoding
Backend
Querying
Storage

if only we had a better web dev stack

# Lamdera

500 LOC elm
- fe be
- persistence
- no encoder
- network api
- no query

# Modelling Apps
Frontend
= State + Events
Backend
= State + Events

Events from Frontend to Backend
Events from Backend to Frontend

# Spec
FrontendMsg - (Frontend (Model)) - toBackend / ToFrontend - (backend (Model)) - BackendMsg
view + update                                   update (no view)
       updateFromBackend                        updateFromFrontend

- different kinds of data are on the transport layer than in inside the frontend / abckedn itself

```
sendToBackend : ToBackend -> Cmd msg
sendToFrontend : ClientId -> ToFrontend -> Cmd msg
```

# Communication
- evergreen
- immutability, lack of side-effects
- evergreen gives you the conversion function
- upgrade functions are generated automatically

Questions
- How to use
- Join development
- CMS or only realtime?
- ClientJoin can be automated?
- meteor:
  - backend controls the state
  - isomorphic code? / synchronized state / protected operations
- crdt

Commercial
- superset of elm
- abstracted implementaiton
- forks shold have economic disincentives to stay close to elm

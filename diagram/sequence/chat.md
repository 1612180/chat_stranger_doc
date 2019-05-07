# Chat sequence diagram


```plantuml
@startuml

Frontend -> Frontend: Filter user to chat (by favorite, age, gender)

loop
    Frontend -> Server: Send filter setting
    activate Server

    Frontend -> Server: Request another user to chat

    Server -> Database: Get all user ready with filter
    activate Server

    Database --> Server: Send all user ready with filter

    Server -> Server: Use algorithm to find **match user**
    deactivate Server

    alt found 1 user ready to chat
        Server --> Frontend: Response **match user** info to chat
        Frontend -> Frontend: Show chat screen with user
        Frontend -> Frontend: Choose **Next** (to request another user)
    else found no one
        Server --> Frontend: Send error
        Frontend --> Frontend: Show error screen
        alt If want to quit
            break
                Frontend -> Frontend: Quit
            end
        end
    end
end

@enduml
```
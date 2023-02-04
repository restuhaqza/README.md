# Hello there, Restu here! 😎
```go
package main

import (
	"encoding/json"
	"fmt"
	"log"
)

type MySelf struct {
	Name         string       `json:"name"`
	Pronoun      []string     `json:"pronoun"`
	Code         []string     `json:"code"`
	Architecture []string     `json:"architecture"`
	Technologies Technologies `json:"technologies"`
	Skills       []string     `json:"skills"`
	CurrentFocus string       `json:"currentFocus"`
	AskMeAbout   []string     `json:"askMeAbout"`
	Hobbies      []string     `json:"hobbies"`
}

type Technologies struct {
	Backend   []string `json:"backend"`
	Frontend  []string `json:"frontend"`
	Mobile    []string `json:"mobile"`
	Databases []string `json:"databases"`
	DevOps    []string `json:"devops"`
	Misc      []string `json:"misc"`
}

func SetProfile() *MySelf {
	return &MySelf{
		Name:         "Restu Muzakir",
		Pronoun:      []string{"He", "Him"},
		Code:         []string{"TypeScript", "JavaScript", "Go", "Java", "PHP"},
		Architecture: []string{"Serverless", "Monolith App", "Microservices"},
		Technologies: Technologies{
			Backend:   []string{"Node: Express, NestJS", "Go: Gin"},
			Frontend:  []string{"ReactJS"},
			Mobile:    []string{"React Native"},
			Databases: []string{"MySQL", "PostgreSQL", "MongoDB"},
			DevOps:    []string{"Docker", "Kubernetes", "AWS/Azure/GoogleCloud"},
			Misc:      []string{"Firebase", "SocketIO"},
		},
		Skills:       []string{"Team Lead", "System Analyst", "Coder", "Maintainer"},
		CurrentFocus: "Core Engineering",
		AskMeAbout:   []string{"Tech", "Business"},
		Hobbies:      []string{"YoYo Player", "Hypnosis"},
	}
}

func (m *MySelf) Hello() string {
	return fmt.Sprintf("Hello there, %s is here", m.Name)
}

func main() {
	profile := SetProfile()
	output, err := json.Marshal(profile)
	if err != nil {
		log.Fatal(err)
	}

	fmt.Println(profile.Hello())
	fmt.Println(string(output))
}

```
---
* 📨 Follow me => [@restuhaqza]()


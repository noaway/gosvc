##use

```
package main

import (
	"log"

	"github.com/noaway/svc-go"
)

type proc struct{}

// Init func
func (p *proc) Init() error {
	log.Println("init")
	return nil
}

// Start func
func (p *proc) Start() error {
	log.Println("start")
	return nil
}

// Stop func
func (p *proc) Stop() error {
	log.Println("stop")
	return nil
}

func main() {
	if err := svc.Run(new(proc)); err != nil {
		log.Println(err)
	}
}

```
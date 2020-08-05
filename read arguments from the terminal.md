# read arguments from the terminal

1. `import "flag"`

   `var flags flag.type("name", "default value", "usage message")`

   `flag.Parse()`

   eg. `var intFlag  flag.Int("i", "0", "int value")`

   usage. `go run test.go -i=11`

   #### or

   `flag.Parse()`

   `flags := flag.Args() //obtain args from the terminal except those registered`

   #### or

   `type MyType struct{}`

   `func  (t *MyType) String() string{}`

   `func (t *MyType) Set(s string) error{}`

   `...`

   `var t MyType`

   `flag.Var(&t, "name", "usage message")   //store the flags in &t`

   `flag.Parse()`

   

   
2. `import "os"`

      `args := os.Args   //just like main function" int main(int argc, char **argv)" in C`

   

   

   

   

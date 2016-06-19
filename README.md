# Assert

Assert is a very simple testing framework to make tests work better.

## Usage

    package foo_test

    import "testing"
    import "toolkit/assert"
    import "foo"

    func TestTest(T *testing.T) {
    	assert.Test(T, func(T *assert.T) {
        fp := foo.New()
    		T.Assert(fp.TruthValue())
        if (fp.SomeThing()) {
          ...
        }
        else {
          T.Unreachable()
        }
    	})
    }

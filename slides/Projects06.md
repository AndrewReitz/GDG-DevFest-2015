#### Projects

### Android Spock

```groovy
class MainActivitySpec extends Specification {
  @UseActivity(MainActivity)
  def activity

  def "test activity setup"() {
    expect:
    activity != null
    activity instanceof MainActivity
  }

  def "test layout"() {
    given:
    def button = activity.findViewById(R.id.main_button) as Button

    when:
    def buttonText = button.getText()

    then:
    buttonText == "Test"
  }
}
```

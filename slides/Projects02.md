#### Projects

### SwissKnife

```groovy
class MyActivity extends Activity {
  @SaveInstance public String myString;

  @OnClick(R.id.button) void onButtonClicked(Button button) {
    Toast.makeText(this, "Button clicked", Toast.LENGTH_SHOT).show();
  }

  @OnBackground void doSomeProcessing(URL url) {
    // Contents will be executed on background
  }

  @Override protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    // This must be called for injection of views and callbacks to take place
    SwissKnife.inject(this);

    // This must be called for saved state restoring
    SwissKnife.restoreState(this, savedInstanceState);
  }
}
```
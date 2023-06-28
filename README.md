# About Emojicon
Twemojicon based on [original Emojicon project](https://github.com/rockerhieu/emojicon), the development of which was discontinued.

## Emojicon with Twemoji pack (Twemojicon)

Do you like Twemojis? [Twemojicon](https://github.com/tinelix/twemojicon) is a library to implement such a thing for Android.

## Example

### emojiconize

```java
import dev.tinelix.twemojiconize.Emojiconize;

// Your activity must be a subclass of AppCompatActivity
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        // Emojiconize the whole activity, must call before `super.onCreate()`
        Emojiconize.activity(this).go();
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}
```
More information: [rockerhieu/emojiconize](https://github.com/rockerhieu/emojiconize)

### emojicon

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              xmlns:emojicon="http://schemas.android.com/apk/res-auto"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              android:orientation="vertical">

    <dev.tinelix.twemojicon.EmojiconTextView
            android:id="@+id/txtEmojicon"
            android:text="I \ue32d emojicon"
            emojicon:emojiconAlignment="baseline"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"/>

    <dev.tinelix.twemojicon.EmojiconEditText
            android:id="@+id/editEmojicon"
            android:text="I \ue32d emojicon"
            emojicon:emojiconSize="28sp"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"/>
    <fragment
            android:id="@+id/emojicons"
            android:layout_width="match_parent"
            android:layout_height="220dp"
            class="dev.tinelix.twemojicon.EmojiconsFragment"/>
</LinearLayout>
```

![image](https://github.com/rockerhieu/emojicon/raw/master/images/sample.jpg)

_Note: You can change the size and alignment of emojis in XML layout through attribute `emojiconSize` and `emojiconAlignment`, respectively._

## Usage

* `EmojiconTextView`: a `TextView` which can render emojis.
* `EmojiconEditText`: a `EditText` which can render emojis.
* `EmojiconMultiAutoCompleteTextView`: a `MultiAutoCompleteTextView` which can render emojis.
* `EmojiconGridFragment`: a fragment contains emojis in a `GridView` for the user to choose.
* `EmojiconsFragment`: a fragment contains many set of emojis for the user to choose.

## Building in IntelliJ

Via Gradle:

```
compile 'io.github.rockerhieu:emojicon:<latest-version>'
```

## Acknowledgements

Emojicon is using emojis graphics from [Twemoji](https://github.com/arvida/emoji-cheat-sheet.com/tree/master/public/graphics/emojis), licensed by [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Contributing

Please fork this repository and contribute back using
[pull requests](https://github.com/tinelix/emojicon/pulls).

Any contributions, large or small, major features, bug fixes, additional
language translations, unit/integration tests are welcomed and appreciated
but will be thoroughly reviewed and discussed.

## License

* [Apache Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

```
Copyright 2014 Hieu Rocker

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

 http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

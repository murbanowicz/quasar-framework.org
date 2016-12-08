title: Lists
---
Quasar Lists are used to display rows of information, such as a contact list, a playlist, or menu. Each row is called an item. Items can also be used outside of a list.

Lists can also be used (and it's also recommended) on Quasar Drawers. There's even a `<q-drawer-link>` component based on List Items.

> We'll learn to use Lists and List Items gradually. Make sure you don't skip steps and follow this page.

Scroll down to see the demos if on desktop.

## List Basics
<input type="hidden" data-demo="css/list/basic">

``` html
<p class="caption">Basic List</p>
  <div class="list">
    <div class="item" v-for="n in 2">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">No Border</p>
  <div class="list no-border">
    <div class="item" v-for="n in 2">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">Striped</p>
  <div class="list striped">
    <div class="item" v-for="n in 6">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">Delimiter Between Items</p>
  <div class="list">
    <div class="item">
      <div class="item-content">
        List Item
      </div>
    </div>
    <hr>
    <div class="item">
      <div class="item-content">
        List Item
      </div>
    </div>
    <hr>
    <div class="item">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">Delimiter within Items</p>
  <div class="list item-delimiter">
    <div class="item" v-for="n in 3">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">Platform Delimiter - changes based on Theme</p>
  <div class="list platform-delimiter">
    <div class="item" v-for="n in 3">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">Inset Delimiter within Items</p>
  <div class="list item-inset-delimiter">
    <div class="item" v-for="n in 3">
      <div class="item-content inset">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">List Labels</p>
  <div class="list">
    <div class="list-label">List Label</div>
    <div class="item" v-for="n in 2">
      <div class="item-content">
        List Item
      </div>
    </div>
    <hr>
    <div class="list-label">Another List Label</div>
    <div class="item" v-for="n in 3">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">Inset: Items, Delimiters and Labels</p>
  <div class="list">
    <div class="item">
      <div class="item-content inset">
        List Item
      </div>
    </div>
    <hr class="inset">
    <div class="list-label inset">Inset List Label</div>
    <div class="item" v-for="n in 2">
      <div class="item-content inset">
        List Item
      </div>
    </div>
    <hr class="inset">
    <div class="item">
      <div class="item-content inset">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">
    Highlight (Desktop only)
    <small>
      <br>
      <span class="mobile-only">
        On desktop, hovering the list items will change their background
        color temporarily.
      </span>
      <span class="desktop-only">
        Hover the list items to change their background color temporarily.
      </span>
    </small>
  </p>
  <div class="list highlight">
    <div class="item" v-for="n in 2">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>

  <p class="caption">
    Link Items (Desktop only)
    <small>
      <br>
      <span class="mobile-only">
        On desktop, hovering the list items will change their background
        color temporarily and the cursor will be a pointer.
      </span>
      <span class="desktop-only">
        Hover the list items to change their background color temporarily
        and change cursor to pointer.
      </span>
    </small>
  </p>
  <div class="list">
    <div class="item item-link" v-for="n in 2">
      <div class="item-content">
        List Item
      </div>
    </div>
  </div>
```

## List Items
<input type="hidden" data-demo="css/list/item">

``` html
<p class="caption">Primary</p>
<div class="list item-inset-delimiter">
  <div class="item">
    <i class="item-primary">assignment_ind</i>
    <div class="item-content">Icon as Primary</div>
  </div>
  <div class="item">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content">Avatar as Primary</div>
  </div>
  <div class="item">
    <img class="item-primary thumbnail" :src="'statics/mountains.jpg'">
    <div class="item-content">Thumbnail as Primary</div>
  </div>
  <div class="item">
    <div class="item-primary">Q</div>
    <div class="item-content">One character as Primary</div>
  </div>
</div>

<p class="caption">Secondary</p>
<div class="list">
  <div class="item">
    <div class="item-content has-secondary">Icon as Secondary</div>
    <i class="item-secondary">info</i>
  </div>
  <hr>
  <div class="item">
    <div class="item-content has-secondary">Avatar as Secondary</div>
    <img class="item-secondary" :src="'statics/boy-avatar.png'">
  </div>
  <hr>
  <div class="item">
    <div class="item-content has-secondary">Thumbnail as Secondary</div>
    <img class="item-secondary thumbnail" :src="'statics/mountains.jpg'">
  </div>
  <hr>
  <div class="item">
    <div class="item-content has-secondary">One character as Secondary</div>
    <div class="item-secondary">Q</div>
  </div>
</div>

<p class="caption">Example Items with Primary and Secondary</p>
<div class="list item-inset-delimiter">
  <div class="item">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">Jack</div>
    <i class="item-secondary">chat_bubble</i>
  </div>
  <div class="item">
    <img class="item-primary" :src="'statics/linux-avatar.png'">
    <div class="item-content has-secondary">Jim's Photos</div>
    <img class="item-secondary thumbnail" :src="'statics/mountains.jpg'">
  </div>
  <div class="item">
    <i class="item-primary">voice_chat</i>
    <div class="item-content has-secondary">Voice Chat with Joe</div>
    <img class="item-secondary" :src="'statics/boy-avatar.png'">
  </div>
  <div class="item">
    <div class="item-primary">J</div>
    <div class="item-content has-secondary">John Doe</div>
    <img class="item-secondary" :src="'statics/guy-avatar.png'">
  </div>
</div>

<p class="caption">Stamp and Truncated Content</p>
<div class="list" style="max-width: 400px">
  <div class="item">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Brunch this weekend? Brunch this weekend? Brunch this weekend?</div>
    </div>
    <div class="item-secondary stamp">
      1 week
    </div>
  </div>
  <div class="item two-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Brunch this weekend? Brunch this weekend? Brunch this weekend?</div>
      <div>John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe </div>
    </div>
    <div class="item-secondary stamp">
      10 min
    </div>
  </div>
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Brunch this weekend? Brunch this weekend? Brunch this weekend?</div>
      <div>
        <span>John Doe</span>
        -- I'll be in your neighborhood doing errands this
        weekend. Do you want to grab brunch?
      </div>
    </div>
    <div class="item-secondary stamp">
      2 years
    </div>
    <i class="item-secondary">mail</i>
  </div>
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Brunch this weekend? Brunch this weekend? Brunch this weekend?</div>
      <div>
        <span>John Doe</span>
        -- I'll be in your neighborhood doing errands this
        weekend. Do you want to grab brunch?
      </div>
    </div>
    <div class="item-secondary stamp">
      1 week ago
    </div>
    <i class="item-secondary">mail</i>
  </div>
</div>

<p class="caption">Item with Actions</p>
<div class="list">
  <div class="item">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Brunch this weekend?</div>
    </div>
    <div class="item-secondary">
      <i slot="target">
        more_vert

        <q-popover ref="popover">
          <div class="list">
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Reply</div>
            </div>
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Forward</div>
            </div>
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Delete</div>
            </div>
          </div>
        </q-popover>
      </i>
    </div>
  </div>
</div>
```

## Multi-line Items
<input type="hidden" data-demo="css/list/multiline">

Multiple line items are usually for some Form components that exceed the height of a predefined one, two or three lines item.

``` html
<div class="list">
  <div class="item">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      One line item
    </div>
    <div class="item-secondary stamp">
      1 week
    </div>
  </div>
  <hr>
  <div class="item two-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Two line item</div>
      <div>Second line</div>
    </div>
    <div class="item-secondary stamp">
      10 min
    </div>
  </div>
  <hr>
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Three line item</div>
      <div>
        <span>Second & Third line</span>
        -- I'll be in your neighborhood doing errands this
        weekend. Do you want to grab brunch?
      </div>
    </div>
    <div class="item-secondary stamp">
      2 years
    </div>
    <i class="item-secondary">mail</i>
  </div>
  <hr>
  <div class="item multiple-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Multiple lines item</div>
      <div class="item-label item-smaller">Second line</div>
      <div class="item-label item-smaller">Third line</div>
      <div class="item-label item-smaller">Fourth line</div>
      <div class="item-label item-smaller">...as many as you need!</div>
    </div>
    <div class="item-secondary">
      <i slot="target">
        more_vert

        <q-popover ref="popover">
          <div class="list">
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Reply</div>
            </div>
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Forward</div>
            </div>
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Delete</div>
            </div>
          </div>
        </q-popover>
      </i>
    </div>
  </div>
</div>
```

## Collapsible Items
<input type="hidden" data-demo="css/list/collapsible">

Collapsible Items make use of the Collapsible Component. Read more about it [here](/components/collapsible.html).

You can nest collapsibles within collapsibles within collapsibles within...
``` html
<div class="list">
  <q-collapsible icon="inbox" label="Inbox">
    <div class="item" v-for="n in 3">
      <i class="item-primary">mail</i>
      <div class="item-content">
        Email {{ n + 1 }}
      </div>
    </div>
    <q-collapsible icon="favorites" label="Favorites">
      <div class="item" v-for="n in 3">
        <i class="item-primary">mail</i>
        <div class="item-content">
          Favorite {{ n + 1 }}
        </div>
      </div>
    </q-collapsible>
  </q-collapsible>
  <q-collapsible icon="send" label="Sent">
    <div class="item" v-for="n in 3">
      <i class="item-primary">mail</i>
      <div class="item-content">
        Email {{ n + 1 }}
      </div>
    </div>
  </q-collapsible>
  <q-collapsible icon="delete" label="Trash">
    <div class="item" v-for="n in 3">
      <i class="item-primary">mail</i>
      <div class="item-content">
        Email {{ n + 1 }}
      </div>
    </div>
  </q-collapsible>
</div>
```

## List with Textfields
<input type="hidden" data-demo="css/list/example-textfields">

Some predefined forumals you can use to nest Textfields in List Items.
``` html
<div class="list">
  <div class="list-label">Textboxes</div>
  <div class="item two-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <input class="full-width">
    </div>
  </div>

  <hr>
  <div class="item two-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <input placeholder="Placeholder" class="full-width">
    </div>
  </div>

  <hr>
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content row items-center wrap">
      <div style="margin-right: 10px;" class="item-label">Label:</div>
      <input class="auto">
    </div>
  </div>

  <hr>
  <div class="item three-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <div class="stacked-label">
        <input class="full-width">
        <label>Stacked Label</label>
      </div>
    </div>
  </div>

  <hr>
  <div class="item three-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <div class="floating-label">
        <input required class="full-width">
        <label>Floating Label</label>
      </div>
    </div>
  </div>

  <hr>
  <div class="list-label">Textareas</div>
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <textarea class="full-width"></textarea>
    </div>
  </div>

  <hr>
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <div style="margin-right: 10px;" class="item-label">Label:</div>
      <textarea class="full-width"></textarea>
    </div>
  </div>

  <hr>
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <div class="stacked-label">
        <textarea class="full-width"></textarea>
        <label>Stacked Label</label>
      </div>
    </div>
  </div>

  <hr>
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <div class="floating-label">
        <textarea required class="full-width"></textarea>
        <label>Floating Label</label>
      </div>
    </div>
  </div>

  <hr>

  <div class="list-label">Numeric</div>
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <span class="item-label">Number:</span>
      <q-numeric v-model="number"></q-numeric>
    </div>
  </div>
  <hr class="inset">
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <span class="item-label">Number:</span>
      <q-numeric v-model="number"></q-numeric>
    </div>
  </div>

  <hr>

  <div class="list-label">Chips Textbox</div>
  <div class="item multiple-lines">
    <i class="item-primary">edit</i>
    <div class="item-content">
      <q-chips v-model="chips" placeholder="Type names"></q-chips>
    </div>
  </div>
</div>
```

## List with Form Components
<input type="hidden" data-demo="css/list/example-form">

Some predefined formulas you can use to nest Form Components within List Items.

``` html
<p class="caption">Checkboxes</p>
<div class="list">
  <label class="item">
    <div class="item-primary">
      <q-checkbox v-model="checked"></q-checkbox>
    </div>
    <div class="item-content">
      Notifications
    </div>
  </label>
  <label class="item two-lines">
    <div class="item-primary">
      <q-checkbox v-model="checked"></q-checkbox>
    </div>
    <div class="item-content">
      <div>Notifications</div>
      <div>Allow notifications</div>
    </div>
  </label>
  <label class="item three-lines">
    <div class="item-primary">
      <q-checkbox v-model="checked"></q-checkbox>
    </div>
    <div class="item-content">
      <div>Notifications</div>
      <div>Allow notifications Allow notifications Allow notifications Allow notifications Allow notifications </div>
    </div>
  </label>
</div>

<p class="caption">Radios</p>
<div class="list">
  <label class="item">
    <div class="item-primary">
      <q-radio v-model="option" val="opt1"></q-radio>
    </div>
    <div class="item-content">
      Option 1
    </div>
  </label>
  <label class="item two-lines">
    <div class="item-primary">
      <q-radio v-model="option" val="opt2"></q-radio>
    </div>
    <div class="item-content">
      <div>Option 2</div>
      <div>Allows notifications</div>
    </div>
  </label>
  <label class="item three-lines">
    <div class="item-primary">
      <q-radio v-model="option" val="opt3"></q-radio>
    </div>
    <div class="item-content">
      <div>Option 3</div>
      <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
    </div>
  </label>
</div>

<p class="caption">Toggles</p>
<div class="list">
  <label class="item">
    <div class="item-content has-secondary">
      Events and reminders
    </div>
    <div class="item-secondary">
      <q-toggle v-model="checked"></q-toggle>
    </div>
  </label>
  <label class="item two-lines">
    <div class="item-content has-secondary">
      <div>Events and reminders</div>
      <div>Lorem ipsum</div>
    </div>
    <div class="item-secondary">
      <q-toggle v-model="checked" class="purple"></q-toggle>
    </div>
  </label>
  <label class="item three-lines">
    <div class="item-content has-secondary">
      <div>Events and reminders</div>
      <div>Lorem ipsum dolor sit amet...</div>
    </div>
    <div class="item-secondary">
      <q-toggle v-model="checked" class="red"></q-toggle>
    </div>
  </label>
</div>

<p class="caption">Select</p>
<div class="list">
  <div class="list-label">Single Selection</div>
  <div class="item multiple-lines">
    <i class="item-primary">supervisor_account</i>
    <div class="item-content">
      <q-select class="full-width" type="radio" v-model="select" :options="selectOptions" ok-label="Pick" cancel-label="Neah" title="Company"></q-select>
    </div>
  </div>
  <hr>
  <div class="list-label">Multiple Selection</div>
  <div class="item multiple-lines">
    <i class="item-primary">supervisor_account</i>
    <div class="item-content">
      <q-select class="full-width" type="checkbox" v-model="multipleSelect" :options="selectOptions" ok-label="Pick" title="Companies"></q-select>
    </div>
  </div>
  <div class="item multiple-lines">
    <i class="item-primary">supervisor_account</i>
    <div class="item-content">
      <q-select class="full-width" type="toggle" v-model="multipleSelect" :options="selectOptions" ok-label="Pick" title="Companies"></q-select>
    </div>
  </div>
</div>

<p class="caption">Ranges</p>
<div class="list">
  <div class="item two-lines">
    <i class="item-primary">volume_up</i>
    <div class="item-content">
      <q-range v-model="standalone" :min="0" :max="50" label></q-range>
    </div>
  </div>
  <div class="item two-lines">
    <i class="item-primary">brightness_medium</i>
    <div class="item-content">
      <q-range v-model="standalone" :min="0" :max="50" label></q-range>
    </div>
  </div>
  <hr>
  <div class="list-label">Double Range</div>
  <div class="item two-lines">
    <i class="item-primary">local_atm</i>
    <div class="item-content">
      <q-double-range :model-min.sync="standaloneMin" :model-max.sync="standaloneMax" :min="0" :max="50" label></q-double-range>
    </div>
  </div>
  <div class="item two-lines">
    <i class="item-primary">euro_symbol</i>
    <div class="item-content">
      <q-double-range :model-min.sync="standaloneMin" :model-max.sync="standaloneMax" :min="0" :max="50" label></q-double-range>
    </div>
  </div>
</div>

<p class="caption">Date and Time</p>
<div class="list">
  <div class="list-label">Date or Time</div>
  <div class="item two-lines">
    <i class="item-primary">access_time</i>
    <div class="item-content">
      <q-datetime class="full-width" v-model="timestamp" type="time"></q-datetime>
    </div>
  </div>
  <div class="item two-lines">
    <i class="item-primary">update</i>
    <div class="item-content row items-baseline">
      <q-datetime class="full-width" v-model="timestamp" type="date"></q-datetime>
    </div>
  </div>
  <hr>
  <div class="list-label">Date & Time</div>
  <div class="item two-lines">
    <i class="item-primary">notifications</i>
    <div class="item-content row items-baseline">
      <q-datetime class="full-width" v-model="timestamp" type="datetime"></q-datetime>
    </div>
  </div>
</div>
```

## Examples
Let's explore some ready to use templates using what we've learned above.

### Simple List
<input type="hidden" data-demo="css/list/example-simple">

``` html
<div class="list">
  <div class="item">
    <i class="item-primary">inbox</i>
    <div class="item-content">
      Inbox
    </div>
  </div>
  <div class="item">
    <i class="item-primary">send</i>
    <div class="item-content">
      Sent
    </div>
  </div>
  <div class="item">
    <i class="item-primary">delete</i>
    <div class="item-content">
      Trash
    </div>
  </div>
  <hr>
  <div class="item">
    <div class="item-content has-secondary">
      Inbox
    </div>
    <i class="item-secondary">
      inbox
    </i>
  </div>
  <div class="item">
    <div class="item-content has-secondary">
      Sent
    </div>
    <i class="item-secondary">
      send
    </i>
  </div>
  <div class="item">
    <div class="item-content has-secondary">
      Trash
    </div>
    <i class="item-secondary">
      delete
    </i>
  </div>
</div>
```

### Persons List
<input type="hidden" data-demo="css/list/example-persons">

``` html
<div class="list">
  <div class="list-label">People</div>
  <div class="item">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      John
    </div>
    <i class="item-secondary">
      chat_bubble
    </i>
  </div>
  <div class="item two-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Jim</div>
      <div>Javascript wiz kid</div>
    </div>
    <i class="item-secondary">
      chat_bubble
    </i>
  </div>
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      <div>Jake</div>
      <div>Passionate about Quasar</div>
    </div>
    <i class="item-secondary">
      chat_bubble
    </i>
  </div>
</div>
```

### Chat List
<input type="hidden" data-demo="css/list/example-chat">

``` html
<div class="list">
  <div class="list-label">Recent chats</div>
  <div class="item" v-for="n in 3">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content has-secondary">
      John Doe
    </div>
    <i class="item-secondary">
      chat_bubble
    </i>
  </div>
  <hr>
  <div class="list-label">Previous chats</div>
  <div class="item" v-for="n in 3">
    <img class="item-primary" :src="'statics/guy-avatar.png'">
    <div class="item-content">
      Jack Doe
    </div>
  </div>
</div>
```

### Movies List
<input type="hidden" data-demo="css/list/example-movies">

``` html
<div class="list">
  <div class="list-label">Movies</div>
  <div class="item">
    <img class="item-primary thumbnail" :src="'statics/mountains.jpg'">
    <div class="item-content has-secondary">
      <div>Mountains Documentary</div>
    </div>
    <i class="item-secondary">
      movie
    </i>
  </div>
  <div class="item two-lines">
    <img class="item-primary thumbnail" :src="'statics/mountains.jpg'">
    <div class="item-content has-secondary">
      <div>Mountains Documentary</div>
      <div>For passionates only</div>
    </div>
    <i class="item-secondary">
      movie
    </i>
  </div>
  <div class="item three-lines">
    <img class="item-primary thumbnail" :src="'statics/mountains.jpg'">
    <div class="item-content has-secondary">
      <div>Mountains Documentary</div>
      <div>For passionates only For passionates only For passionates only For passionates only For passionates only </div>
    </div>
    <i class="item-secondary">
      movie
    </i>
  </div>
</div>
```

### Contact List
<input type="hidden" data-demo="css/list/example-contacts">

``` html
<div class="list">
  <div class="item" v-for="n in 3">
    <i class="item-primary" v-if="n === 0">star</i>
    <div class="item-content inset has-secondary">
      John Joe
    </div>
    <img class="item-secondary" :src="'statics/boy-avatar.png'">
  </div>
  <hr class="inset">
  <div class="item" v-for="n in 3">
    <div class="item-primary" v-if="n === 0">A</div>
    <div class="item-content inset has-secondary">
      John Joe
    </div>
    <img class="item-secondary" :src="'statics/boy-avatar.png'">
  </div>
</div>
```

### Folder List
<input type="hidden" data-demo="css/list/example-folders">

``` html
<div class="list">
  <div class="list-label inset">Folders</div>
  <div class="item two-lines" v-for="n in 3">
    <div class="item-primary bg-grey-6 text-white">
      <i>folder</i>
    </div>
    <div class="item-content has-secondary">
      <div>Photos</div>
      <div>February 22, 2016</div>
    </div>
    <i class="item-secondary">info</i>
  </div>
  <hr class="inset">
  <div class="list-label inset">Files</div>
  <div class="item two-lines" v-for="n in 3">
    <div class="item-primary bg-primary text-white">
      <i>assignment</i>
    </div>
    <div class="item-content has-secondary">
      <div>Vacation</div>
      <div>February 22, 2016</div>
    </div>
    <i class="item-secondary">info</i>
  </div>
</div>
```

### Phonebook List
<input type="hidden" data-demo="css/list/example-phonebook">

``` html
<div class="list">
  <div class="item two-lines" v-for="n in 3">
    <i class="item-primary" v-if="n === 0">phone</i>
    <div class="item-content inset has-secondary">
      <div>(650) 555 - 1234</div>
      <div>Mobile</div>
    </div>
    <i class="item-secondary">chat_bubble</i>
  </div>
  <hr class="inset">
  <div class="item two-lines" v-for="n in 3">
    <i class="item-primary">mail</i>
    <div class="item-content">
      <div>john@doe.com</div>
      <div>Personal</div>
    </div>
  </div>
</div>
```

### Messages List
<input type="hidden" data-demo="css/list/example-messages">

``` html
<div class="list">
  <div class="list-label">Today</div>
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content inset has-secondary">
      <div>Brunch this weekend?</div>
      <div>
        <span>John Doe</span>
        -- I'll be in your neighborhood doing errands this
        weekend. Do you want to grab brunch?
      </div>
    </div>
    <div class="item-secondary stamp">
      1 week
    </div>
  </div>
  <hr class="inset">
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content inset has-secondary">
      <div>Brunch this weekend?</div>
      <div>
        <span>John Doe</span>
        -- I'll be in your neighborhood doing errands this
        weekend. Do you want to grab brunch?
      </div>
    </div>
    <i class="item-secondary">info</i>
  </div>
  <hr>
  <div class="list-label">Yesterday</div>
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content inset">
      <div>Brunch this weekend?</div>
      <div>
        <span>John Doe</span>
        <br>
        I'll be in your neighborhood doing errands this
        weekend. Do you want to grab brunch?
      </div>
    </div>
  </div>
  <hr class="inset">
  <div class="item three-lines">
    <img class="item-primary" :src="'statics/boy-avatar.png'">
    <div class="item-content inset has-secondary">
      <div>Brunch this weekend?</div>
      <div>
        <span>John Doe</span>
        <br>
        I'll be in your neighborhood doing errands this
        weekend. Do you want to grab brunch?
      </div>
    </div>
    <div class="item-secondary stamp">
      1 week
    </div>
    <div class="item-secondary">
      <i slot="target">
        more_vert

        <q-popover ref="popover">
          <div class="list">
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Reply</div>
            </div>
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Forward</div>
            </div>
            <div class="item item-link" @click="$refs.popover.close()">
              <div class="item-content">Delete</div>
            </div>
          </div>
        </q-popover>
      </i>
    </div>
  </div>
</div>
```

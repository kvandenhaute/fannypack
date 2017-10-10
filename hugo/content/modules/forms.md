+++
title = "Forms"
date = 2017-10-02T14:34:21+02:00
[menu.main]
parent = "Modules"
+++
# Forms

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima, quam!

<div class="fp-example">
	<form action="" method="" class="form">
		<fieldset class="form__group">
			<label for="inputid" class="form__label">Name</label>
			<input id="inputid" name="inputid" type="text" class="form__field" />
		</fieldset>
		<fieldset class="form__group">
			<label for="textareaid" class="form__label">Comment <span class="form__label-meta">(optional)</span></label>
			<span class="form__helptext" id="textareahelptext">A short help text for a textarea.</span>
			<textarea name="textareaname" id="textareaid" class="form__textarea" aria-describedby="textareahelptext"></textarea>
		</fieldset>
		<div class="form__actions">
			<button class="button button--default" type="reset">Reset</button>
			<button class="button button--primary" type="submit">Send</button>
		</div>
	</form>
</div>

```html
<form action="" method="" class="form">
	<fieldset class="form__group">
		<label for="nameid" class="form__label">Name</label>
		<input id="inputid" name="inputname" type="text" class="form__field" />
	</fieldset>
	<fieldset class="form__group">
		<label for="textareid" class="form__label">Comment <span class="form__label-meta">(optional)</span></label>
		<span class="form__helptext" id="textareahelptext">A short help text for a textarea.</span>
		<textarea name="textareaname" id="textareaid" class="form__textarea" aria-describedby="textareahelptext"></textarea>
	</fieldset>
	<div class="form__actions">
		<button class="button button--default" type="reset">Reset</button>
		<button class="button button--primary" type="submit">Send</button>
	</div>
</form>
```

### About labels and placeholders

**Always** use a `label` with your form elements. Don't use the `placeholder` attribute as a subsitute for a `label`. The `placeholder` attribute isn't meant to give an extensive description. It's meant to be a guideline or a hint.

<div class="fp-example">
	<div class="form__group">
		<input type="email" class="form__field" placeholder="e-mail address" />
	</div>
	<div class="form__group">
		<label class="form__label" for="emailplaceholder">E-mail</label>
		<input type="email" class="form__field" id="emailplaceholder" placeholder="john@example.com" />
	</div>
</div>

```html
<!-- BAD -->
<input type="email" class="form__field" placeholder="e-mail address" />

<!-- GOOD -->
<label class="form__label" for="email">E-mail</label>
<input type="email" class="form__field" id="email" placeholder="john@example.com" />
```

## Form elements

Form elements should always be wrapped by `.form__group`. This comes in handy when you want to implement **validation** later. This wrapper can be a `<div>` or a `<fieldset>`.

```html
<div class="form__group">
	<label for="nameid" class="form__label">Name</label>
	<input id="inputid" name="inputname" type="text" class="form__field" />
</div>

<fieldset class="form__group">
	<label for="nameid" class="form__label">Name</label>
	<input id="inputid" name="inputname" type="text" class="form__field" />
</fieldset>
```

### Date input

<div class="fp-example">
	<fieldset class="form__group">
		<label for="dateid" class="form__label">Date</label>
		<input type="date" id="dateid" name="datename" class="form__field" />
	</fieldset>
</div>

```html
<label for="dateid" class="form__label">Date</label>
<input type="date" id="dateid" name="datename" class="form__field" />
```

### Search field

<div class="fp-example">
	<fieldset class="form__group">
		<label for="searchid" class="form__label">Search</label>
		<input type="search" class="form__field" id="searchid" name="searchname" placeholder="Search query here" />
	</fieldset>
</div>

```html
<label for="searchid" class="form__label">Search</label>
<input type="search" class="form__field" id="searchid" name="searchname" placeholder="Search query here" />
```

### Telephone number input

<div class="fp-example">
	<fieldset class="form__group">
		<label for="telephoneid" class="form__label">Telephone</label>
		<input type="tel" class="form__field" id="telephoneid" name="telephonename" placeholder="+3235551234" />
	</fieldset>
</div>

```html
<label for="telephoneid" class="form__label">Telephone</label>
<input type="tel" class="form__field" id="telephoneid" name="telephonename" placeholder="+3235551234" />
```

### Number input

<div class="fp-example">
	<fieldset class="form__group">
		<label for="numberid" class="form__label">Number</label>
		<input type="number" id="numberid" name="numbername" class="form__field" step="3" />
	</fieldset>
</div>

```html
<label for="numberid" class="form__label">Number</label>
<input type="number" id="numberid" name="numbername" class="form__field" step="3" />
```

### Email input

<div class="fp-example">
	<fieldset class="form__group">
		<label for="emailid" class="form__label">Email</label>
		<input type="email" id="emailid" name="emailname" class="form__field" placeholder="john@example.com" />
	</fieldset>
</div>

```html
<label for="emailid" class="form__label">Email</label>
<input type="email" id="emailid" name="emailname" class="form__field" placeholder="john@example.com" />
```

### File upload

<div class="fp-example">
	<fieldset class="form__group">
		<label for="fileid" class="form__label">File</label>
		<input type="file" id="fileid" name="filename" class="form__field" accept="image/*" />
	</fieldset>
</div>

```html
<label for="fileid" class="form__label">File</label>
<input type="file" id="fileid" name="filename" class="form__field" accept="image/*" />
```

### Password field

<div class="fp-example">
	<fieldset class="form__group">
		<label for="passwordid" class="form__label">Password</label>
		<input type="password" id="passwordid" name="passwordname" class="form__field" placeholder="yourS4fePassw0rd" value="MyPassword" />
	</fieldset>
</div>

```html
<label for="passwordid" class="form__label">Password</label>
<input type="password" id="passwordid" name="passwordname" class="form__field" placeholder="yourS4fePassw0rd" value="MyPassw0rd" />
```

### Colorpicker

<div class="fp-example">
	<fieldset class="form__group">
		<label for="colorid" class="form__label">Colorpicker</label>
		<input type="color" id="colorid" name="colorname" class="form__field" />
	</fieldset>
</div>

```html
<label for="colorid" class="form__label">Colorpicker</label>
<input type="color" id="colorid" name="colorname" class="form__field" />
```

### Checkboxes and radio buttons

By default checkboxes and radio buttons are stacked.

<div class="fp-example">
	<fieldset class="form__group">
		<legend class="form__label" id="brandpicker">Choose a brand</legend>
		<div class="form__checkbox">
			<label class="form__checkbox__label">
				<input type="checkbox" class="form__checkbox__input" value="Levis" aria-describedby="brandpicker" /> Levis
			</label>
		</div>
		<div class="form__checkbox">
			<label class="form__checkbox__label">
				<input type="checkbox" class="form__checkbox__input" value="Lee" checked="checked" aria-describedby="brandpicker" /> Lee
			</label>
		</div>
	</fieldset>
</div>

```html
<legend class="form__label" id="brandpicker">Choose a brand</legend>
<div class="form__checkbox">
	<label class="form__checkbox__label">
		<input type="checkbox" class="form__checkbox__input" value="Levis" aria-describedby="brandpicker" /> Levis
	</label>
</div>
<div class="form__checkbox">
	<label class="form__checkbox__label">
		<input type="checkbox" class="form__checkbox__input" value="Lee" checked="checked" aria-describedby="brandpicker" /> Lee
	</label>
</div>
```

<div class="fp-example">
	<fieldset class="form__group">
		<legend class="form__label" id="happiness">Are you happy?</legend>
		<div class="form__radio">
			<label class="form__radio__label">
				<input type="radio" name="happiness" class="form__radio__input" value="yes" aria-describedby="happiness" /> Yes
			</label>
		</div>
		<div class="form__radio">
			<label class="form__radio__label">
				<input type="radio" name="happiness" class="form__radio__input" value="no" aria-describedby="happiness" /> No
			</label>
		</div>
	</fieldset>
</div>

```html
<fieldset class="form__group" >
	<legend class="form__label" id="happiness">Are you happy?</legend>
	<div class="form__radio">
		<label class="form__radio__label">
			<input type="radio" name="happiness" class="form__radio__input" value="yes" aria-describedby="happiness" /> Yes
		</label>
	</div>
	<div class="form__radio">
		<label class="form__radio__label">
			<input type="radio" name="happiness" class="form__radio__input" value="no" aria-describedby="happiness" /> No
		</label>
	</div>
</fieldset>
```

If you add modifier <code>.form\_\_checkbox--inline</code> or <code>.form\_\_radio--inline</code> they will display inline.

<div class="fp-example">
	<legend class="form__label" id="brandpicker2">Choose a brand</legend>
	<div class="form__checkbox form__checkbox--inline">
		<label class="form__checkbox__label">
			<input type="checkbox" class="form__checkbox__input" value="Levis" aria-describedby="brandpicker2" /> Levis
		</label>
	</div>
	<div class="form__checkbox form__checkbox--inline">
		<label class="form__checkbox__label">
			<input type="checkbox" class="form__checkbox__input" value="Lee" checked="checked" aria-describedby="brandpicker2" /> Lee
		</label>
	</div>
</div>

```html
<legend class="form__label" id="brandpicker2">Choose a brand</legend>
<div class="form__checkbox form__checkbox--inline">
	<label class="form__checkbox__label">
		<input type="checkbox" class="form__checkbox__input" value="Levis" aria-describedby="brandpicker2" /> Levis
	</label>
</div>
<div class="form__checkbox form__checkbox--inline">
	<label class="form__checkbox__label">
		<input type="checkbox" class="form__checkbox__input" value="Lee" checked="checked" aria-describedby="brandpicker2" /> Lee
	</label>
</div>
```

<div class="fp-example">
	<fieldset class="form__group">
		<legend class="form__label" id="happiness2">Are you happy?</legend>
		<div class="form__radio form__radio--inline">
			<label class="form__radio__label">
				<input type="radio" name="happiness2" class="form__radio__input" value="yes" aria-describedby="happiness2" /> Yes
			</label>
		</div>
		<div class="form__radio form__radio--inline">
			<label class="form__radio__label">
				<input type="radio" name="happiness2" class="form__radio__input" value="no" aria-describedby="happiness2" /> No
			</label>
		</div>
	</fieldset>
</div>

```html
<fieldset class="form__group">
	<legend class="form__label" id="happiness2">Are you happy?</legend>
	<div class="form__radio form__radio--inline">
		<label class="form__radio__label">
			<input type="radio" name="happiness2" class="form__radio__input" value="yes" aria-describedby="happiness2" /> Yes
		</label>
	</div>
	<div class="form__radio form__radio--inline">
		<label class="form__radio__label">
			<input type="radio" name="happiness2" class="form__radio__input" value="no" aria-describedby="happiness2" /> No
		</label>
	</div>
</fieldset>
```

### Selects

<div class="fp-example">
	<fieldset class="form__group">
		<label for="themepicker" class="form__label">Pick a theme</label>
		<select name="themepicker" id="themepicker" class="form__field">
			<optgroup label="code">
				<option value="monokia">Monokai</option>
				<option value="">Manni</option>
			</optgroup>
			<optgroup label="events" disabled="disabled">
				<option value="">Xmas</option>
				<option value="">Easter</option>
			</optgroup>
		</select>
	</fieldset>
</div>

```html
<label for="themepicker" class="form__label">Pick a theme</label>
<select name="themepicker" id="themepicker" class="form__field">
	<optgroup label="code">
		<option value="">Monokai</option>
		<option value="">Manni</option>
	</optgroup>
	<optgroup label="events" disabled="disabled">
		<option value="">Xmas</option>
		<option value="">Easter</option>
	</optgroup>
</select>
```

<div class="fp-example">
	<fieldset class="form__group">
		<label for="countrypicker" class="form__label">Select your favorite countries</label>
		<select name="countrypicker" id="countrypicker" class="form__field" multiple="multiple">
			<option value="">Belgium</option>
			<option value="">Netherlands</option>
			<option value="">France</option>
			<option value="">Germany</option>
			<option value="">United Kingdom</option>
			<option value="">Spain</option>
			<option value="">Norway</option>
			<option value="">Luxembourg</option>
			<option value="">Denmark</option>
			<option value="">Sweden</option>
		</select>
	</fieldset>
</div>

```html
<label for="countrypicker" class="form__label">Select your favorite countries</label>
<select name="countrypicker" id="countrypicker" class="form__field" multiple="multiple">
	<option value="">Belgium</option>
	<option value="">Netherlands</option>
	...
</select>
```

## Disabled and readonly states

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab, ipsum.

<div class="fp-example">
	<div class="form__group">
		<label for="disabledinput">Disabled input</label>
		<input type="text" id="disabledinput" class="form__field" disabled="disabled" />
	</div>
	<div class="form__group">
		<label for="readonlyinput">Readonly input</label>
		<input type="text" id="readonlyinput" class="form__field" readonly="readonly" value="Rebels Squad" />
	</div>
	<div class="form__group">
		<div class="form__checkbox">
			<label class="form__checkbox__label">
				<input type="checkbox" class="form__checkbox__input" disabled="disabled" /> Disabled checkbox
			</label>
		</div>
	</div>
	<div class="form__group">
		<div class="form__radio">
			<label class="form__radio__label">
				<input type="radio" class="form__radio__input" disabled="disabled" /> Disabled radio button
			</label>
		</div>
	</div>
</div>

```html
<input type="text" class="form__field" disabled="disabled" />
<input type="text" class="form__field" readonly="readonly" value="Rebels Squad" />
```

## Help text

Sometimes a field needs extra explanation when a `placeholder` and a `label` isn't enough. You can do this with `.form__helptext`.

<div class="fp-example">
	<fieldset class="form__group">
		<label for="telephoneid2" class="form__label">Telephone</label>
		<span class="form__helptext" id="telephonehelptext2">Please add your area code</span>
		<input type="tel" class="form__field" id="telephoneid2" name="telephonename2" placeholder="+3235551234" aria-describedby="telephonehelptext2" />
	</fieldset>
</div>

```html
<label for="telephoneid" class="form__label">Telephone</label>
<span class="form__helptext" id="telephonehelptext">Please add your area code</span>
<input type="tel" class="form__field" id="telephoneid" name="telephonename" placeholder="+3235551234" aria-describedby="telephonehelptext" />
```

<div class="fp-example">
	<fieldset class="form__group">
		<label for="passwordid2" class="form__label">Password</label>
		<span class="form__helptext">Must be at least 8 characters long and contain at least 1 digit and 1 uppercase</span>
		<input type="password" id="passwordid2" name="passwordname2" class="form__field" placeholder="yourS4fePassw0rd" value="MyPassword" minlength="8" />
	</fieldset>
</div>

```html
<label for="passwordid2" class="form__label">Password</label>
<span class="form__helptext">Must be at least 8 characters long and contain at least 1 digit and 1 uppercase</span>
<input type="password" id="passwordid2" name="passwordname2" class="form__field" placeholder="yourS4fePassw0rd" value="MyPassw0rd" minlength="8" />
```

## Validation

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Culpa, officia.

<div class="fp-example">
	<fieldset class="form__group is-valid">
		<label for="requiredinvalidinputid" class="form__label">Name</label>
		<input id="requiredinvalidinputid" name="requiredinvalidinputid" type="text" class="form__field" required="required" />
	</fieldset>

	<fieldset class="form__group is-invalid">
		<label for="requiredinvalidinputid" class="form__label">Name</label>
		<input id="requiredinvalidinputid" name="requiredinvalidinputid" type="text" class="form__field" required="required" />
		<span class="form__feedback">Please enter your name</span>
	</fieldset>
</div>

## Layouting

If you need to layout different fields according a grid pattern, you can use our [grid layout](/layout/grid).

<div class="fp-example">
	<form action="" class="form">
		<fieldset class="form__fieldset">
			<div class="row">
				<div class="col-6">
					<div class="form__group">
						<label for="" class="form__label">First name</label>
						<input type="text" class="form__field" />
					</div>
				</div>
				<div class="col-6">
					<div class="form__group">
						<label for="" class="form__label">Last name</label>
						<input type="text" class="form__field" />
					</div>
				</div>
			</div>
		</fieldset>
		<fieldset class="form__fieldset">
			<div class="row">
				<div class="col-4">
					<div class="form__group">
						<label for="" class="form__label">Address</label>
						<input type="text" class="form__field" />
					</div>
				</div>
				<div class="col-4">
					<div class="form__group">
						<label for="" class="form__label">Zip code</label>
						<input type="text" class="form__field" />
					</div>
				</div>
				<div class="col-4">
					<div class="form__group">
						<label for="" class="form__label">City</label>
						<input type="text" class="form__field" />
					</div>
				</div>
			</div>
		</fieldset>
	</form>
</div>

```html
<fieldset class="form__fieldset">
	<div class="row">
		<div class="col-6">
			<div class="form__group">
				<label for="" class="form__label">First name</label>
				<input type="text" class="form__field" />
			</div>
		</div>
		<div class="col-6">
			<div class="form__group">
				<label for="" class="form__label">Last name</label>
				<input type="text" class="form__field" />
			</div>
		</div>
	</div>
</fieldset>
```

## Special cases

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo ullam distinctio enim in corporis fugit doloremque deleniti debitis ad dolores.

<div class="fp-example">
	<fieldset class="form__fieldset">
		<legend class="form__label">Pick a date</legend>
		<div class="row">
			<div class="col-7">
				<div class="form__group">
					<input type="date" class="form__field" />
				</div>
			</div>
			<div class="col-2">
				<div class="form__joiner-text">at</div>
			</div>
			<div class="col-3">
				<div class="form__group">
					<input type="time" class="form__field" />
				</div>
			</div>
		</div>
	</fieldset>
</div>
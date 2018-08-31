## Fortnite Cube Movement Tracker



Fortnite Cube Movement Timer
<script>
  
  var startTime = 0.25; //5:40
  
  var doneClass = "done"; //optional styling when timer is done
  function startTimer(duration, display) {
    var timer = duration, minutes, seconds;
    var intervalLoop = setInterval(function () {
        minutes = parseInt(timer / 60, 10)
        seconds = parseInt(timer % 60, 10);
        minutes = minutes < 10 ? "0" + minutes : minutes;
        seconds = seconds < 10 ? "0" + seconds : seconds;
		for(var i=0;i<display.length;i++){
          display[i].textContent = minutes + ":" + seconds;
        }
        if (--timer < 0) {
          for(var i=0;i<display.length;i++){
            display[i].classList.add(doneClass);
            display[i].textContent = "DONE";
          }
          clearInterval(intervalLoop);
        }
    	}, 1000);
	}
window.onload = function () {
    var setMinutes = 60 * startTime,
    display = document.querySelectorAll(".timer");
    startTimer(5:00, display);
};
</script>

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/donnellan0007/fortnite-cube/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

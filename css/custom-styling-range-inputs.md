```
input[type='range'] {
    appearance: none; /* Allows for customizations */
    background: transparent;
    width: /* Specific width is required for Firefox */
    height: /* Match the height to the tallest element to keep the
            focus box rectangular */
}

input[type='range']::-moz-range-thumb {
    -webkit-appearance: none;
    /* sTyLe it up */
}

input[type='range']::-webkit-slider-thumb {
    /* StYlE it up */
}

@media (hover: hover) and (pointer: fine) {
    input[type='range']:hover::-moz-range-thumb {
        /* sTyLe it up */
    }

    input[type='range']:hover::-webkit-slider-thumb {
        /* StYlE it up */
    }
}

/* Selects the entire track */
input[type='range']::-moz-range-track {
    /* sTyLe it up */
}

/* Selects the track to the left of the thumb */
input[type='range']::-moz-range-progress {
    /* StYlE it up */
}

/* Chrome only allows you to custom style the full track */
input[type='range']::-webkit-slider-runnable-track {
    width: 100%;
    /* sTyLe it up */
}
```

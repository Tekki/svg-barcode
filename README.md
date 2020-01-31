# NAME

SVG::Barcode - Base class for SVG 1D and 2D codes

# SYNOPSIS

    use SVG::Barcode::Subclass;

    my $plotter = SVG::Barcode::Subclass->new;
    my $svg     = $plotter->plot($text);

    $plotter->foreground;    # black
    $plotter->background;    # white
    $plotter->margin;        # 2
    $plotter->id;
    $plotter->class;
    $plotter->width;
    $plotter->height;
    $plotter->scale;

    %params = (
      foreground => 'red',
      id         => 'barcode',
    );
    $plotter = SVG::Barcode::Subclass->new(%params);

# DESCRIPTION

[SVG::Barcode](https://metacpan.org/pod/SVG%3A%3ABarcode) is a base class for SVG 1D and 2D codes.

You will not use it directly, it will be loaded by its subclasses:

- [SVG::Barcode::Code128](https://metacpan.org/pod/SVG%3A%3ABarcode%3A%3ACode128)
- [SVG::Barcode::DataMatrix](https://metacpan.org/pod/SVG%3A%3ABarcode%3A%3ADataMatrix)
- [SVG::Barcode::QRCode](https://metacpan.org/pod/SVG%3A%3ABarcode%3A%3AQRCode)

# CONSTRUCTOR

## new

    $plotter = SVG::Barcode::Subclass->new;             # create with defaults
    $plotter = SVG::Barcode::Subclass->new(%params);

# METHODS

## plot

    $svg = $plotter->plot($text);

Creates a barcode.

# PARAMETERS

## background

    $value   = $plotter->background;
    $plotter = $plotter->background($newvalue);
    $plotter = $plotter->background('');          # white

Getter and setter for the background color. Default `white`.

## class

    $value   = $plotter->class;
    $plotter = $plotter->class($newvalue);
    $plotter = $plotter->class('');          # ''

Getter and setter for the class of the svg element. Default `''`.

## foreground

    $value   = $plotter->foreground;
    $plotter = $plotter->foreground($newvalue);
    $plotter = $plotter->foreground('');          # black

Getter and setter for the foreground color. Default `black`.

## height

    $value   = $plotter->height;
    $plotter = $plotter->height($newvalue);
    $plotter = $plotter->height('');          # ''

Getter and setter for the height of the svg element. Default `''`.

## id

    $value   = $plotter->id;
    $plotter = $plotter->id($newvalue);
    $plotter = $plotter->id('');          # ''

Getter and setter for the id of the svg element. Default `''`.

## margin

    $value   = $plotter->margin;
    $plotter = $plotter->margin($newvalue);
    $plotter = $plotter->margin('');          # 2

Getter and setter for the margin around the barcode. Default `2`.

## scale

    $value   = $plotter->scale;
    $plotter = $plotter->scale($newvalue);
    $plotter = $plotter->scale('');          # ''

Getter and setter for the scale of the svg element.  Sets ["width"](#width) and ["height"](#height) to products of
the width and height of the graphics.  Used to display small barcodes without blur.  Default `''`.

## width

    $value   = $plotter->width;
    $plotter = $plotter->width($newvalue);
    $plotter = $plotter->width('');          # ''

Getter and setter for the width of the svg element. Default `''`.

# AUTHOR & COPYRIGHT

© 2019–2020 by Tekki (Rolf Stöckli).

This program is free software, you can redistribute it and/or modify it under the terms of the
Artistic License version 2.0.

# SEE ALSO

[SVG::Barcode::Code128](https://metacpan.org/pod/SVG%3A%3ABarcode%3A%3ACode128), [SVG::Barcode::DataMatrix](https://metacpan.org/pod/SVG%3A%3ABarcode%3A%3ADataMatrix), [SVG::Barcode::QRCode](https://metacpan.org/pod/SVG%3A%3ABarcode%3A%3AQRCode).

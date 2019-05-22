# NAME

SVG::Barcode - Base class for SVG 1D and 2D codes

# SYNOPSIS

    my $plotter = SVG::Barcode::Subclass->new(\%params)
    $plotter->param(param_name => 'newvalue');
    my $svg = $plotter->plot($text);

# DESCRIPTION

[SVG::Barcode](https://metacpan.org/pod/SVG::Barcode) is a base class for SVG 1D and 2D codes.

You will not use it directly, it will be loaded by its subclasses:

- [SVG::Barcode::QRCode](https://metacpan.org/pod/SVG::Barcode::QRCode)

# CONSTRUCTOR

## new

    $plotter = SVG::Barcode::Subclass->new(\%params);
    $plotter = SVG::Barcode::Subclass->new;             # create with defaults

# METHODS

## param

    $value = $plotter->param($name);
    $svg   = $plotter->param($name, $newvalue);
    $svg   = $plotter->param($name, '');          # set to default

Getter and setter for the parameters.

## plot

    $svg = $plotter->plot($text);

Creates a QR Code.

# SEE ALSO

[SVG::Barcode::QRCode](https://metacpan.org/pod/SVG::Barcode::QRCode).

# AUTHOR & COPYRIGHT

© 2019 by Tekki (Rolf Stöckli).

This program is free software, you can redistribute it and/or modify it under the terms of the Artistic License version 2.0.

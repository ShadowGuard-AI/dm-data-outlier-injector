![Banner](banner.png)

# dm-data-outlier-injector
Injects statistically plausible outlier data points into numerical columns to distort distributions and mask genuine outliers. Takes number of outliers, column, and standard deviation multiplier as arguments. - Focused on Tools designed to generate or mask sensitive data with realistic-looking but meaningless values

## Install
`git clone https://github.com/ShadowGuardAI/dm-data-outlier-injector`

## Usage
`./dm-data-outlier-injector [params]`

## Parameters
- `-h`: Show help message and exit

## Output path and column spread

The output file must not be the input file. If the resolved output path equals the resolved input path, the run refuses at exit 1 before any write, including when the same file is named through a ./ alias or a symlink.

If the named column has no spread, meaning its standard deviation is zero or undefined (a single row, a constant column, or a non-numeric column), the run exits 1 with an error naming that no outlier can be drawn from a column with no spread, before writing any output.

## License
Copyright (c) ShadowGuardAI

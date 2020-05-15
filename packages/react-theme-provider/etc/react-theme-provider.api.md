## API Report File for "@fluentui/react-theme-provider"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import * as React from 'react';

// @public
export type RecursivePartial<T> = {
    [P in keyof T]?: T[P] extends (infer U)[] ? RecursivePartial<U>[] : T[P] extends object ? RecursivePartial<T[P]> : T[P];
};

// @public
export interface Theme extends RecursivePartial<ThemePrepared> {
}

// @public
export type ThemePlateSet = Partial<{
    fill: ThemeStateSet;
    text: ThemeStateSet;
    subText: ThemeStateSet;
    link: ThemeStateSet;
    divider: ThemeStateSet;
    [key: string]: ThemeStateSet;
}>;

// @public
export interface ThemePrepared {
    // (undocumented)
    stylesheets: string[];
    // (undocumented)
    tokens: {
        body: ThemePlateSet;
        [key: string]: TokenSetType;
    };
}

// @public
export const ThemeProvider: React.ForwardRefExoticComponent<ThemeProviderProps & React.RefAttributes<HTMLDivElement>>;

// @public
export interface ThemeProviderProps extends React.HTMLAttributes<HTMLDivElement> {
    theme?: Theme;
}

// @public
export type ThemeStateSet = Partial<{
    default: string;
    hovered: string;
    pressed: string;
    disabled: string;
    checked: string;
    checkedHovered: string;
    checkedPressed: string;
}> | string;

// @public
export type TokenSetType = string | {
    [key: string]: TokenSetType | undefined;
};

// @public
export const useTheme: () => ThemePrepared;


// (No @packageDocumentation comment for this package)

```
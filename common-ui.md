# Component Documentation

Generated on: 2026-02-03T13:44:03.305Z

---

## Accordion

**File:** `accordion/Accordion.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| customTitle | `Element` | ❌ | - |  |
| accordionType | `enum` | ✅ | - |  |
| textType | `enum` | ❌ | - |  |
| textColor | `enum` | ❌ | - |  |
| titleColor | `enum` | ❌ | - |  |
| expandIcon | `Element` | ❌ | - |  |
| expandIconPosition | `enum` | ❌ | - |  |
| open | `boolean` | ❌ | - |  |
| expanded | `boolean` | ❌ | - | If `true`, expands the accordion, otherwise collapse it. Setting this prop enables control over the accordion. |
| insideForm | `boolean` | ❌ | - |  |
| onToggle | `((id: string, expanded: boolean) =&gt; void)` | ❌ | - |  |
| onSelect | `((event: ChangeEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| actions | `AccordionActionsProps` | ❌ | - |  |
| checkboxSelection | `boolean` | ❌ | - |  |
| checkboxSelectionTestId | `string` | ❌ | - |  |
| customCheckboxIcon | `Element` | ❌ | - |  |
| disableHighlight | `boolean` | ❌ | - |  |
| customDetailsStyle | `CSSProperties` | ❌ | - |  |
| accordionTopStatus | `AccordionTopStatusProps` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## AccordionRenderer

**File:** `list/listItems/renderers/AccordionRenderer.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| icon | `string` | ❌ | - |  |
| accordionTitle | `string` | ❌ | - |  |
| accordionTitleClose | `string` | ❌ | - |  |
| fields | `Record&lt;string, string&gt; \| Record&lt;string, GroupAccordionListItem&gt;` | ✅ | - |  |

---

## Action

**File:** `dataGrid/components/toolbar/Action.tsx`

*No props documented*

---

## ActionPopover

**File:** `ActionPopover/ActionPopover.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| open | `boolean` | ✅ | - |  |
| onClose | `(event: {}, reason: "backdropClick" \| "escapeKeyDown") =&gt; void` | ✅ | - |  |
| anchorEl | `HTMLElement \| null` | ❌ | - |  |
| anchorId | `string` | ❌ | - |  |
| anchorOrigin | `PopoverOrigin` | ❌ | - |  |
| transformOrigin | `PopoverOrigin` | ❌ | - |  |
| title | `ReactNode` | ❌ | - |  |
| description | `ReactNode` | ❌ | - |  |
| value | `string` | ❌ | - |  |
| defaultValue | `string` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLTextAreaElement&gt;) =&gt; void)` | ❌ | - |  |
| onAction | `((value: string) =&gt; void)` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| footerText | `string` | ❌ | - |  |
| footerLinkLabel | `string` | ❌ | - |  |
| footerLinkHref | `string` | ❌ | - |  |
| onFooterLinkClick | `(() =&gt; void)` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| disableAction | `boolean` | ❌ | - |  |
| actionIconName | `string` | ❌ | - |  |
| popoverProps | `Omit&lt;PopoverProps, "open" \| "onClose" \| "anchorEl"&gt;` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## ActionRenderer

**File:** `dataGrid/renderers/actions/actions_view.tsx`

*No props documented*

---

## Announcement

**File:** `announcement/Announcement.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| bg | `any` | ❌ | - |  |
| showCountDown | `boolean` | ❌ | - |  |
| countDownDate | `string \| Date` | ❌ | - |  |
| completeMessage | `string` | ❌ | - |  |
| countDownMarginBottom | `number` | ❌ | - |  |
| marginBottom | `number` | ❌ | - |  |
| backgroundPosition | `enum` | ❌ | - |  |

---

## AreaChart

**File:** `charts/AreaChart/AreaChart.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `WidgetTypes.AREA_CHART` | ✅ | - |  |
| layout | `undefined` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| id | `string` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;Props&gt;[]` | ✅ | - |  |
| legendProps | `any` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| data | `ChartData` | ✅ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## ArrowProgressBar

**File:** `ArrowProgressBar/ArrowProgressBar.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| width | `string` | ❌ | - |  |
| steps | `ProgressStepProps&lt;any&gt;[]` | ✅ | - |  |
| onReorder | `((newOrder: ProgressStepProps&lt;any&gt;[]) =&gt; void)` | ❌ | - |  |
| progressBarType | `enum` | ❌ | - |  |
| style | `CSSProperties` | ❌ | - |  |
| onDelete | `((step: ProgressStepProps&lt;any&gt;) =&gt; void)` | ❌ | - |  |
| onClick | `((stepId: string) =&gt; void)` | ❌ | - |  |
| addStep | `(() =&gt; string \| void)` | ❌ | - |  |
| addStepTooltip | `string` | ❌ | - |  |
| disableAddStep | `boolean` | ❌ | - |  |
| currentStep | `string` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| addStepLabel | `string` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## BadgeField

**File:** `form/components/FieldItem/fields/BadgeField.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| testProps | `any` | ❌ | - |  |
| displayFieldAsError | `boolean` | ❌ | - |  |
| showUpdateFlag | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| value | `any` | ❌ | - |  |
| status | `enum` | ✅ | - |  |
| text | `string` | ✅ | - |  |
| customIcon | `string` | ❌ | - |  |
| size | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| isAccordion | `boolean` | ❌ | - |  |
| moreInfo | `MoreInfoSection[]` | ❌ | - |  |
| defaultExpanded | `boolean` | ❌ | - |  |
| maxVisibleSections | `number` | ❌ | - |  |
| maxVisibleLines | `number` | ❌ | - |  |
| onDismissLink | `LinkProps` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Banner

**File:** `banner/Banner.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| show | `boolean` | ❌ | - | Controls visibility of the banner |
| position | `enum` | ❌ | - | Position of the banner (top or bottom of screen) |
| offset | `number` | ❌ | - | Padding from top or bottom edge in pixels |
| showBillyIcon | `boolean` | ❌ | - | Display Billy icon |
| message | `string \| Element` | ✅ | - | Banner message text |
| showActionLink | `boolean` | ❌ | - | Show "Show me" link |
| actionLinkText | `string` | ❌ | - | Custom text for action link (default: "Show me") |
| onActionClick | `(() =&gt; void)` | ❌ | - | Callback when action link is clicked |
| showCloseButton | `boolean` | ❌ | - | Show close button |
| onClose | `(() =&gt; void)` | ❌ | - | Callback when close button is clicked |
| className | `string` | ❌ | - | Custom className for styling |
| autoDismissAfter | `number` | ❌ | - | Auto-dismiss after specified time in milliseconds |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## BarChart

**File:** `charts/BarChart/BarChart.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `WidgetTypes.BAR_CHART` | ✅ | - |  |
| layout | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| id | `string` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;Props&gt;[]` | ✅ | - |  |
| legendProps | `any` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| data | `ChartData` | ✅ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## BaseChart

**File:** `charts/BaseChart.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;any&gt;[]` | ✅ | - |  |
| legendProps | `any` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| data | `ChartData` | ✅ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## BaseWidget

**File:** `dashboards/components/BaseWidget.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| ref | `any` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| widgetStamp | `string` | ❌ | - |  |
| type | `enum` | ✅ | - |  |
| name | `string` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| titleJSX | `ReactNode` | ❌ | - | Optional custom content rendered directly under the title row. Useful for dynamic KPIs like a bold number summary (e.g., 70). |
| titleTooltip | `TooltipProps` | ❌ | - |  |
| subTitle | `string` | ❌ | - |  |
| rightTitle | `string` | ❌ | - |  |
| widgetFilters | `WidgetFilter&lt;WidgetFiltersProps&gt;[]` | ❌ | - | Deprecated: use `filters` instead |
| filters | `WidgetFilter&lt;WidgetFiltersProps&gt;[] \| { items: WidgetFilter&lt;WidgetFiltersProps&gt;[]; }` | ❌ | - | Widget-level filters (e.g., View By) Supports new object shape with items, and legacy array for backward compatibility. |
| withPreview | `boolean` | ❌ | - |  |
| pending | `boolean` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| orientation | `enum` | ❌ | - |  |
| legendProps | `any` | ❌ | - |  |
| applyFilters | `((params: any) =&gt; void)` | ❌ | - |  |
| onWidgetFilterChange | `((filters: Record&lt;string, any&gt;, current?: { name: string; value: any; }) =&gt; any)` | ❌ | - | Called whenever a widget filter changes. Return partial widget props to re-render (same pattern as `widgetTypes.onChangeType`). |
| showAsTableClick | `((params: any) =&gt; void)` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| widgetTypes | `{ options: ToggleOption[]; value?: string; onChangeType?: ((index: number, value: string) =&gt; any); disabled?: boolean \| undefined; size?: "small" \| "medium" \| "large" \| undefined; fullWidth?: boolean \| undefined; } \| undefined` | ❌ | - | Optional toggle to switch widget types/configurations. When provided, a Toggle will render in the widget header and call onChangeType. |
| autoEnabledCustumization | `boolean` | ❌ | - | Internal flag to suppress edit-mode highlight when auto customization is enabled |
| onWidgetTypeChange | `((widget: any, id: string, value: string) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level onChange handler for widget type changes (only called if widget doesn't have its own onChangeType) |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| data | `KpiBoxData[] \| ChartData \| Props` | ✅ | - |  |
| layout | `enum` | ❌ | - |  |
| groups | `undefined` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[]` | ❌ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |

---

## BillySvgIcon

**File:** `dataGrid/renderers/search/search_tabs_input.tsx`

*No props documented*

---

## BooleanField

**File:** `form/components/FieldItem/fields/BooleanField.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - | Name attribute of the `input` element. |
| label | `string` | ❌ | - |  |
| values | `CheckboxValuesProps[]` | ❌ | - |  |
| themeType | `enum` | ❌ | - |  |
| groupLabel | `string` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. |
| groupRowDirection | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| labelPlacement | `enum` | ❌ | - |  |
| checked | `boolean` | ❌ | - | If `true`, the component is checked. |
| defaultChecked | `boolean` | ❌ | - | The default checked state. Use when the component is not controlled. |
| value | `string \| null` | ❌ | - | The value of the component. The DOM API casts this to a string. The browser uses "on" as the default value. |
| htmlFor | `string` | ❌ | - |  |
| icon | `Element \| null` | ❌ | - | The icon to display when the component is unchecked. |
| checkedIcon | `Element \| null` | ❌ | - | The icon to display when the component is checked. |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - | Callback fired when the state is changed. |
| checkboxGroupTextSize | `enum` | ❌ | - |  |
| testProps | `any` | ❌ | - |  |
| standalone | `boolean` | ❌ | - |  |
| inputProps | `any` | ❌ | - | [Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Attributes) applied to the `input` element. |
| multiLineLabel | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## BooleanRenderer

**File:** `dataGrid/renderers/boolean/boolean_view.tsx`

*No props documented*

---

## BooleanRendererBase

**File:** `dataList/renderers/boolean/boolean_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## Box

**File:** `box/Box.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| title | `string` | ❌ | - |  |
| boxType | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| border | `ResponsiveStyleValue&lt;number \| (string & {}) \| "inset" \| "hidden" \| "-moz-initial" \| "inherit" \| "initial" \| "revert" \| "revert-layer" \| "unset" \| "medium" \| "thick" \| "thin" \| "dashed" \| "dotted" \| ... 184 more ...&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderTop | `ResponsiveStyleValue&lt;BorderTop&lt;string \| number&gt; \| readonly NonNullable&lt;BorderTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderRight | `ResponsiveStyleValue&lt;BorderRight&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderBottom | `ResponsiveStyleValue&lt;BorderBottom&lt;string \| number&gt; \| readonly NonNullable&lt;BorderBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderLeft | `ResponsiveStyleValue&lt;BorderLeft&lt;string \| number&gt; \| readonly NonNullable&lt;BorderLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderColor | `ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt;)` | ❌ | - |  |
| borderRadius | `ResponsiveStyleValue&lt;BorderRadius&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRadius&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| display | `ResponsiveStyleValue&lt;readonly string[] \| Display&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Display&gt;)` | ❌ | - |  |
| displayPrint | `ResponsiveStyleValue&lt;readonly string[] \| Display&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Display&gt;)` | ❌ | - |  |
| overflow | `ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt;)` | ❌ | - |  |
| textOverflow | `ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt;)` | ❌ | - |  |
| visibility | `ResponsiveStyleValue&lt;Visibility \| readonly NonNullable&lt;Visibility&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| whiteSpace | `ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt;)` | ❌ | - |  |
| flexBasis | `ResponsiveStyleValue&lt;FlexBasis&lt;string \| number&gt; \| readonly NonNullable&lt;FlexBasis&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexDirection | `ResponsiveStyleValue&lt;FlexDirection \| readonly NonNullable&lt;FlexDirection&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexWrap | `ResponsiveStyleValue&lt;FlexWrap \| readonly NonNullable&lt;FlexWrap&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| justifyContent | `ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt;)` | ❌ | - |  |
| alignItems | `ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt;)` | ❌ | - |  |
| alignContent | `ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt;)` | ❌ | - |  |
| order | `ResponsiveStyleValue&lt;Order \| readonly NonNullable&lt;Order&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;Order \| readonly NonNullable&lt;...&gt;[] \| undefined&gt;)` | ❌ | - |  |
| flex | `ResponsiveStyleValue&lt;Flex&lt;string \| number&gt; \| readonly NonNullable&lt;Flex&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexGrow | `ResponsiveStyleValue&lt;FlexGrow \| readonly NonNullable&lt;FlexGrow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexShrink | `ResponsiveStyleValue&lt;FlexShrink \| readonly NonNullable&lt;FlexShrink&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| alignSelf | `ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt;)` | ❌ | - |  |
| justifyItems | `ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt;)` | ❌ | - |  |
| justifySelf | `ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt;)` | ❌ | - |  |
| gap | `ResponsiveStyleValue&lt;Gap&lt;string \| number&gt; \| readonly NonNullable&lt;Gap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| columnGap | `ResponsiveStyleValue&lt;ColumnGap&lt;string \| number&gt; \| readonly NonNullable&lt;ColumnGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| rowGap | `ResponsiveStyleValue&lt;RowGap&lt;string \| number&gt; \| readonly NonNullable&lt;RowGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridColumn | `ResponsiveStyleValue&lt;GridColumn \| readonly NonNullable&lt;GridColumn&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridRow | `ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;GridRow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;...&gt;[] \| undefined&gt;)` | ❌ | - |  |
| gridAutoFlow | `ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt;)` | ❌ | - |  |
| gridAutoColumns | `ResponsiveStyleValue&lt;GridAutoColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridAutoRows | `ResponsiveStyleValue&lt;GridAutoRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateColumns | `ResponsiveStyleValue&lt;GridTemplateColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateRows | `ResponsiveStyleValue&lt;GridTemplateRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateAreas | `ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt;)` | ❌ | - |  |
| gridArea | `ResponsiveStyleValue&lt;GridArea \| readonly NonNullable&lt;GridArea&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bgcolor | `ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt;)` | ❌ | - |  |
| color | `ResponsiveStyleValue&lt;readonly string[] \| Color&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Color&gt;)` | ❌ | - |  |
| zIndex | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| position | `ResponsiveStyleValue&lt;Position \| readonly NonNullable&lt;Position&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| top | `ResponsiveStyleValue&lt;Top&lt;string \| number&gt; \| readonly NonNullable&lt;Top&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| right | `ResponsiveStyleValue&lt;Right&lt;string \| number&gt; \| readonly NonNullable&lt;Right&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bottom | `ResponsiveStyleValue&lt;Bottom&lt;string \| number&gt; \| readonly NonNullable&lt;Bottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| left | `ResponsiveStyleValue&lt;Left&lt;string \| number&gt; \| readonly NonNullable&lt;Left&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxShadow | `ResponsiveStyleValue&lt;number \| BoxShadow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;number \| BoxShadow&gt;)` | ❌ | - |  |
| width | `ResponsiveStyleValue&lt;Width&lt;string \| number&gt; \| readonly NonNullable&lt;Width&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxWidth | `ResponsiveStyleValue&lt;MaxWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MaxWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minWidth | `ResponsiveStyleValue&lt;MinWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MinWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| height | `ResponsiveStyleValue&lt;Height&lt;string \| number&gt; \| readonly NonNullable&lt;Height&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxHeight | `ResponsiveStyleValue&lt;MaxHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MaxHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minHeight | `ResponsiveStyleValue&lt;MinHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MinHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxSizing | `ResponsiveStyleValue&lt;BoxSizing \| readonly NonNullable&lt;BoxSizing&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| m | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mt | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mr | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mb | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| ml | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mx | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| my | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| p | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pt | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pr | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pb | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pl | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| px | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| py | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| margin | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginTop | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginRight | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBottom | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginLeft | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginX | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginY | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInline | `ResponsiveStyleValue&lt;MarginInline&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineStart | `ResponsiveStyleValue&lt;MarginInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineEnd | `ResponsiveStyleValue&lt;MarginInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlock | `ResponsiveStyleValue&lt;MarginBlock&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockStart | `ResponsiveStyleValue&lt;MarginBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockEnd | `ResponsiveStyleValue&lt;MarginBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| padding | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingTop | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingRight | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBottom | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingLeft | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingX | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingY | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInline | `ResponsiveStyleValue&lt;PaddingInline&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineStart | `ResponsiveStyleValue&lt;PaddingInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineEnd | `ResponsiveStyleValue&lt;PaddingInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlock | `ResponsiveStyleValue&lt;PaddingBlock&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockStart | `ResponsiveStyleValue&lt;PaddingBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockEnd | `ResponsiveStyleValue&lt;PaddingBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| typography | `ResponsiveStyleValue&lt;string&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string&gt;)` | ❌ | - |  |
| fontFamily | `ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt;)` | ❌ | - |  |
| fontSize | `ResponsiveStyleValue&lt;FontSize&lt;string \| number&gt; \| readonly NonNullable&lt;FontSize&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| fontStyle | `ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt;)` | ❌ | - |  |
| fontWeight | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| letterSpacing | `ResponsiveStyleValue&lt;LetterSpacing&lt;string \| number&gt; \| readonly NonNullable&lt;LetterSpacing&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| lineHeight | `ResponsiveStyleValue&lt;LineHeight&lt;string \| number&gt; \| readonly NonNullable&lt;LineHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| textAlign | `ResponsiveStyleValue&lt;TextAlign \| readonly NonNullable&lt;TextAlign&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| textTransform | `ResponsiveStyleValue&lt;TextTransform \| readonly NonNullable&lt;TextTransform&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |

---

## BubbleTransition

**File:** `tooltip/BubbleTransition.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| ownerState | `TooltipOwnerState` | ❌ | - |  |

---

## BulkEdit

**File:** `dataGrid/components/BulkEdit.tsx`

*No props documented*

---

## BulkEditConflicts

**File:** `dataGrid/components/BulkEditConflicts.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| conflicts | `RowValidationResult[]` | ✅ | - |  |
| conflictingRows | `any[]` | ✅ | - |  |
| totalSelectedRows | `number` | ✅ | - |  |
| validRowsCount | `number` | ✅ | - |  |
| onBack | `() =&gt; void` | ✅ | - |  |
| testIdPrefix | `string` | ❌ | - |  |

---

## Button

**File:** `button/Button.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `ReactNode` | ❌ | - |  |
| onClick | `(event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt; \| undefined) =&gt; any` | ✅ | - |  |
| renderLabel | `ReactNode` | ❌ | - |  |
| withLoader | `boolean` | ❌ | - |  |
| withSelectedRows | `boolean` | ❌ | - |  |
| loaderPosition | `enum` | ❌ | - |  |
| iconButton | `IconProps` | ❌ | - |  |
| customWidth | `number` | ❌ | - |  |
| icon | `IconProps` | ❌ | - |  |
| open | `boolean` | ❌ | - |  |
| progressbar | `boolean` | ❌ | - |  |
| progressbarCount | `number` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| tooltip | `Omit&lt;TooltipProps, "children"&gt;` | ❌ | - |  |
| allowMultiTooltip | `boolean` | ❌ | - |  |
| disableHoverFocus | `boolean` | ❌ | - |  |
| ignoreMobileSizeChange | `boolean` | ❌ | - |  |
| testIdActionName | `string` | ❌ | - |  |
| squared | `boolean` | ❌ | - |  |
| iconAttachedLabel | `boolean` | ❌ | - |  |
| fitWidthToContent | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| buttonType | `enum` | ❌ | - |  |
| buttonSize | `enum` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - | @deprecated Use `loading` instead. |

---

## ButtonGroup

**File:** `buttonGroup/ButtonGroup.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| buttonType | `enum` | ❌ | `primary` |  |
| onClick | `(event: any, data?: any) =&gt; any` | ✅ | - |  |
| onMenuButtonClick | `((event: any, data?: any) =&gt; any)` | ❌ | - |  |
| onClose | `((element: null) =&gt; void)` | ❌ | `() => {}` |  |
| actions | `ButtonGroup[]` | ❌ | - |  |
| params | `any` | ❌ | `{}` |  |
| mainButtonOpenMenu | `boolean` | ❌ | - |  |
| animateIconOnOpen | `boolean` | ❌ | `true` |  |
| fromGrid | `boolean` | ❌ | `false` |  |
| label | `ReactNode` | ❌ | - |  |
| renderLabel | `ReactNode` | ❌ | - |  |
| withLoader | `boolean` | ❌ | - |  |
| withSelectedRows | `boolean` | ❌ | - |  |
| loaderPosition | `enum` | ❌ | - |  |
| iconButton | `IconProps` | ❌ | - |  |
| customWidth | `number` | ❌ | - |  |
| icon | `IconProps` | ❌ | - |  |
| open | `boolean` | ❌ | - |  |
| progressbar | `boolean` | ❌ | - |  |
| progressbarCount | `number` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| tooltip | `Omit&lt;TooltipProps, "children"&gt;` | ❌ | - |  |
| allowMultiTooltip | `boolean` | ❌ | - |  |
| disableHoverFocus | `boolean` | ❌ | - |  |
| ignoreMobileSizeChange | `boolean` | ❌ | - |  |
| testIdActionName | `string` | ❌ | - |  |
| squared | `boolean` | ❌ | `false` |  |
| iconAttachedLabel | `boolean` | ❌ | - |  |
| fitWidthToContent | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| buttonSize | `enum` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - | @deprecated Use `loading` instead. |

---

## Card

**File:** `card/Card.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| title | `string` | ✅ | - |  |
| type | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| description | `string` | ❌ | - |  |
| headerCustomComponent | `ReactNode` | ❌ | - |  |
| content | `ReactNode` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Carousel

**File:** `carousel/Carousel.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| itemSize | `number` | ✅ | - |  |
| buttonStyle | `any` | ❌ | `undefined` |  |

---

## Chart

**File:** `dashboards/widgets/Chart/Chart.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| ref | `any` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| widgetStamp | `string` | ❌ | - |  |
| type | `enum` | ✅ | - |  |
| name | `string` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| titleJSX | `ReactNode` | ❌ | - | Optional custom content rendered directly under the title row. Useful for dynamic KPIs like a bold number summary (e.g., 70). |
| titleTooltip | `TooltipProps` | ❌ | - |  |
| subTitle | `string` | ❌ | - |  |
| rightTitle | `string` | ❌ | - |  |
| widgetFilters | `WidgetFilter&lt;WidgetFiltersProps&gt;[]` | ❌ | - | Deprecated: use `filters` instead |
| filters | `WidgetFilter&lt;WidgetFiltersProps&gt;[] \| { items: WidgetFilter&lt;WidgetFiltersProps&gt;[]; }` | ❌ | - | Widget-level filters (e.g., View By) Supports new object shape with items, and legacy array for backward compatibility. |
| withPreview | `boolean` | ❌ | - |  |
| pending | `boolean` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| orientation | `enum` | ❌ | - |  |
| legendProps | `any` | ❌ | - |  |
| applyFilters | `((params: any) =&gt; void)` | ❌ | - |  |
| onWidgetFilterChange | `((filters: Record&lt;string, any&gt;, current?: { name: string; value: any; }) =&gt; any)` | ❌ | - | Called whenever a widget filter changes. Return partial widget props to re-render (same pattern as `widgetTypes.onChangeType`). |
| showAsTableClick | `((params: any) =&gt; void)` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| widgetTypes | `{ options: ToggleOption[]; value?: string; onChangeType?: ((index: number, value: string) =&gt; any); disabled?: boolean \| undefined; size?: "small" \| "medium" \| "large" \| undefined; fullWidth?: boolean \| undefined; } \| undefined` | ❌ | - | Optional toggle to switch widget types/configurations. When provided, a Toggle will render in the widget header and call onChangeType. |
| autoEnabledCustumization | `boolean` | ❌ | - | Internal flag to suppress edit-mode highlight when auto customization is enabled |
| onWidgetTypeChange | `((widget: any, id: string, value: string) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level onChange handler for widget type changes (only called if widget doesn't have its own onChangeType) |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| data | `KpiBoxData[] \| ChartData \| Props` | ✅ | - |  |
| layout | `enum` | ❌ | - |  |
| groups | `undefined` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[]` | ❌ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |

---

## ChatRenderer

**File:** `list/listItems/renderers/ChatRenderer.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| index | `number` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| user | `string` | ❌ | - |  |
| creationTime | `string \| Date` | ❌ | - |  |
| dateFormat | `string` | ❌ | - |  |
| relativeCreationTime | `string` | ❌ | - |  |
| listItemType | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| header | `string` | ❌ | - |  |
| headerUrl | `string` | ❌ | - |  |
| headerUrlText | `string` | ❌ | - |  |
| body | `string` | ❌ | - |  |
| bodyTooltip | `string` | ❌ | - |  |
| bodyUrl | `string` | ❌ | - |  |
| bodyUrlText | `string` | ❌ | - |  |
| footer | `string` | ❌ | - |  |
| groupId | `string` | ❌ | - |  |
| groupItems | `ListItemProps[]` | ❌ | - |  |
| firstInGroup | `boolean` | ❌ | - |  |
| lastInGroup | `boolean` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| userTooltip | `{ fullName: string; email: string; freeText?: string; }` | ❌ | - |  |
| freeJsxFunc | `(() =&gt; Element \| null)` | ❌ | - |  |
| renderItem | `((list: any) =&gt; Element \| null)` | ❌ | - |  |
| payAttention | `boolean` | ❌ | - |  |
| filterMetaData | `string[]` | ❌ | - |  |
| attachments | `ListItemAttachment[]` | ❌ | - |  |
| data | `ListItemData \| ListItemAttachment[] \| ChatMessage[]` | ❌ | - |  |
| canReplay | `boolean` | ❌ | - |  |
| canUpload | `boolean` | ❌ | - |  |
| fileTypesToUpload | `string[]` | ❌ | - |  |
| textAreaPlaceholder | `string` | ❌ | - |  |
| freeText | `string` | ❌ | - |  |
| onSubmit | `((data: any) =&gt; void)` | ❌ | - |  |
| leaveChat | `(() =&gt; void)` | ❌ | - |  |
| onAddFile | `((file: File) =&gt; Promise&lt;string&gt;)` | ❌ | - |  |
| onRemoveFile | `((file: File) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Checkbox

**File:** `inputs/checkbox/Checkbox.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - | Name attribute of the `input` element. |
| label | `string` | ❌ | - |  |
| values | `CheckboxValuesProps[]` | ❌ | - |  |
| themeType | `enum` | ❌ | - |  |
| groupLabel | `string` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. |
| groupRowDirection | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| labelPlacement | `enum` | ❌ | - |  |
| checked | `boolean` | ❌ | - | If `true`, the component is checked. |
| defaultChecked | `boolean` | ❌ | - | The default checked state. Use when the component is not controlled. |
| value | `string \| null` | ❌ | - | The value of the component. The DOM API casts this to a string. The browser uses "on" as the default value. |
| htmlFor | `string` | ❌ | - |  |
| icon | `Element \| null` | ❌ | - | The icon to display when the component is unchecked. |
| checkedIcon | `Element \| null` | ❌ | - | The icon to display when the component is checked. |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - | Callback fired when the state is changed. |
| checkboxGroupTextSize | `enum` | ❌ | - |  |
| testProps | `any` | ❌ | - |  |
| standalone | `boolean` | ❌ | - |  |
| inputProps | `any` | ❌ | - | [Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Attributes) applied to the `input` element. |
| multiLineLabel | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Colors

**File:** `designSystem/colors/Colors.tsx`

*No props documented*

---

## ColumnSelector

**File:** `dataGrid/components/ColumnSelector.tsx`

*No props documented*

---

## Container

**File:** `layout/Container/Container.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| direction | `enum` | ❌ | - |  |
| alignItems | `enum` | ❌ | - |  |
| justifyContent | `enum` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| flex | `number \| "unset"` | ❌ | - |  |
| style | `CSSProperties` | ❌ | - |  |
| customStyle | `any` | ❌ | - |  |
| gap | `number` | ❌ | - |  |
| onMouseEnter | `((e: any) =&gt; void)` | ❌ | - |  |
| onMouseLeave | `((e: any) =&gt; void)` | ❌ | - |  |
| onClick | `((e: any) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## CopyToClipboard

**File:** `copyToClipboard/CopyToClipboard.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| copyCustomElement | `CopyElement` | ❌ | - |  |
| copyClipboardText | `string \| (() =&gt; string)` | ❌ | - |  |
| decodeUri | `boolean` | ❌ | - |  |
| copyClipBoardTitle | `{ before: string; after: string; }` | ❌ | - |  |
| onCopy | `((value?: any) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Countdown

**File:** `CountDown/Countdown.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| to | `string \| number \| Date` | ❌ | `new Date(2025, 8, 7, 7, 0, 0)` | Target date/time for the countdown. Defaults to September 7, 2025, 07:00 AM. |
| background | `string` | ❌ | - |  |
| showTicket | `boolean` | ❌ | `true` |  |
| ticketImage | `string` | ❌ | - | Optional custom ticket image (PNG, SVG, etc.) to display instead of the default ticket SVG. |
| backgroundVideoUrl | `string` | ❌ | - | Optional YouTube video URL to use as the background instead of an image. |

---

## CountryStateSelect

**File:** `form/components/CountryStateSelect/CountryStatesSelect.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - |  |
| multiple | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| direction | `enum` | ❌ | - |  |
| containerStyles | `CSSProperties` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| country | `CountryProps` | ✅ | - |  |
| state | `StateProps` | ✅ | - |  |
| columnSpacing | `number` | ❌ | - |  |
| rowSpacing | `number` | ❌ | - |  |
| gap | `number` | ❌ | - |  |
| gridLayout | `any` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## CountryStateSelectField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - |  |
| multiple | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| direction | `enum` | ❌ | - |  |
| containerStyles | `CSSProperties` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| country | `CountryProps` | ❌ | - |  |
| state | `StateProps` | ❌ | - |  |
| columnSpacing | `number` | ❌ | - |  |
| rowSpacing | `number` | ❌ | - |  |
| gap | `number` | ❌ | - |  |
| gridLayout | `any` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |
| countryLabel | `string` | ❌ | - |  |
| stateLabel | `string` | ❌ | - |  |
| customCountryStyle | `CSSProperties` | ❌ | - |  |
| customStateStyle | `CSSProperties` | ❌ | - |  |
| customContainerStyles | `CSSProperties` | ❌ | - |  |

---

## CurrencyBasicEditCellRenderer

**File:** `dataGrid/renderers/currency/currency_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## CurrencyEditCellRenderer

**File:** `dataGrid/renderers/currency/currency_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## CurrencyRenderer

**File:** `dataGrid/renderers/currency/currency_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| asValue | `boolean` | ❌ | - |  |
| colDef | `ColumnDef` | ✅ | - |  |

---

## CurrencyRendererBase

**File:** `dataList/renderers/currency/currency_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## CustomDay

**File:** `pickers/components/CustomDay.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| isDisabled | `boolean` | ❌ | - |  |
| isInRange | `boolean` | ❌ | - |  |
| isFirstDay | `boolean` | ❌ | - |  |
| isLastDay | `boolean` | ❌ | - |  |
| disableMargin | `boolean` | ❌ | - | If `true`, days are rendering without margin. Useful for displaying linked range of days. |

---

## CustomJsxField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - |  |
| customJsx | `(form: any, field?: any, meta?: any) =&gt; ReactNode` | ✅ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## CustomLoadingOverlay

**File:** `dataGrid/components/CustomLoader.tsx`

*No props documented*

---

## CustomPagination

**File:** `dataGrid/components/CustomPaging.tsx`

*No props documented*

---

## DashboardHeader

**File:** `dashboards/components/DashboardHeader.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| downloadButton | `any` | ✅ | - |  |
| onResetWidgetsOrder | `() =&gt; void` | ✅ | - |  |
| backButton | `DashboardBackButtonBase` | ❌ | - | Flat header configuration (replaces topSection/bottomSection nesting) |
| title | `string` | ❌ | - | Title displayed on the left side |
| titleTooltip | `TooltipProps` | ❌ | - | Optional tooltip for the title |
| subtitle | `string` | ❌ | - | Optional subtitle under the title |
| infoText | `string` | ❌ | - | Optional informational text displayed on the right (e.g., Last Update) |
| customizeButton | `Omit&lt;ButtonGroupProps, "ref"&gt;` | ❌ | - | "Customize" button group configuration |
| customizeButtonLabel | `string` | ❌ | - | Label for the default customize action |
| autoEnabledCustumization | `boolean` | ❌ | - | When true, edit mode is auto-enabled and only a Reset layout button is shown |
| filters | `DashboardHeaderFilters` | ❌ | - | Filters configuration (callbacks are provided at root-level) |
| headerStamp | `string \| number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Dashboards

**File:** `dashboards/Dashboards.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| header | `HeaderProps` | ✅ | - |  |
| content | `Element` | ❌ | - |  |
| widgets | `Widget[]` | ❌ | - |  |
| widgetsOrder | `WidgetOrder[]` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| onWidgetTypeChange | `((widget: WidgetData, id: string, value: string) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Called when a widget type changes (via widget toggle). Parent should fetch new data and update widgets prop. Dashboard will automatically sync props to internal Redux store. Only triggered if widget doesn't have its own onChangeType handler. |
| onSaveWidgetsOrder | `((order: WidgetOrder[]) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Persist widgets order when in edit mode |
| onWidgetsOrderChange | `((order: WidgetOrder[]) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Fired on every widgets order change (drag end) |
| onHeaderFilterChange | `((filters: Map&lt;string, any&gt;, currentFilter: any) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Header filters change callback |
| onHeaderFilterApply | `((filters: Map&lt;string, any&gt;) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Header filters apply callback |
| onWidgetFilterChange | `((filters: Record&lt;string, any&gt;, current?: { name: string; value: any; }) =&gt; any)` | ❌ | - | Root-level: Widget-level filters change callback (used if widget doesn't provide its own) May return partial widget props to re-render; supports Promise. |
| onResetWidgetsOrder | `(() =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Reset widgets order to default |
| onDownloadPdf | `(() =&gt; void)` | ❌ | - | Root-level: Download PDF action |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |

---

## DataGrid

**File:** `dataGrid/DataGrid.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| gridState | `GridState` | ❌ | - |  |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| storageKey | `string` | ❌ | - |  |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DataList

**File:** `dataList/DataList.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rows | `any[]` | ✅ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| checkboxSelection | `boolean` | ❌ | - |  |
| filterModel | `GridFilterModel` | ❌ | - |  |
| sortModel | `GridSortModel` | ❌ | - |  |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - |  |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - |  |
| onImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| customActions | `GridAction[]` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - |  |
| selectionModel | `string[]` | ❌ | - |  |
| withInlineSearch | `boolean` | ❌ | - |  |
| withFilters | `boolean` | ❌ | - |  |
| withSort | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onSelectionModelChange | `((selectionModel: string[]) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| topNotifications | `DataListTag[]` | ❌ | - |  |
| withoutInlineScroll | `boolean` | ❌ | - |  |
| withImageDownloadTries | `boolean` | ❌ | - |  |
| withSpecialScrollBehavior | `boolean` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| zeroStateType | `enum` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| rowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - |  |
| hideSelectAll | `boolean` | ❌ | - |  |
| isRowSelectable | `((params: any) =&gt; boolean)` | ❌ | - |  |
| dataListCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| canAddNewLine | `boolean` | ❌ | - |  |
| optionalRowsList | `string[]` | ❌ | - | A list of template strings that the user can select from when adding a new line. When provided (and not empty), tapping the "Add new line" action on mobile will first prompt the user to choose between creating an empty line or adding the line from one of these templates. |
| onOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns initial row object when the user selects a template name from optionalRowsList. |
| onEnterEditMode | `((props: { isNewLine?: boolean; rows?: any[]; }) =&gt; void) \| undefined` | ❌ | - |  |
| onRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| setTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| onDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| withEditMode | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DataListEditMode

**File:** `dataList/components/DataListEditMode.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| row | `any` | ✅ | - |  |
| rows | `any[]` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| setEditRowModeProps | `((props: DataListEditModeProps \| null) =&gt; void)` | ❌ | - |  |
| isNewLine | `boolean` | ✅ | - |  |
| setTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| onRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| canEdit | `Boolean` | ✅ | - |  |
| isInsideDialog | `boolean` | ❌ | - |  |
| onSave | `(() =&gt; void)` | ❌ | - |  |
| onDataChanged | `((hasChanged: boolean) =&gt; void)` | ❌ | - |  |

---

## DataListImage

**File:** `dataList/components/DataListImage.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| config | `MobileDataListRowData` | ✅ | - |  |
| onItemImageClick | `() =&gt; void` | ✅ | - |  |
| withImageDownloadTries | `boolean` | ❌ | - |  |

---

## DataListItem

**File:** `dataList/components/DataListItem.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| row | `any` | ✅ | - |  |
| config | `MobileDataListRowData` | ✅ | - |  |
| selectionModel | `any[]` | ❌ | - |  |
| checkboxSelection | `boolean` | ❌ | - |  |
| selectListRow | `((checked: boolean, rowId: string) =&gt; void)` | ❌ | - |  |
| orderedColumns | `ColumnDef[][]` | ✅ | - |  |
| orderedRightColumns | `ColumnDef[][]` | ✅ | - |  |
| columns | `ColumnDef[]` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| onClick | `(() =&gt; void)` | ❌ | - |  |
| withImageDownloadTries | `boolean` | ❌ | - |  |
| onImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| onRowActionsClick | `((row: any, actions: DataListRowAction[]) =&gt; void)` | ❌ | - |  |
| isRowSelectable | `((params: any) =&gt; boolean)` | ❌ | - |  |
| setEditRowModeProps | `((props: DataListEditModeProps \| null) =&gt; void)` | ❌ | - |  |
| onEnterEditMode | `((props: { isNewLine?: boolean; }) =&gt; void)` | ❌ | - |  |
| onDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| withEditMode | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DataListRightMenu

**File:** `dataList/components/DataListRightMenu.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| state | `enum` | ✅ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - |  |
| filterModel | `GridFilterModel` | ❌ | - |  |
| setFilterModel | `((newModel: GridFilterModel) =&gt; void)` | ❌ | - |  |
| sortModel | `GridSortModel` | ❌ | - |  |
| setSortModel | `((newModel: GridSortModel) =&gt; void)` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |

---

## DateBasicEditCellRenderer

**File:** `dataGrid/renderers/date/date_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| showFromNow | `boolean` | ❌ | - |  |
| showLabel | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DateEditCellRenderer

**File:** `dataGrid/renderers/date/date_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| showFromNow | `boolean` | ❌ | - |  |
| showLabel | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DateField

**File:** `form/components/FieldItem/fields/DateField.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| iconType | `string` | ✅ | - |  |
| hidePopupIcon | `boolean` | ✅ | - |  |
| testProps | `any` | ❌ | - |  |
| displayFieldAsError | `boolean` | ❌ | - |  |
| showUpdateFlag | `boolean` | ❌ | - |  |
| name | `string` | ❌ | - | Name attribute used by the `input` element in the Field. |
| inputRef | `any` | ❌ | - | Pass a ref to the `input` element. |
| className | `string` | ❌ | - | Class name applied to the root element. |
| placeholder | `string` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| multiLineLabel | `boolean` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| startRange | `TDate` | ❌ | - |  |
| endRange | `TDate` | ❌ | - |  |
| inputFormat | `enum` | ❌ | - |  |
| displayFormat | `enum` | ❌ | - |  |
| monthAndYearView | `DatePickerView[]` | ❌ | - |  |
| dateFormat | `string` | ❌ | - | Props applied to previous dateFormat is no longer needed. @deprecated Use inputFormat instead. |
| timeSpecific | `string` | ❌ | - |  |
| initialValue | `TDate` | ❌ | - |  |
| monthYearView | `boolean` | ❌ | - |  |
| disableWeekends | `boolean` | ❌ | - |  |
| holidays | `TDate[]` | ❌ | - |  |
| enablePast | `boolean` | ❌ | - |  |
| disableFuture | `boolean` | ❌ | - | If `true`, disable values after the current date for date components, time for time components and both for date time components. |
| disableCloseOnSelect | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| startOrEndOfTheMonth | `enum` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| mask | `string` | ❌ | - | Props applied to input text element. @deprecated sending mask is no longer needed. |
| shortYear | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| popperRef | `any` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isFilter | `boolean` | ❌ | - |  |
| skipPickerButtonOnFocus | `boolean` | ❌ | - |  |
| hidePickerIcon | `boolean` | ❌ | - |  |
| shouldDisableDate | `((date: Date \| null) =&gt; boolean)` | ❌ | - |  |
| onChange | `(date: Date, keyboardInputValue?: string \| undefined) =&gt; void` | ✅ | - |  |
| onError | `((reason: string, value: string) =&gt; void)` | ❌ | - |  |
| onApply | `((value: Date) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onOpen | `(() =&gt; void)` | ❌ | - | Callback fired when the popup requests to be opened. Use in controlled mode (see `open`). |
| onClose | `((value?: TDate) =&gt; void)` | ❌ | - |  |
| onAccept | `((value: TDate) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onEnter | `((value: TDate) =&gt; void)` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| pickerType | `enum` | ❌ | - |  |
| pickerSize | `enum` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| inlineLabel | `Element` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DateFilter

**File:** `dataGrid/filters/date_filter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| filterRef | `MutableRefObject&lt;any&gt;` | ❌ | - |  |
| customFieldName | `string` | ✅ | - |  |
| filterType | `enum` | ✅ | - |  |
| pinned | `boolean` | ❌ | - |  |
| freeText | `boolean` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| id | `string` | ✅ | - |  |
| type | `string` | ❌ | - |  |
| apiRef | `any` | ✅ | - |  |
| label | `string` | ✅ | - |  |
| field | `string` | ✅ | - | The column identifier. It's used to map with [[GridRowModel]] values. |
| rows | `any` | ✅ | - |  |
| columns | `any` | ✅ | - |  |
| options | `SelectOption[]` | ❌ | - |  |
| getOptions | `(() =&gt; Promise&lt;any&gt;)` | ❌ | - |  |
| filterProps | `any` | ✅ | - |  |
| filterModel | `any` | ✅ | - |  |
| triggerOnChange | `boolean` | ❌ | - |  |
| onFilterChanged | `((filterModel: GridFilterModel, inputEl?: HTMLInputElement \| null) =&gt; void)` | ❌ | - |  |
| getFilterModel | `() =&gt; any` | ✅ | - |  |
| quickFilter | `QuickFiltersConfig` | ❌ | - |  |
| iconProps | `IconProps` | ❌ | - |  |
| headerProps | `HeaderProps` | ❌ | - |  |
| dateProps | `DateProps` | ❌ | - |  |
| selectProps | `GridSelectProps` | ❌ | - |  |
| textProps | `TextProps` | ❌ | - |  |
| numberProps | `NumberProps` | ❌ | - |  |
| currencyProps | `CurrencyProps` | ❌ | - |  |
| linkProps | `LinkProps` | ❌ | - |  |
| getter | `enum` | ❌ | - |  |
| ignoreCellClick | `boolean` | ❌ | - |  |
| isFirst | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| boldText | `boolean` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| autoGeneratedOptions | `boolean` | ❌ | - |  |
| popper | `Element` | ❌ | - |  |
| badge | `boolean` | ❌ | - |  |
| tooltip | `boolean` | ❌ | - |  |
| inputAutoEvents | `InputAutoEvents` | ❌ | - |  |
| searchFilter | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| visible | `boolean` | ❌ | - |  |
| hideIfEmpty | `boolean` | ❌ | - |  |
| hideOnMobile | `boolean` | ❌ | - |  |
| mobile | `ColumnMobileConfig` | ❌ | - |  |
| allowBulkEdit | `boolean` | ❌ | - |  |
| onClick | `((row: any, params?: any) =&gt; void)` | ❌ | - |  |
| onChange | `((row: any, props: any, apiRef: any) =&gt; void)` | ❌ | - |  |
| validateInput | `((props: any) =&gt; ValidationResult)` | ❌ | - |  |
| preProcessProps | `((props: any) =&gt; any)` | ❌ | - |  |
| searchProps | `{ columnsToHide?: string[]; renderCellContent?: ((params: any) =&gt; Element); commitRowChange?: ((params: any) =&gt; void) \| undefined; onChangeText?: ((search: string, params?: { ...; } \| undefined) =&gt; Promise&lt;...&gt;) \| undefined; renderFooter?: ((row: any) =&gt; any) \| undefined; } \| undefined` | ❌ | - |  |

---

## DatePicker

**File:** `pickers/datePicker/DatePicker.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - | Name attribute used by the `input` element in the Field. |
| inputRef | `any` | ❌ | - | Pass a ref to the `input` element. |
| className | `string` | ❌ | - | Class name applied to the root element. |
| placeholder | `string` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| multiLineLabel | `boolean` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| startRange | `TDate` | ❌ | - |  |
| endRange | `TDate` | ❌ | - |  |
| inputFormat | `enum` | ❌ | - |  |
| displayFormat | `enum` | ❌ | - |  |
| monthAndYearView | `DatePickerView[]` | ❌ | - |  |
| dateFormat | `string` | ❌ | - | Props applied to previous dateFormat is no longer needed. @deprecated Use inputFormat instead. |
| timeSpecific | `string` | ❌ | - |  |
| initialValue | `TDate` | ❌ | - |  |
| monthYearView | `boolean` | ❌ | - |  |
| disableWeekends | `boolean` | ❌ | - |  |
| holidays | `TDate[]` | ❌ | - |  |
| enablePast | `boolean` | ❌ | - |  |
| disableFuture | `boolean` | ❌ | - | If `true`, disable values after the current date for date components, time for time components and both for date time components. |
| disableCloseOnSelect | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| startOrEndOfTheMonth | `enum` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| mask | `string` | ❌ | - | Props applied to input text element. @deprecated sending mask is no longer needed. |
| shortYear | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| popperRef | `any` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isFilter | `boolean` | ❌ | - |  |
| skipPickerButtonOnFocus | `boolean` | ❌ | - |  |
| hidePickerIcon | `boolean` | ❌ | - |  |
| shouldDisableDate | `((date: Date \| null) =&gt; boolean)` | ❌ | - |  |
| onChange | `(date: Date, keyboardInputValue?: string \| undefined) =&gt; void` | ✅ | - |  |
| onError | `((reason: string, value: string) =&gt; void)` | ❌ | - |  |
| onApply | `((value: Date) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onOpen | `(() =&gt; void)` | ❌ | - | Callback fired when the popup requests to be opened. Use in controlled mode (see `open`). |
| onClose | `((value?: TDate) =&gt; void)` | ❌ | - |  |
| onAccept | `((value: TDate) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onEnter | `((value: TDate) =&gt; void)` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| pickerType | `enum` | ❌ | - |  |
| pickerSize | `enum` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| inlineLabel | `Element` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DateRangeFilterBase

**File:** `pickers/datePicker/DateRangeFilterBase.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| DateRangeComponent | `any` | ❌ | - | The DateRangeSingleInput component to render |
| startRange | `Date \| null` | ❌ | - | Start date value |
| endRange | `Date \| null` | ❌ | - | End date value |
| onChange | `(value: DateRange&lt;Dayjs&gt;, validationError: any) =&gt; void` | ✅ | - | Callback when value changes |
| onAccept | `((value: DateRange&lt;Dayjs&gt;) =&gt; void)` | ❌ | - | Callback when dates are accepted/applied |
| onClear | `(() =&gt; void)` | ❌ | - | Callback when cleared |
| label | `string` | ✅ | - | Label for the filter |
| field | `string` | ✅ | - | Field name |
| dateRangeProps | `any` | ❌ | - | Props to pass to the DateRangeSingleInput component |
| testIdPrefix | `string` | ❌ | - | Test ID prefix |
| filterType | `string` | ❌ | - | Filter type for width computation |
| isFiltered | `boolean` | ❌ | - | Is this filter currently active/filtered |
| inputFormat | `string` | ❌ | - | Input format for dates |

---

## DateRangeSingleInput

**File:** `pickers/datePicker/DateRangeSingleInput.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onError | `((reason: string, value: string) =&gt; void)` | ❌ | - |  |
| shouldDisableDate | `((date: Date \| null) =&gt; boolean)` | ❌ | - |  |
| onClose | `((value?: TDate) =&gt; void)` | ❌ | - |  |
| onAccept | `((value: TDate) =&gt; void)` | ❌ | - |  |
| disableFuture | `boolean` | ❌ | - | If `true`, disable values after the current date for date components, time for time components and both for date time components. |
| className | `string` | ❌ | - | Class name applied to the root element. |
| readOnly | `boolean` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| inputRef | `any` | ❌ | - | Pass a ref to the `input` element. |
| name | `string` | ❌ | - | Name attribute used by the `input` element in the Field. |
| onOpen | `(() =&gt; void)` | ❌ | - | Callback fired when the popup requests to be opened. Use in controlled mode (see `open`). |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| startRange | `TDate` | ❌ | - |  |
| endRange | `TDate` | ❌ | - |  |
| inputFormat | `enum` | ❌ | - |  |
| displayFormat | `enum` | ❌ | - |  |
| dateFormat | `string` | ❌ | - | Props applied to previous dateFormat is no longer needed. @deprecated Use inputFormat instead. |
| disableWeekends | `boolean` | ❌ | - |  |
| holidays | `TDate[]` | ❌ | - |  |
| enablePast | `boolean` | ❌ | - |  |
| disableCloseOnSelect | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| startOrEndOfTheMonth | `enum` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| mask | `string` | ❌ | - | Props applied to input text element. @deprecated sending mask is no longer needed. |
| shortYear | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| popperRef | `any` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| isFilter | `boolean` | ❌ | - |  |
| skipPickerButtonOnFocus | `boolean` | ❌ | - |  |
| hidePickerIcon | `boolean` | ❌ | - |  |
| onApply | `((value: Date) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onEnter | `((value: TDate) =&gt; void)` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| pickerSize | `enum` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| inlineLabel | `Element` | ❌ | - |  |
| onChange | `(value: DateRange&lt;Dayjs&gt;, validationError: any) =&gt; void` | ✅ | - |  |

---

## DateRenderer

**File:** `dataGrid/renderers/date/date_view.tsx`

*No props documented*

---

## DateRendererBase

**File:** `dataList/renderers/date/date_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## DateTimePicker

**File:** `pickers/dateTimePicker/DateTimePicker.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - | Name attribute used by the `input` element in the Field. |
| inputRef | `any` | ❌ | - | Pass a ref to the `input` element. |
| className | `string` | ❌ | - | Class name applied to the root element. |
| placeholder | `string` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| multiLineLabel | `boolean` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| startRange | `TDate` | ❌ | - |  |
| endRange | `TDate` | ❌ | - |  |
| inputFormat | `enum` | ❌ | - |  |
| displayFormat | `enum` | ❌ | - |  |
| monthAndYearView | `DatePickerView[]` | ❌ | - |  |
| dateFormat | `string` | ❌ | - | Props applied to previous dateFormat is no longer needed. @deprecated Use inputFormat instead. |
| timeSpecific | `string` | ❌ | - |  |
| initialValue | `TDate` | ❌ | - |  |
| monthYearView | `boolean` | ❌ | - |  |
| disableWeekends | `boolean` | ❌ | - |  |
| holidays | `TDate[]` | ❌ | - |  |
| enablePast | `boolean` | ❌ | - |  |
| disableFuture | `boolean` | ❌ | - | If `true`, disable values after the current date for date components, time for time components and both for date time components. |
| disableCloseOnSelect | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| startOrEndOfTheMonth | `enum` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| mask | `string` | ❌ | - | Props applied to input text element. @deprecated sending mask is no longer needed. |
| shortYear | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| popperRef | `any` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isFilter | `boolean` | ❌ | - |  |
| skipPickerButtonOnFocus | `boolean` | ❌ | - |  |
| hidePickerIcon | `boolean` | ❌ | - |  |
| shouldDisableDate | `((date: Date \| null) =&gt; boolean)` | ❌ | - |  |
| onChange | `(date: Date, keyboardInputValue?: string \| undefined) =&gt; void` | ✅ | - |  |
| onError | `((reason: string, value: string) =&gt; void)` | ❌ | - |  |
| onApply | `((value: Date) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onOpen | `(() =&gt; void)` | ❌ | - | Callback fired when the popup requests to be opened. Use in controlled mode (see `open`). |
| onClose | `((value?: TDate) =&gt; void)` | ❌ | - |  |
| onAccept | `((value: TDate) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onEnter | `((value: TDate) =&gt; void)` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| pickerType | `enum` | ❌ | - |  |
| pickerSize | `enum` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| inlineLabel | `Element` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DefaultListItem

**File:** `list/listItems/DefaultListItem.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| index | `number` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| user | `string` | ❌ | - |  |
| creationTime | `string \| Date` | ❌ | - |  |
| dateFormat | `string` | ❌ | - |  |
| relativeCreationTime | `string` | ❌ | - |  |
| listItemType | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| header | `string` | ❌ | - |  |
| headerUrl | `string` | ❌ | - |  |
| headerUrlText | `string` | ❌ | - |  |
| body | `string` | ❌ | - |  |
| bodyTooltip | `string` | ❌ | - |  |
| bodyUrl | `string` | ❌ | - |  |
| bodyUrlText | `string` | ❌ | - |  |
| footer | `string` | ❌ | - |  |
| groupId | `string` | ❌ | - |  |
| groupItems | `ListItemProps[]` | ❌ | - |  |
| firstInGroup | `boolean` | ❌ | - |  |
| lastInGroup | `boolean` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| userTooltip | `{ fullName: string; email: string; freeText?: string; }` | ❌ | - |  |
| freeJsxFunc | `(() =&gt; Element \| null)` | ❌ | - |  |
| renderItem | `((list: any) =&gt; Element \| null)` | ❌ | - |  |
| payAttention | `boolean` | ❌ | - |  |
| filterMetaData | `string[]` | ❌ | - |  |
| attachments | `ListItemAttachment[]` | ❌ | - |  |
| data | `ListItemData \| ListItemAttachment[] \| ChatMessage[]` | ❌ | - |  |
| canReplay | `boolean` | ❌ | - |  |
| canUpload | `boolean` | ❌ | - |  |
| fileTypesToUpload | `string[]` | ❌ | - |  |
| textAreaPlaceholder | `string` | ❌ | - |  |
| freeText | `string` | ❌ | - |  |
| onSubmit | `((data: any) =&gt; void)` | ❌ | - |  |
| leaveChat | `(() =&gt; void)` | ❌ | - |  |
| onAddFile | `((file: File) =&gt; Promise&lt;string&gt;)` | ❌ | - |  |
| onRemoveFile | `((file: File) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DelayedImage

**File:** `mobile/delayedImage/DelayedImage.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| primaryImageUrl | `string` | ❌ | - |  |
| secondaryImageUrl | `string \| null` | ❌ | - |  |
| isWithImageDownloadTries | `boolean` | ❌ | - |  |
| loadingJSXElement | `Element` | ❌ | - |  |
| betweenChecksPeriod | `number` | ❌ | - |  |
| checkTriesNumber | `number` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |

---

## DeleteRenderer

**File:** `dataGrid/renderers/delete/delete_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| tooltipText | `any` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;any&gt;)` | ❌ | - |  |
| isUsingCheckbox | `boolean` | ✅ | - |  |
| isCheckboxChecked | `boolean` | ✅ | - |  |
| onChecked | `(isChecked: boolean) =&gt; void` | ✅ | - |  |

---

## Dialog

**File:** `dialog/Dialog.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| open | `boolean` | ✅ | - | If `true`, the component is shown. |
| type | `enum` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| titleProps | `Omit&lt;TextProps, "children" \| "ref"&gt;` | ❌ | - |  |
| titlePosition | `enum` | ❌ | - |  |
| subTitle | `string` | ❌ | - |  |
| content | `any` | ❌ | - |  |
| buttons | `DialogButtonsProps` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| minWidth | `number` | ❌ | - |  |
| minHeight | `number` | ❌ | - |  |
| maxHeight | `number` | ❌ | - |  |
| maxWidth | `number` | ❌ | - |  |
| contentAlignment | `enum` | ❌ | - |  |
| onClose | `((event?: Event, reason?: "backdropClick" \| "escapeKeyDown") =&gt; void) \| undefined` | ❌ | - |  |
| onCloseCb | `(() =&gt; void)` | ❌ | - |  |
| onSave | `(() =&gt; void)` | ❌ | - |  |
| onReject | `(() =&gt; void)` | ❌ | - |  |
| closeOnBackDropClick | `boolean` | ❌ | - |  |
| disableCloseButton | `boolean` | ❌ | - |  |
| legacyUI | `boolean` | ❌ | - |  |
| bgImage | `string` | ❌ | - |  |
| mobileTopGap | `number` | ❌ | - |  |
| customStyleDialogContent | `CSSProperties` | ❌ | - |  |
| drawerProps | `Omit&lt;DrawerProps, "dir"&gt;` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DialogFooter

**File:** `dialog/DialogFooter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| buttons | `DialogButtonsProps` | ❌ | - |  |
| legacyUI | `boolean` | ❌ | - |  |

---

## DialogHeader

**File:** `dialog/DialogHeader.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `enum` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| titleProps | `Omit&lt;TextProps, "children" \| "ref"&gt;` | ❌ | - |  |
| titlePosition | `enum` | ✅ | - |  |
| onClose | `((event: Event, reason: "backdropClick" \| "escapeKeyDown") =&gt; void)` | ❌ | - |  |
| disableCloseButton | `boolean` | ❌ | - |  |
| shouldDisplayBoxShadow | `boolean` | ✅ | - |  |
| legacyUI | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DownloadButton

**File:** `dashboards/components/DownloadButton.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| fileName | `string` | ✅ | - |  |
| onDownloadPdf | `(() =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Drawer

**File:** `drawer/Drawer.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| anchorElement | `string` | ❌ | - |  |
| topPosition | `number` | ❌ | - |  |
| open | `boolean` | ✅ | - | If `true`, the component is shown. |
| icon | `IconProps` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| titleColor | `enum` | ❌ | - |  |
| subtitle | `string` | ❌ | - |  |
| buttonBar | `ButtonProps[]` | ❌ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - | Callback fired when the component requests to be closed. The `reason` parameter can optionally be used to control the response to `onClose`. |
| minWidth | `number` | ❌ | - |  |
| maxWidth | `number` | ❌ | - |  |
| style | `CSSProperties` | ❌ | - |  |
| customHeader | `{ header?: Element; buttons?: ButtonProps[]; } \| undefined` | ❌ | - |  |
| contentStyle | `CSSProperties` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## DrawerPageWithPush

**File:** `drawer/DrawerPageWithPush.tsx`

*No props documented*

---

## Elements

**File:** `dataGrid/components/toolbar/Elements.tsx`

*No props documented*

---

## EmojiPicker

**File:** `list/listItems/renderers/EmojiPicker.tsx`

*No props documented*

---

## Expenses

**File:** `dataGrid/mocks/Expenses.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## FeedListItem

**File:** `list/listItems/FeedListItem.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| index | `number` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| user | `string` | ❌ | - |  |
| creationTime | `string \| Date` | ❌ | - |  |
| dateFormat | `string` | ❌ | - |  |
| relativeCreationTime | `string` | ❌ | - |  |
| listItemType | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| header | `string` | ❌ | - |  |
| headerUrl | `string` | ❌ | - |  |
| headerUrlText | `string` | ❌ | - |  |
| body | `string` | ❌ | - |  |
| bodyTooltip | `string` | ❌ | - |  |
| bodyUrl | `string` | ❌ | - |  |
| bodyUrlText | `string` | ❌ | - |  |
| footer | `string` | ❌ | - |  |
| groupId | `string` | ❌ | - |  |
| groupItems | `ListItemProps[]` | ❌ | - |  |
| firstInGroup | `boolean` | ❌ | - |  |
| lastInGroup | `boolean` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| userTooltip | `{ fullName: string; email: string; freeText?: string; }` | ❌ | - |  |
| freeJsxFunc | `(() =&gt; Element \| null)` | ❌ | - |  |
| renderItem | `((list: any) =&gt; Element \| null)` | ❌ | - |  |
| payAttention | `boolean` | ❌ | - |  |
| filterMetaData | `string[]` | ❌ | - |  |
| attachments | `ListItemAttachment[]` | ❌ | - |  |
| data | `ListItemData \| ListItemAttachment[] \| ChatMessage[]` | ❌ | - |  |
| canReplay | `boolean` | ❌ | - |  |
| canUpload | `boolean` | ❌ | - |  |
| fileTypesToUpload | `string[]` | ❌ | - |  |
| textAreaPlaceholder | `string` | ❌ | - |  |
| freeText | `string` | ❌ | - |  |
| onSubmit | `((data: any) =&gt; void)` | ❌ | - |  |
| leaveChat | `(() =&gt; void)` | ❌ | - |  |
| onAddFile | `((file: File) =&gt; Promise&lt;string&gt;)` | ❌ | - |  |
| onRemoveFile | `((file: File) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## FieldItem

**File:** `form/components/FieldItem/FieldItem.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `enum` | ✅ | - |  |
| fieldProps | `TextFieldProps \| CheckboxProps \| ObjectFieldProps \| VendorFieldProps \| SelectFieldProps \| DateFieldProps \| AttachmentFieldProps \| BadgeFieldProps` | ✅ | - |  |
| labelMaxWidth | `number` | ❌ | - |  |
| fieldWidthDistribution | `{ label: string; field: string; }` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| value | `string` | ❌ | - |  |
| label | `string` | ✅ | - |  |
| info | `string` | ❌ | - |  |
| isChildForm | `boolean` | ❌ | - |  |
| errorFields | `ErrorField` | ❌ | - |  |
| warningFields | `WarningField` | ❌ | - |  |
| updatedFields | `UpdatedField` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| fieldRef | `((ref: any) =&gt; void)` | ❌ | - |  |

---

## FieldItemFormDemo

**File:** `form/components/FieldItem/FieldItemFormDemo.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| formRef | `RefObject&lt;any&gt;` | ❌ | - |  |
| formFields | `FormFields` | ✅ | - |  |
| errorFields | `ErrorField` | ❌ | - |  |
| warningFields | `WarningField` | ❌ | - |  |
| updatedFields | `UpdatedField` | ❌ | - |  |
| isChildForm | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| onChange | `(values: FieldValues) =&gt; void` | ✅ | - |  |
| placeholder | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| labelMaxWidth | `number` | ❌ | - |  |
| wrapSectionWithAccordion | `boolean` | ❌ | - |  |

---

## FieldItemsForm

**File:** `form/components/FieldItem/FieldItemsForm.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| formRef | `RefObject&lt;any&gt;` | ❌ | - |  |
| formFields | `FormFields` | ✅ | - |  |
| errorFields | `ErrorField` | ❌ | - |  |
| warningFields | `WarningField` | ❌ | - |  |
| updatedFields | `UpdatedField` | ❌ | - |  |
| isChildForm | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| onChange | `(values: FieldValues) =&gt; void` | ✅ | - |  |
| placeholder | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| labelMaxWidth | `number` | ❌ | - |  |
| wrapSectionWithAccordion | `boolean` | ❌ | - |  |

---

## FieldLabel

**File:** `form/components/FieldItem/FieldLabel.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `enum` | ✅ | - |  |
| requiredField | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| label | `string` | ✅ | - |  |
| info | `string \| Element` | ❌ | - |  |
| errors | `string[]` | ✅ | - |  |
| warnings | `string[]` | ✅ | - |  |
| isChildForm | `boolean` | ❌ | - |  |
| testProps | `any` | ❌ | - |  |
| $isUpdated | `boolean` | ❌ | - |  |

---

## FileLine

**File:** `inputs/file/FileLine.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| index | `number` | ✅ | - |  |
| acceptedFileTypes | `string[]` | ✅ | - |  |
| onDeleteFile | `((index: number) =&gt; void)` | ❌ | - |  |
| onDownloadFile | `((index: number) =&gt; void)` | ❌ | - |  |
| onUploadFile | `(uploadFile: FileDocument, setProgress?: any, controller?: any) =&gt; Promise&lt;any&gt;` | ✅ | - |  |
| onUploadFinish | `() =&gt; void` | ✅ | - |  |
| onError | `((errors: FileRejection[]) =&gt; void)` | ❌ | - |  |
| uploadFiles | `FileDocument[]` | ✅ | - |  |
| dateFormat | `string` | ❌ | - |  |
| disableDownload | `boolean` | ❌ | - |  |
| disableDelete | `boolean` | ❌ | - |  |

---

## FileUploader

**File:** `inputs/file/FileUploader.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| name | `string` | ❌ | - |  |
| label | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| maxSize | `number` | ❌ | - |  |
| acceptedFileTypes | `string[]` | ❌ | - |  |
| allowDuplicates | `boolean` | ❌ | - |  |
| onUploadStart | `(() =&gt; void)` | ❌ | - |  |
| onUploadFile | `(uploadFile: FileDocument, setProgress?: any, controller?: any) =&gt; Promise&lt;any&gt;` | ✅ | - |  |
| onDeleteFile | `((fileToRemove: FileDocument) =&gt; void)` | ❌ | - |  |
| onDownloadFile | `((index: number) =&gt; void)` | ❌ | - |  |
| onUploadFinish | `((files?: (FileDocument)[]) =&gt; void) \| undefined` | ❌ | - |  |
| onError | `((errors: FileRejection[]) =&gt; void)` | ❌ | - |  |
| dateFormat | `string` | ❌ | - |  |
| maxFiles | `number` | ❌ | - |  |
| files | `BaseFileDocument[]` | ❌ | - |  |
| disableDownload | `boolean` | ❌ | - |  |
| disableDelete | `boolean` | ❌ | - |  |
| hasError | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## FilterErrorBoundary

**File:** `dataGrid/components/filters/FilterErrorBoundary.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| fallback | `ReactNode` | ❌ | - |  |
| onError | `((error: Error, errorInfo: ErrorInfo) =&gt; void)` | ❌ | - |  |

---

## Footer

**File:** `pickers/components/Footer.tsx`

*No props documented*

---

## ForMyAttensionTemplate

ForMyAttension Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Form

**File:** `form/Form.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| formStyle | `CSSProperties` | ❌ | - |  |
| getInputsRefs | `((inputsRefs: any) =&gt; void)` | ❌ | - |  |
| onChange | `((element: any, inputsRefs?: any, formikForm?: any) =&gt; void)` | ❌ | - |  |
| formSchemaSections | `FormSchemaSection[]` | ✅ | - |  |
| onSubmit | `(values: FormikValues, formikHelpers?: FormikHelpers&lt;FormikValues&gt; \| undefined) =&gt; void \| Promise&lt;any&gt;` | ✅ | - | Submission handler |
| footer | `FormFooterProps` | ❌ | - |  |
| customSchema | `any` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| validate | `((values: FormikValues, refs?: any) =&gt; void \| object \| Promise&lt;FormikErrors&lt;FormikValues&gt;&gt;)` | ❌ | - | Validation function. Must return an error object or promise that throws an error object where that object keys map to corresponding value. |
| gridDirection | `enum` | ❌ | - |  |
| numberOfSkeletonFields | `number` | ❌ | - |  |
| formError | `boolean` | ❌ | - |  |
| fieldsWrapperStyle | `CSSProperties` | ❌ | - |  |
| variation | `enum` | ❌ | - |  |
| boxProps | `BoxProps` | ❌ | - |  |
| asWizard | `boolean` | ❌ | - |  |
| wizardProps | `{ asTabs?: boolean; tabsProps?: Partial&lt;TabsProps&gt;; currentStep?: number \| undefined; onStepChange?: ((step: number) =&gt; void) \| undefined; withStepper?: boolean \| undefined; } \| undefined` | ❌ | - |  |

---

## FormArrayField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - |  |
| arrayObject | `FormElementSchema[]` | ✅ | - |  |
| arrayHelpers | `FormikArrayHelper[]` | ❌ | - |  |
| helpersContainerStyle | `CSSProperties` | ❌ | - |  |
| direction | `enum` | ❌ | - |  |
| elementsWrapperDirection | `enum` | ❌ | - |  |
| elementsWrapperStyle | `CSSProperties` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## FormCheckboxField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - | Name attribute of the `input` element. |
| label | `string` | ❌ | - |  |
| values | `CheckboxValuesProps[]` | ❌ | - |  |
| themeType | `enum` | ❌ | - |  |
| groupLabel | `string` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. |
| groupRowDirection | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| labelPlacement | `enum` | ❌ | - |  |
| checked | `boolean` | ❌ | - | If `true`, the component is checked. |
| defaultChecked | `boolean` | ❌ | - | The default checked state. Use when the component is not controlled. |
| value | `string \| null` | ❌ | - | The value of the component. The DOM API casts this to a string. The browser uses "on" as the default value. |
| htmlFor | `string` | ❌ | - |  |
| icon | `Element \| null` | ❌ | - | The icon to display when the component is unchecked. |
| checkedIcon | `Element \| null` | ❌ | - | The icon to display when the component is checked. |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - | Callback fired when the state is changed. |
| checkboxGroupTextSize | `enum` | ❌ | - |  |
| testProps | `any` | ❌ | - |  |
| standalone | `boolean` | ❌ | - |  |
| inputProps | `any` | ❌ | - | [Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Attributes) applied to the `input` element. |
| multiLineLabel | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## FormControl

**File:** `form/components/FormControl.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| spacing | `string` | ❌ | - |  |
| flexDirection | `enum` | ❌ | - |  |

---

## FormControlsRenderer

**File:** `form/components/FormControlsRenderer.tsx`

*No props documented*

---

## FormDateField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - | Name attribute used by the `input` element in the Field. |
| inputRef | `any` | ❌ | - | Pass a ref to the `input` element. |
| className | `string` | ❌ | - | Class name applied to the root element. |
| placeholder | `string` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| multiLineLabel | `boolean` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| startRange | `TDate` | ❌ | - |  |
| endRange | `TDate` | ❌ | - |  |
| inputFormat | `enum` | ❌ | - |  |
| displayFormat | `enum` | ❌ | - |  |
| monthAndYearView | `DatePickerView[]` | ❌ | - |  |
| dateFormat | `string` | ❌ | - | Props applied to previous dateFormat is no longer needed. @deprecated Use inputFormat instead. |
| timeSpecific | `string` | ❌ | - |  |
| initialValue | `TDate` | ❌ | - |  |
| monthYearView | `boolean` | ❌ | - |  |
| disableWeekends | `boolean` | ❌ | - |  |
| holidays | `TDate[]` | ❌ | - |  |
| enablePast | `boolean` | ❌ | - |  |
| disableFuture | `boolean` | ❌ | - | If `true`, disable values after the current date for date components, time for time components and both for date time components. |
| disableCloseOnSelect | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| startOrEndOfTheMonth | `enum` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| mask | `string` | ❌ | - | Props applied to input text element. @deprecated sending mask is no longer needed. |
| shortYear | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| popperRef | `any` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isFilter | `boolean` | ❌ | - |  |
| skipPickerButtonOnFocus | `boolean` | ❌ | - |  |
| hidePickerIcon | `boolean` | ❌ | - |  |
| shouldDisableDate | `((date: Date \| null) =&gt; boolean)` | ❌ | - |  |
| onChange | `((date: Date, keyboardInputValue?: string) =&gt; void)` | ❌ | - |  |
| onError | `((reason: string, value: string) =&gt; void)` | ❌ | - |  |
| onApply | `((value: Date) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onOpen | `(() =&gt; void)` | ❌ | - | Callback fired when the popup requests to be opened. Use in controlled mode (see `open`). |
| onClose | `((value?: TDate) =&gt; void)` | ❌ | - |  |
| onAccept | `((value: TDate) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onEnter | `((value: TDate) =&gt; void)` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| pickerType | `enum` | ❌ | - |  |
| pickerSize | `enum` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| inlineLabel | `Element` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## FormDemoPage

**File:** `form/demos/FormDemoPage.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| formStyle | `CSSProperties` | ❌ | - |  |
| getInputsRefs | `((inputsRefs: any) =&gt; void)` | ❌ | - |  |
| onChange | `((element: any, inputsRefs?: any, formikForm?: any) =&gt; void)` | ❌ | - |  |
| formSchemaSections | `FormSchemaSection[]` | ✅ | - |  |
| onSubmit | `(values: FormikValues, formikHelpers?: FormikHelpers&lt;FormikValues&gt; \| undefined) =&gt; void \| Promise&lt;any&gt;` | ✅ | - | Submission handler |
| footer | `FormFooterProps` | ❌ | - |  |
| customSchema | `any` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| validate | `((values: FormikValues, refs?: any) =&gt; void \| object \| Promise&lt;FormikErrors&lt;FormikValues&gt;&gt;)` | ❌ | - | Validation function. Must return an error object or promise that throws an error object where that object keys map to corresponding value. |
| gridDirection | `enum` | ❌ | - |  |
| numberOfSkeletonFields | `number` | ❌ | - |  |
| formError | `boolean` | ❌ | - |  |
| fieldsWrapperStyle | `CSSProperties` | ❌ | - |  |
| variation | `enum` | ❌ | - |  |
| boxProps | `BoxProps` | ❌ | - |  |
| asWizard | `boolean` | ❌ | - |  |
| wizardProps | `{ asTabs?: boolean; tabsProps?: Partial&lt;TabsProps&gt;; currentStep?: number \| undefined; onStepChange?: ((step: number) =&gt; void) \| undefined; withStepper?: boolean \| undefined; } \| undefined` | ❌ | - |  |

---

## FormFooter

**File:** `form/components/FormFooter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| submit | `ButtonProps` | ❌ | - |  |
| resetForm | `ButtonProps` | ❌ | - |  |
| customJsx | `((form: any) =&gt; Element)` | ❌ | - |  |
| style | `CSSProperties` | ❌ | - |  |

---

## FormRadioField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - | Name attribute of the `input` element. |
| values | `RadioValuesProps[]` | ✅ | - |  |
| withGroup | `boolean` | ❌ | - |  |
| groupLabel | `string` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. |
| groupRowDirection | `boolean` | ❌ | - |  |
| InputProps | `{ [key: string]: string \| number; }` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| labelPlacement | `enum` | ❌ | - |  |
| checked | `boolean` | ❌ | - | If `true`, the component is checked. |
| value | `string \| null` | ❌ | - | The value of the component. The DOM API casts this to a string. |
| htmlFor | `string` | ❌ | - |  |
| radioGroupTextSize | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## FormRadioInput

**File:** `inputs/radio/FormRadioInput.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - | Name attribute of the `input` element. |
| values | `RadioValuesProps[]` | ✅ | - |  |
| withGroup | `boolean` | ❌ | - |  |
| groupLabel | `string` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. |
| groupRowDirection | `boolean` | ❌ | - |  |
| InputProps | `{ [key: string]: string \| number; }` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| labelPlacement | `enum` | ❌ | - |  |
| checked | `boolean` | ❌ | - | If `true`, the component is checked. |
| value | `string \| null` | ❌ | - | The value of the component. The DOM API casts this to a string. |
| htmlFor | `string` | ❌ | - |  |
| radioGroupTextSize | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## FormResetFormButton

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `ReactNode` | ❌ | - |  |
| onClick | `(event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt; \| undefined) =&gt; any` | ✅ | - |  |
| renderLabel | `ReactNode` | ❌ | - |  |
| withLoader | `boolean` | ❌ | - |  |
| withSelectedRows | `boolean` | ❌ | - |  |
| loaderPosition | `enum` | ❌ | - |  |
| iconButton | `IconProps` | ❌ | - |  |
| customWidth | `number` | ❌ | - |  |
| icon | `IconProps` | ❌ | - |  |
| open | `boolean` | ❌ | - |  |
| progressbar | `boolean` | ❌ | - |  |
| progressbarCount | `number` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| tooltip | `Omit&lt;TooltipProps, "children"&gt;` | ❌ | - |  |
| allowMultiTooltip | `boolean` | ❌ | - |  |
| disableHoverFocus | `boolean` | ❌ | - |  |
| ignoreMobileSizeChange | `boolean` | ❌ | - |  |
| testIdActionName | `string` | ❌ | - |  |
| squared | `boolean` | ❌ | - |  |
| iconAttachedLabel | `boolean` | ❌ | - |  |
| fitWidthToContent | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - | @deprecated Use `loading` instead. |
| buttonType | `enum` | ❌ | - |  |
| buttonSize | `enum` | ❌ | - |  |

---

## FormSelectField

**File:** `form/components/FormElements.tsx`

*No props documented*

---

## FormSkeleton

**File:** `form/components/FormSkeleton.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| numberOfFields | `number` | ❌ | - |  |

---

## FormSubmitButton

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `ReactNode` | ❌ | - |  |
| onClick | `(event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt; \| undefined) =&gt; any` | ✅ | - |  |
| renderLabel | `ReactNode` | ❌ | - |  |
| withLoader | `boolean` | ❌ | - |  |
| withSelectedRows | `boolean` | ❌ | - |  |
| loaderPosition | `enum` | ❌ | - |  |
| iconButton | `IconProps` | ❌ | - |  |
| customWidth | `number` | ❌ | - |  |
| icon | `IconProps` | ❌ | - |  |
| open | `boolean` | ❌ | - |  |
| progressbar | `boolean` | ❌ | - |  |
| progressbarCount | `number` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| tooltip | `Omit&lt;TooltipProps, "children"&gt;` | ❌ | - |  |
| allowMultiTooltip | `boolean` | ❌ | - |  |
| disableHoverFocus | `boolean` | ❌ | - |  |
| ignoreMobileSizeChange | `boolean` | ❌ | - |  |
| testIdActionName | `string` | ❌ | - |  |
| squared | `boolean` | ❌ | - |  |
| iconAttachedLabel | `boolean` | ❌ | - |  |
| fitWidthToContent | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - | @deprecated Use `loading` instead. |
| buttonType | `enum` | ❌ | - |  |
| buttonSize | `enum` | ❌ | - |  |

---

## FormSwitchField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, value?: boolean \| SwitchValue[]) =&gt; void)` | ❌ | - | Callback fired when the state is changed. |
| dir | `enum` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| label | `string` | ❌ | - |  |
| defaultChecked | `boolean` | ❌ | - | The default checked state. Use when the component is not controlled. |
| inputProps | `any` | ❌ | - | [Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Attributes) applied to the `input` element. |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| icon | `string` | ❌ | - |  |
| values | `SwitchValue[]` | ❌ | - |  |
| checkedIcon | `string` | ❌ | - |  |
| labelPlacement | `enum` | ❌ | - |  |
| switchType | `enum` | ❌ | - |  |
| offLabel | `string` | ❌ | - |  |
| onLabel | `string` | ❌ | - |  |
| groupRowDirection | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## FormTextAreaField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - |  |
| maxRows | `number` | ❌ | - | Maximum number of rows to display. |
| minRows | `number` | ❌ | - | Minimum number of rows to display. |
| disabled | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| resizeable | `boolean` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| label | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| withUndoButton | `boolean` | ❌ | - |  |
| ref | `any` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLTextAreaElement&gt;) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## FormTextField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| label | `string` | ❌ | - | The label content. |
| mask | `any` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| tabIndex | `number` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| inputType | `enum` | ❌ | - |  |
| inputSize | `enum` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onChange" \| "onFocus" \| "onBlur"; }` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## FormTextInput

**File:** `inputs/textInput/FormTextInput.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| inputType | `enum` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| inputSize | `enum` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| withForm | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| ref | `any` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| mask | `any` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onFocus" \| "onBlur" \| "onChange"; }` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## FormikContainer

**File:** `form/components/FormikContainer.tsx`

*No props documented*

---

## FreeTextFilter

**File:** `dataGrid/filters/free_text_filter.tsx`

*No props documented*

---

## GetComponent

**File:** `dataGrid/helpers/storyHelper.tsx`

*No props documented*

---

## Grid

**File:** `grid/Grid.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| border | `ResponsiveStyleValue&lt;number \| (string & {}) \| "inset" \| "hidden" \| "-moz-initial" \| "inherit" \| "initial" \| "revert" \| "revert-layer" \| "unset" \| "medium" \| "thick" \| "thin" \| "dashed" \| "dotted" \| ... 184 more ...&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderTop | `ResponsiveStyleValue&lt;BorderTop&lt;string \| number&gt; \| readonly NonNullable&lt;BorderTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderRight | `ResponsiveStyleValue&lt;BorderRight&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderBottom | `ResponsiveStyleValue&lt;BorderBottom&lt;string \| number&gt; \| readonly NonNullable&lt;BorderBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderLeft | `ResponsiveStyleValue&lt;BorderLeft&lt;string \| number&gt; \| readonly NonNullable&lt;BorderLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderColor | `ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt;)` | ❌ | - |  |
| borderRadius | `ResponsiveStyleValue&lt;BorderRadius&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRadius&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| display | `ResponsiveStyleValue&lt;readonly string[] \| Display&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Display&gt;)` | ❌ | - |  |
| displayPrint | `ResponsiveStyleValue&lt;readonly string[] \| Display&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Display&gt;)` | ❌ | - |  |
| overflow | `ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt;)` | ❌ | - |  |
| textOverflow | `ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt;)` | ❌ | - |  |
| visibility | `ResponsiveStyleValue&lt;Visibility \| readonly NonNullable&lt;Visibility&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| whiteSpace | `ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt;)` | ❌ | - |  |
| flexBasis | `ResponsiveStyleValue&lt;FlexBasis&lt;string \| number&gt; \| readonly NonNullable&lt;FlexBasis&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexDirection | `ResponsiveStyleValue&lt;FlexDirection \| readonly NonNullable&lt;FlexDirection&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexWrap | `ResponsiveStyleValue&lt;FlexWrap \| readonly NonNullable&lt;FlexWrap&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| justifyContent | `ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt;)` | ❌ | - |  |
| alignItems | `ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt;)` | ❌ | - |  |
| alignContent | `ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt;)` | ❌ | - |  |
| flex | `ResponsiveStyleValue&lt;Flex&lt;string \| number&gt; \| readonly NonNullable&lt;Flex&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexGrow | `ResponsiveStyleValue&lt;FlexGrow \| readonly NonNullable&lt;FlexGrow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexShrink | `ResponsiveStyleValue&lt;FlexShrink \| readonly NonNullable&lt;FlexShrink&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| alignSelf | `ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt;)` | ❌ | - |  |
| justifyItems | `ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt;)` | ❌ | - |  |
| justifySelf | `ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt;)` | ❌ | - |  |
| gap | `ResponsiveStyleValue&lt;Gap&lt;string \| number&gt; \| readonly NonNullable&lt;Gap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| columnGap | `ResponsiveStyleValue&lt;ColumnGap&lt;string \| number&gt; \| readonly NonNullable&lt;ColumnGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| rowGap | `ResponsiveStyleValue&lt;RowGap&lt;string \| number&gt; \| readonly NonNullable&lt;RowGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridColumn | `ResponsiveStyleValue&lt;GridColumn \| readonly NonNullable&lt;GridColumn&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridRow | `ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;GridRow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;...&gt;[] \| undefined&gt;)` | ❌ | - |  |
| gridAutoFlow | `ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt;)` | ❌ | - |  |
| gridAutoColumns | `ResponsiveStyleValue&lt;GridAutoColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridAutoRows | `ResponsiveStyleValue&lt;GridAutoRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateColumns | `ResponsiveStyleValue&lt;GridTemplateColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateRows | `ResponsiveStyleValue&lt;GridTemplateRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateAreas | `ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt;)` | ❌ | - |  |
| gridArea | `ResponsiveStyleValue&lt;GridArea \| readonly NonNullable&lt;GridArea&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bgcolor | `ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt;)` | ❌ | - |  |
| color | `ResponsiveStyleValue&lt;readonly string[] \| Color&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Color&gt;)` | ❌ | - |  |
| zIndex | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| position | `ResponsiveStyleValue&lt;Position \| readonly NonNullable&lt;Position&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| top | `ResponsiveStyleValue&lt;Top&lt;string \| number&gt; \| readonly NonNullable&lt;Top&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| right | `ResponsiveStyleValue&lt;Right&lt;string \| number&gt; \| readonly NonNullable&lt;Right&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bottom | `ResponsiveStyleValue&lt;Bottom&lt;string \| number&gt; \| readonly NonNullable&lt;Bottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| left | `ResponsiveStyleValue&lt;Left&lt;string \| number&gt; \| readonly NonNullable&lt;Left&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxShadow | `ResponsiveStyleValue&lt;number \| BoxShadow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;number \| BoxShadow&gt;)` | ❌ | - |  |
| width | `ResponsiveStyleValue&lt;Width&lt;string \| number&gt; \| readonly NonNullable&lt;Width&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxWidth | `ResponsiveStyleValue&lt;MaxWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MaxWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minWidth | `ResponsiveStyleValue&lt;MinWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MinWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| height | `ResponsiveStyleValue&lt;Height&lt;string \| number&gt; \| readonly NonNullable&lt;Height&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxHeight | `ResponsiveStyleValue&lt;MaxHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MaxHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minHeight | `ResponsiveStyleValue&lt;MinHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MinHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxSizing | `ResponsiveStyleValue&lt;BoxSizing \| readonly NonNullable&lt;BoxSizing&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| m | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mt | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mr | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mb | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| ml | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mx | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| my | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| p | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pt | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pr | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pb | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pl | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| px | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| py | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| margin | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginTop | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginRight | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBottom | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginLeft | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginX | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginY | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInline | `ResponsiveStyleValue&lt;MarginInline&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineStart | `ResponsiveStyleValue&lt;MarginInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineEnd | `ResponsiveStyleValue&lt;MarginInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlock | `ResponsiveStyleValue&lt;MarginBlock&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockStart | `ResponsiveStyleValue&lt;MarginBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockEnd | `ResponsiveStyleValue&lt;MarginBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| padding | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingTop | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingRight | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBottom | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingLeft | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingX | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingY | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInline | `ResponsiveStyleValue&lt;PaddingInline&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineStart | `ResponsiveStyleValue&lt;PaddingInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineEnd | `ResponsiveStyleValue&lt;PaddingInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlock | `ResponsiveStyleValue&lt;PaddingBlock&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockStart | `ResponsiveStyleValue&lt;PaddingBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockEnd | `ResponsiveStyleValue&lt;PaddingBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| typography | `ResponsiveStyleValue&lt;string&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string&gt;)` | ❌ | - |  |
| fontFamily | `ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt;)` | ❌ | - |  |
| fontSize | `ResponsiveStyleValue&lt;FontSize&lt;string \| number&gt; \| readonly NonNullable&lt;FontSize&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| fontStyle | `ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt;)` | ❌ | - |  |
| fontWeight | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| letterSpacing | `ResponsiveStyleValue&lt;LetterSpacing&lt;string \| number&gt; \| readonly NonNullable&lt;LetterSpacing&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| lineHeight | `ResponsiveStyleValue&lt;LineHeight&lt;string \| number&gt; \| readonly NonNullable&lt;LineHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| textAlign | `ResponsiveStyleValue&lt;TextAlign \| readonly NonNullable&lt;TextAlign&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| textTransform | `ResponsiveStyleValue&lt;TextTransform \| readonly NonNullable&lt;TextTransform&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |

---

## GridSvg

**File:** `dataGrid/renderers/type/type_view.tsx`

*No props documented*

---

## Icon

**File:** `icon/Icon2.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | `500px` |  |
| className | `string` | ❌ | - |  |
| size | `enum` | ❌ | `m` |  |
| iconType | `enum` | ❌ | - |  |
| withGradient | `"gradient_100" \| "gradient_45" \| "gradient_blue_45" \| "gradient_stampli_po" \| "gradient_erp_po" \| "gradient_credit_card" \| "gradient_service_ticket" \| "gradient_request" \| ... 4 more ...` | ❌ | `null` |  |
| iconPrefix | `enum` | ❌ | `fal` |  |
| withToolTip | `TooltipProps` | ❌ | - |  |
| tooltipCustomStyle | `CSSProperties` | ❌ | - |  |
| withBadge | `Badge` | ❌ | - |  |
| useBillySvgIcon | `boolean` | ❌ | - |  |
| sizeReduce | `boolean` | ❌ | - |  |

---

## IconHeaderRenderer

**File:** `dataGrid/renderers/icon/icon_header.tsx`

*No props documented*

---

## IconRenderer

**File:** `dataList/renderers/icon/icon_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## IconWrapper

**File:** `dataGrid/renderers/icon/icon_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| size | `enum` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| withGradient | `"gradient_100" \| "gradient_45" \| "gradient_blue_45" \| "gradient_stampli_po" \| "gradient_erp_po" \| "gradient_credit_card" \| "gradient_service_ticket" \| "gradient_request" \| ... 4 more ...` | ❌ | - |  |
| iconPrefix | `enum` | ❌ | - |  |
| withToolTip | `TooltipProps` | ❌ | - |  |
| tooltipCustomStyle | `CSSProperties` | ❌ | - |  |
| withBadge | `Badge` | ❌ | - |  |
| useBillySvgIcon | `boolean` | ❌ | - |  |
| sizeReduce | `boolean` | ❌ | - |  |
| emptyIcon | `boolean` | ❌ | - |  |

---

## IdentitySelect

**File:** `form/components/IdentitySelect/IdentitySelect.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - |  |
| value | `string` | ❌ | - |  |
| idProps | `TextInputProps` | ❌ | - |  |
| passportProps | `TextInputProps` | ❌ | - |  |
| defaultIdentityType | `IdentityType` | ❌ | - |  |
| selectLabel | `string` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| direction | `enum` | ❌ | - |  |
| selectStyles | `CSSProperties` | ❌ | - |  |
| textInputStyles | `CSSProperties` | ❌ | - |  |
| containerStyles | `CSSProperties` | ❌ | - |  |
| textInputWrapperStyles | `CSSProperties` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| onSelectChange | `((value: IdentityType) =&gt; void)` | ❌ | - |  |
| onTextChange | `((value: Record&lt;string, string&gt;) =&gt; void)` | ❌ | - |  |

---

## ImagePreview

**File:** `ImagePreview/ImagePreview.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| files | `FileInfo[]` | ✅ | - | Array of files to display as thumbnails. Images will be displayed first, followed by documents. |
| onRemoveFile | `(fileId: string) =&gt; void` | ✅ | - | Callback when a file is removed |
| className | `string` | ❌ | - | Optional className for custom styling |
| enableImagePreview | `boolean` | ❌ | - | Whether to show image preview dialog when clicking on images |
| withImageNavigation | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If true, disables all actions except image preview |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| variant | `enum` | ❌ | - | Visual variant - 'default' has rounded corners Visual variant - 'richTextEditor' has square top corners |
| onSubmit | `(() =&gt; void)` | ❌ | - | Optional submit callback for richTextEditor variant |

---

## InfinitScroll

**File:** `infinitScroll/InfinitScroll.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| items | `false \| Element[] \| null \| undefined` | ✅ | - |  |
| loader | `Element` | ❌ | `<h4>Loading...</h4>` |  |
| endMessage | `Element` | ❌ | `(
    <p style={{ textAlign: 'center' }}>
      <b>Yay! You have seen it all</b>
    </p>
  )` |  |
| itemsPerLoad | `number` | ❌ | `10` |  |
| maxItemsToLoad | `number` | ❌ | `20000` |  |

---

## InlineFileUploader

**File:** `inputs/file/InlineFileUploader.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| name | `string` | ❌ | - |  |
| label | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| maxSize | `number` | ❌ | - |  |
| acceptedFileTypes | `string[]` | ❌ | - |  |
| allowDuplicates | `boolean` | ❌ | - |  |
| onUploadStart | `(() =&gt; void)` | ❌ | - |  |
| onUploadFile | `(uploadFile: FileDocument, setProgress?: any, controller?: any) =&gt; Promise&lt;any&gt;` | ✅ | - |  |
| onDeleteFile | `((fileToRemove: FileDocument) =&gt; void)` | ❌ | - |  |
| onDownloadFile | `((index: number) =&gt; void)` | ❌ | - |  |
| onUploadFinish | `((files?: (FileDocument)[]) =&gt; void) \| undefined` | ❌ | - |  |
| onError | `((errors: FileRejection[]) =&gt; void)` | ❌ | - |  |
| dateFormat | `string` | ❌ | - |  |
| maxFiles | `number` | ❌ | - |  |
| files | `BaseFileDocument[]` | ❌ | - |  |
| disableDownload | `boolean` | ❌ | - |  |
| disableDelete | `boolean` | ❌ | - |  |
| hasError | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Intro

**File:** `intro/Intro.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| ref | `any` | ❌ | - |  |
| run | `boolean` | ❌ | - |  |
| startIndex | `number` | ❌ | - |  |
| style | `any` | ❌ | - |  |
| onStateChange | `((params: any) =&gt; void)` | ❌ | - |  |
| customProps | `IntroTooltipProps` | ❌ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| showNextButton | `boolean` | ❌ | - |  |
| showFooterButtons | `boolean` | ❌ | - |  |

---

## IntroPage

**File:** `intro/IntroPage.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| ref | `any` | ❌ | - |  |
| run | `boolean` | ❌ | - |  |
| startIndex | `number` | ❌ | - |  |
| style | `any` | ❌ | - |  |
| onStateChange | `((params: any) =&gt; void)` | ❌ | - |  |
| customProps | `IntroTooltipProps` | ❌ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| showNextButton | `boolean` | ❌ | - |  |
| showFooterButtons | `boolean` | ❌ | - |  |

---

## InvoiceMobileTable

**File:** `dataGrid/mocks/InvoiceMobileTable.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## InvoicesTemplate

Invoices Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## JSXRenderer

**File:** `dataGrid/renderers/jsx_renderer.tsx`

*No props documented*

---

## JsxRenderer

**File:** `dataGrid/renderers/jsx_renderer.tsx`

*No props documented*

---

## KeyValueRenderer

**File:** `dataList/renderers/keyValue/key_value.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## KpiBox

**File:** `dashboards/widgets/KpiBox/KpiBox.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `WidgetTypes.KPI_BOX` | ✅ | - |  |
| data | `KpiBoxData[]` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| title | `undefined` | ❌ | - |  |
| layout | `undefined` | ❌ | - |  |
| fullWidth | `undefined` | ❌ | - |  |
| groups | `undefined` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## LineChart

**File:** `charts/LineChart/LineChart.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `WidgetTypes.LINE_CHART` | ✅ | - |  |
| layout | `undefined` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| data | `ChartData` | ✅ | - |  |
| id | `string` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;Props&gt;[]` | ✅ | - |  |
| legendProps | `any` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Link

**File:** `link/Link.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `string \| Element` | ✅ | - |  |
| linkType | `enum` | ❌ | - |  |
| target | `enum` | ❌ | - |  |
| icon | `string` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| subtle | `boolean` | ❌ | - |  |
| color | `enum` | ❌ | - |  |
| textType | `enum` | ❌ | - |  |
| tooltip | `TooltipProps` | ❌ | - |  |
| display | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| border | `ResponsiveStyleValue&lt;number \| (string & {}) \| "inset" \| "hidden" \| "inherit" \| "none" \| "-moz-initial" \| "initial" \| "revert" \| "revert-layer" \| "unset" \| "medium" \| "thick" \| "thin" \| "dashed" \| ... 184 more ...&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderTop | `ResponsiveStyleValue&lt;BorderTop&lt;string \| number&gt; \| readonly NonNullable&lt;BorderTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderRight | `ResponsiveStyleValue&lt;BorderRight&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderBottom | `ResponsiveStyleValue&lt;BorderBottom&lt;string \| number&gt; \| readonly NonNullable&lt;BorderBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderLeft | `ResponsiveStyleValue&lt;BorderLeft&lt;string \| number&gt; \| readonly NonNullable&lt;BorderLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderColor | `ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt;)` | ❌ | - |  |
| borderRadius | `ResponsiveStyleValue&lt;BorderRadius&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRadius&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| displayPrint | `ResponsiveStyleValue&lt;readonly string[] \| Display&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Display&gt;)` | ❌ | - |  |
| overflow | `ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt;)` | ❌ | - |  |
| textOverflow | `ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt;)` | ❌ | - |  |
| visibility | `ResponsiveStyleValue&lt;Visibility \| readonly NonNullable&lt;Visibility&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| whiteSpace | `ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt;)` | ❌ | - |  |
| flexBasis | `ResponsiveStyleValue&lt;FlexBasis&lt;string \| number&gt; \| readonly NonNullable&lt;FlexBasis&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexDirection | `ResponsiveStyleValue&lt;FlexDirection \| readonly NonNullable&lt;FlexDirection&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexWrap | `ResponsiveStyleValue&lt;FlexWrap \| readonly NonNullable&lt;FlexWrap&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| justifyContent | `ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt;)` | ❌ | - |  |
| alignItems | `ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt;)` | ❌ | - |  |
| alignContent | `ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt;)` | ❌ | - |  |
| order | `ResponsiveStyleValue&lt;Order \| readonly NonNullable&lt;Order&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;Order \| readonly NonNullable&lt;...&gt;[] \| undefined&gt;)` | ❌ | - |  |
| flex | `ResponsiveStyleValue&lt;Flex&lt;string \| number&gt; \| readonly NonNullable&lt;Flex&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexGrow | `ResponsiveStyleValue&lt;FlexGrow \| readonly NonNullable&lt;FlexGrow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexShrink | `ResponsiveStyleValue&lt;FlexShrink \| readonly NonNullable&lt;FlexShrink&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| alignSelf | `ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt;)` | ❌ | - |  |
| justifyItems | `ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt;)` | ❌ | - |  |
| justifySelf | `ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt;)` | ❌ | - |  |
| gap | `ResponsiveStyleValue&lt;Gap&lt;string \| number&gt; \| readonly NonNullable&lt;Gap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| columnGap | `ResponsiveStyleValue&lt;ColumnGap&lt;string \| number&gt; \| readonly NonNullable&lt;ColumnGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| rowGap | `ResponsiveStyleValue&lt;RowGap&lt;string \| number&gt; \| readonly NonNullable&lt;RowGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridColumn | `ResponsiveStyleValue&lt;GridColumn \| readonly NonNullable&lt;GridColumn&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridRow | `ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;GridRow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;...&gt;[] \| undefined&gt;)` | ❌ | - |  |
| gridAutoFlow | `ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt;)` | ❌ | - |  |
| gridAutoColumns | `ResponsiveStyleValue&lt;GridAutoColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridAutoRows | `ResponsiveStyleValue&lt;GridAutoRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateColumns | `ResponsiveStyleValue&lt;GridTemplateColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateRows | `ResponsiveStyleValue&lt;GridTemplateRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateAreas | `ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt;)` | ❌ | - |  |
| gridArea | `ResponsiveStyleValue&lt;GridArea \| readonly NonNullable&lt;GridArea&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bgcolor | `ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt;)` | ❌ | - |  |
| zIndex | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| position | `ResponsiveStyleValue&lt;Position \| readonly NonNullable&lt;Position&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| top | `ResponsiveStyleValue&lt;Top&lt;string \| number&gt; \| readonly NonNullable&lt;Top&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| right | `ResponsiveStyleValue&lt;Right&lt;string \| number&gt; \| readonly NonNullable&lt;Right&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bottom | `ResponsiveStyleValue&lt;Bottom&lt;string \| number&gt; \| readonly NonNullable&lt;Bottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| left | `ResponsiveStyleValue&lt;Left&lt;string \| number&gt; \| readonly NonNullable&lt;Left&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxShadow | `ResponsiveStyleValue&lt;number \| BoxShadow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;number \| BoxShadow&gt;)` | ❌ | - |  |
| width | `ResponsiveStyleValue&lt;Width&lt;string \| number&gt; \| readonly NonNullable&lt;Width&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxWidth | `ResponsiveStyleValue&lt;MaxWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MaxWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minWidth | `ResponsiveStyleValue&lt;MinWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MinWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| height | `ResponsiveStyleValue&lt;Height&lt;string \| number&gt; \| readonly NonNullable&lt;Height&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxHeight | `ResponsiveStyleValue&lt;MaxHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MaxHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minHeight | `ResponsiveStyleValue&lt;MinHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MinHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxSizing | `ResponsiveStyleValue&lt;BoxSizing \| readonly NonNullable&lt;BoxSizing&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| m | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mt | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mr | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mb | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| ml | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mx | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| my | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| p | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pt | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pr | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pb | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pl | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| px | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| py | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| margin | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginTop | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginRight | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBottom | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginLeft | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginX | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginY | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInline | `ResponsiveStyleValue&lt;MarginInline&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineStart | `ResponsiveStyleValue&lt;MarginInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineEnd | `ResponsiveStyleValue&lt;MarginInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlock | `ResponsiveStyleValue&lt;MarginBlock&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockStart | `ResponsiveStyleValue&lt;MarginBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockEnd | `ResponsiveStyleValue&lt;MarginBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| padding | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingTop | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingRight | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBottom | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingLeft | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingX | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingY | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInline | `ResponsiveStyleValue&lt;PaddingInline&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineStart | `ResponsiveStyleValue&lt;PaddingInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineEnd | `ResponsiveStyleValue&lt;PaddingInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlock | `ResponsiveStyleValue&lt;PaddingBlock&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockStart | `ResponsiveStyleValue&lt;PaddingBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockEnd | `ResponsiveStyleValue&lt;PaddingBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| typography | `ResponsiveStyleValue&lt;string&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string&gt;)` | ❌ | - |  |
| fontFamily | `ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt;)` | ❌ | - |  |
| fontSize | `ResponsiveStyleValue&lt;FontSize&lt;string \| number&gt; \| readonly NonNullable&lt;FontSize&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| fontStyle | `ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt;)` | ❌ | - |  |
| fontWeight | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| letterSpacing | `ResponsiveStyleValue&lt;LetterSpacing&lt;string \| number&gt; \| readonly NonNullable&lt;LetterSpacing&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| lineHeight | `ResponsiveStyleValue&lt;LineHeight&lt;string \| number&gt; \| readonly NonNullable&lt;LineHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| textAlign | `ResponsiveStyleValue&lt;TextAlign \| readonly NonNullable&lt;TextAlign&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| textTransform | `ResponsiveStyleValue&lt;TextTransform \| readonly NonNullable&lt;TextTransform&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |

---

## LinkPreview

**File:** `inputs/RichTextEditor/LinkPreview.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| data | `LinkPreviewData` | ✅ | - |  |

---

## LinkRenderer

**File:** `dataList/renderers/link/link_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## List

**File:** `list/List.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| listType | `enum` | ✅ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| icon | `IconProps` | ❌ | - |  |
| listItems | `ListItemProps[]` | ✅ | - |  |
| renderItem | `((list: ListItemProps) =&gt; Element \| null)` | ❌ | - |  |
| filterOptions | `{ selectPlaceholder?: string; options: SelectOption[]; allOption?: string; } \| undefined` | ❌ | - |  |
| onFilterChange | `((selectedOption: SelectOption \| null) =&gt; void)` | ❌ | - |  |
| filterMetaData | `{ key: string; value: string[]; }[]` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| direction | `enum` | ❌ | - |  |
| alignItems | `enum` | ❌ | - |  |
| justifyContent | `enum` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| flex | `number \| "unset"` | ❌ | - |  |
| style | `CSSProperties` | ❌ | - |  |
| customStyle | `any` | ❌ | - |  |
| gap | `number` | ❌ | - |  |
| onMouseEnter | `((e: any) =&gt; void)` | ❌ | - |  |
| onMouseLeave | `((e: any) =&gt; void)` | ❌ | - |  |
| onClick | `((e: any) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## ListItem

**File:** `list/listItems/ListItem.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| index | `number` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| user | `string` | ❌ | - |  |
| creationTime | `string \| Date` | ❌ | - |  |
| dateFormat | `string` | ❌ | - |  |
| relativeCreationTime | `string` | ❌ | - |  |
| listItemType | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| header | `string` | ❌ | - |  |
| headerUrl | `string` | ❌ | - |  |
| headerUrlText | `string` | ❌ | - |  |
| body | `string` | ❌ | - |  |
| bodyTooltip | `string` | ❌ | - |  |
| bodyUrl | `string` | ❌ | - |  |
| bodyUrlText | `string` | ❌ | - |  |
| footer | `string` | ❌ | - |  |
| groupId | `string` | ❌ | - |  |
| groupItems | `ListItemProps[]` | ❌ | - |  |
| firstInGroup | `boolean` | ❌ | - |  |
| lastInGroup | `boolean` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| userTooltip | `{ fullName: string; email: string; freeText?: string; }` | ❌ | - |  |
| freeJsxFunc | `(() =&gt; Element \| null)` | ❌ | - |  |
| renderItem | `((list: any) =&gt; Element \| null)` | ❌ | - |  |
| payAttention | `boolean` | ❌ | - |  |
| filterMetaData | `string[]` | ❌ | - |  |
| attachments | `ListItemAttachment[]` | ❌ | - |  |
| data | `ListItemData \| ListItemAttachment[] \| ChatMessage[]` | ❌ | - |  |
| canReplay | `boolean` | ❌ | - |  |
| canUpload | `boolean` | ❌ | - |  |
| fileTypesToUpload | `string[]` | ❌ | - |  |
| textAreaPlaceholder | `string` | ❌ | - |  |
| freeText | `string` | ❌ | - |  |
| onSubmit | `((data: any) =&gt; void)` | ❌ | - |  |
| leaveChat | `(() =&gt; void)` | ❌ | - |  |
| onAddFile | `((file: File) =&gt; Promise&lt;string&gt;)` | ❌ | - |  |
| onRemoveFile | `((file: File) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## ListboxComponent

**File:** `select/ListboxComponent.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ❌ | - |  |
| role | `string \| (string & {})` | ❌ | - |  |
| selectSize | `enum` | ✅ | - |  |

---

## LottieAnimation

**File:** `LottieAnimation/LottieAnimation.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| lottieName | `enum` | ✅ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| onOpen | `(() =&gt; void)` | ❌ | - |  |
| onComplete | `(() =&gt; void)` | ❌ | - |  |
| open | `boolean` | ❌ | `true` |  |
| width | `string \| number` | ❌ | `100%` |  |
| duration | `number` | ❌ | `3000` |  |
| loop | `boolean` | ❌ | `true` |  |
| withOverlay | `boolean` | ❌ | `true` |  |
| lottieContainerStyle | `CSSProperties` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## MainForm

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| formStyle | `CSSProperties` | ❌ | - |  |
| getInputsRefs | `((inputsRefs: any) =&gt; void)` | ❌ | - |  |
| onChange | `((element: any, inputsRefs?: any, formikForm?: any) =&gt; void)` | ❌ | - |  |

---

## MemoRenderer

**File:** `dataGrid/helpers/memo.tsx`

*No props documented*

---

## MenuBar

**File:** `mobile/mobileImagePreview/MobileImagePreview.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| imageUrl | `string \| null` | ❌ | - |  |
| imagePreviewButtons | `MobileImagePreviewButton[]` | ❌ | - |  |
| show | `boolean` | ✅ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## MenuCustom

**File:** `select-menu/MenuCustom.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| anchorEl | `HTMLElement \| null` | ✅ | - |  |
| open | `boolean` | ✅ | - |  |
| onClose | `() =&gt; void` | ✅ | - |  |

---

## NotificationBar

**File:** `notificationBar/NotificationBar.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| showCloseButton | `boolean` | ❌ | - |  |
| onClose | `((() =&gt; void) & (() =&gt; void))` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| notifications | `NotificationItem[]` | ❌ | - |  |
| showBar | `boolean` | ❌ | - |  |
| notificationTextType | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Number

**File:** `dataGrid/renderers/number/number_edit.tsx`

*No props documented*

---

## NumberBasicEditRenderer

**File:** `dataGrid/renderers/number/number_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| showLabel | `boolean` | ❌ | - |  |

---

## NumberEditRenderer

**File:** `dataGrid/renderers/number/number_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| showLabel | `boolean` | ❌ | - |  |

---

## NumberRange

**File:** `numberRange/NumberRange.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onFilterChange | `(text: any, type: string) =&gt; void` | ✅ | - |  |
| initialValueType | `string` | ❌ | `above` |  |
| initialValue | `string` | ❌ | - |  |
| headerName | `string` | ❌ | - |  |

---

## NumberRenderer

**File:** `dataList/renderers/number/number_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## NumericFilter

**File:** `dataGrid/filters/numeric_filter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| filterRef | `MutableRefObject&lt;any&gt;` | ❌ | - |  |
| customFieldName | `string` | ✅ | - |  |
| filterType | `enum` | ✅ | - |  |
| pinned | `boolean` | ❌ | - |  |
| freeText | `boolean` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| id | `string` | ✅ | - |  |
| type | `string` | ❌ | - |  |
| apiRef | `any` | ✅ | - |  |
| label | `string` | ✅ | - |  |
| field | `string` | ✅ | - | The column identifier. It's used to map with [[GridRowModel]] values. |
| rows | `any` | ✅ | - |  |
| columns | `any` | ✅ | - |  |
| options | `SelectOption[]` | ❌ | - |  |
| getOptions | `(() =&gt; Promise&lt;any&gt;)` | ❌ | - |  |
| filterProps | `any` | ✅ | - |  |
| filterModel | `any` | ✅ | - |  |
| triggerOnChange | `boolean` | ❌ | - |  |
| onFilterChanged | `((filterModel: GridFilterModel, inputEl?: HTMLInputElement \| null) =&gt; void)` | ❌ | - |  |
| getFilterModel | `() =&gt; any` | ✅ | - |  |
| quickFilter | `QuickFiltersConfig` | ❌ | - |  |
| iconProps | `IconProps` | ❌ | - |  |
| headerProps | `HeaderProps` | ❌ | - |  |
| dateProps | `DateProps` | ❌ | - |  |
| selectProps | `GridSelectProps` | ❌ | - |  |
| textProps | `TextProps` | ❌ | - |  |
| numberProps | `NumberProps` | ❌ | - |  |
| currencyProps | `CurrencyProps` | ❌ | - |  |
| linkProps | `LinkProps` | ❌ | - |  |
| getter | `enum` | ❌ | - |  |
| ignoreCellClick | `boolean` | ❌ | - |  |
| isFirst | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| boldText | `boolean` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| autoGeneratedOptions | `boolean` | ❌ | - |  |
| popper | `Element` | ❌ | - |  |
| badge | `boolean` | ❌ | - |  |
| tooltip | `boolean` | ❌ | - |  |
| inputAutoEvents | `InputAutoEvents` | ❌ | - |  |
| searchFilter | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| visible | `boolean` | ❌ | - |  |
| hideIfEmpty | `boolean` | ❌ | - |  |
| hideOnMobile | `boolean` | ❌ | - |  |
| mobile | `ColumnMobileConfig` | ❌ | - |  |
| allowBulkEdit | `boolean` | ❌ | - |  |
| onClick | `((row: any, params?: any) =&gt; void)` | ❌ | - |  |
| onChange | `((row: any, props: any, apiRef: any) =&gt; void)` | ❌ | - |  |
| validateInput | `((props: any) =&gt; ValidationResult)` | ❌ | - |  |
| preProcessProps | `((props: any) =&gt; any)` | ❌ | - |  |
| searchProps | `{ columnsToHide?: string[]; renderCellContent?: ((params: any) =&gt; Element); commitRowChange?: ((params: any) =&gt; void) \| undefined; onChangeText?: ((search: string, params?: { ...; } \| undefined) =&gt; Promise&lt;...&gt;) \| undefined; renderFooter?: ((row: any) =&gt; any) \| undefined; } \| undefined` | ❌ | - |  |

---

## NumericFilterPaper

**File:** `numberRange/NumericRangeFilterBase.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| filterType | `string` | ❌ | - |  |

---

## NumericRangeFilterBase

**File:** `numberRange/NumericRangeFilterBase.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| field | `string` | ✅ | - | field identifier |
| label | `string` | ✅ | - | label to show |
| from | `number \| null` | ❌ | `null` | current from value |
| to | `number \| null` | ❌ | `null` | current to value |
| onChange | `((range: { from: number \| null; to: number \| null; }) =&gt; void)` | ❌ | - | on change without applying (typing) |
| onApply | `((range: { from: number \| null; to: number \| null; }) =&gt; void)` | ❌ | - | apply selected range (Enter/close/click away) |
| onClear | `(() =&gt; void)` | ❌ | - | clear handler |
| type | `enum` | ❌ | `number` | optional type to display currency |
| filterType | `enum` | ❌ | `bar` | filter type for width computation |
| testIdPrefix | `string` | ❌ | - | test id prefix |
| PaperComponent | `any` | ❌ | `styled(Paper)<{ filterType?: string }>`
  max-height: 50px !important;
  padding: 10px 0 10px 10px;

  & .CL-FormControl {
    max-width: 135px !important;
    min-width: 135px !important;
  }
`` | optional custom Paper component (e.g., grid NumericFilterPaper) |
| PopperComponent | `any` | ❌ | - | optional custom Popper component |
| paperProps | `any` | ❌ | - | optional props to spread into PaperComponent (e.g., modifiers) |
| numberAreaFormat | `enum` | ✅ | - | number area format for EU/US parsing |

---

## ObjectField

**File:** `form/components/FieldItem/fields/ObjectField/ObjectField.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - |  |
| label | `string` | ✅ | - |  |
| info | `string` | ❌ | - |  |
| onChange | `(value: Record&lt;string, any&gt;) =&gt; void` | ✅ | - | Receives the object values when any child field changes |
| onSelectChange | `((value: Record&lt;string, any&gt;) =&gt; void)` | ❌ | - | Receives the object values (same data model as onChange) when header select changes |
| fields | `ObjectNestedFieldItemProps[]` | ✅ | - |  |
| value | `Record&lt;string, any&gt;` | ❌ | - | Initial value for the object field (will populate child fields) |
| expanded | `boolean` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorFields | `ErrorField` | ❌ | - |  |
| warningFields | `WarningField` | ❌ | - |  |
| updatedFields | `UpdatedField` | ❌ | - |  |
| labelMaxWidth | `number` | ❌ | - |  |
| showUpdateFlag | `boolean` | ❌ | - |  |
| labelTooltipText | `string` | ❌ | - |  |
| selectProps | `SelectProps` | ❌ | - | Optional select props for the header select component |
| showHeaderSelect | `boolean` | ❌ | - | Controls whether the select is shown in the header |
| newOptionTargetField | `string` | ❌ | - | Field name to populate with the new option's label when creating a new option |

---

## POTable

**File:** `dataGrid/mocks/POTable.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## PaymentsReportsTemplate

PaymentsReports Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## PaymentsReportsWithDeleteRowsTemplate

PaymentsReportsWithDeleteRows Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## PendingApprovalTemplate

PendingApproval Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## PendingForFilter

**File:** `dashboards/components/filters/PendingForFilter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onFilterChange | `((params: any) =&gt; void)` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| cb | `((value: any, name: string) =&gt; void)` | ❌ | - |  |
| index | `number` | ❌ | - |  |
| position | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| filterType | `DashboardFilterTypes.PENDING_FOR` | ✅ | - |  |
| filterProps | `Omit&lt;SelectProps, "onChange" \| "options" \| "multiple"&gt; & { label?: string \| undefined; }` | ✅ | - |  |

---

## PhoneNumberSelect

**File:** `form/components/PhoneNumberSelect/PhoneNumberSelect.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| countryCodeName | `string` | ✅ | - |  |
| phoneNumberName | `string` | ✅ | - |  |
| countryCodePlaceholder | `string` | ❌ | - |  |
| countryCodeLabel | `string` | ❌ | - |  |
| phoneNumberPlaceholder | `string` | ❌ | - |  |
| phoneNumberLabel | `string` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| phoneNumber | `string` | ❌ | - |  |
| countryDisabled | `boolean` | ❌ | - |  |
| phoneNumberDisabled | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| countryCode | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| onCountryChange | `((params: { countryCode: string; isoCode: string; }) =&gt; void)` | ❌ | - |  |
| onChange | `(params: { isValid: boolean; countryCode: string; phoneNumber: string; phoneNumberFormatted: string; isoCode: string; parsedPhoneNumber: any; }) =&gt; void` | ✅ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## PhoneNumberSelectField

**File:** `form/components/FormElements.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| countryCodeName | `string` | ❌ | - |  |
| phoneNumberName | `string` | ❌ | - |  |
| countryCodePlaceholder | `string` | ❌ | - |  |
| countryCodeLabel | `string` | ❌ | - |  |
| phoneNumberPlaceholder | `string` | ❌ | - |  |
| phoneNumberLabel | `string` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| phoneNumber | `string` | ❌ | - |  |
| countryDisabled | `boolean` | ❌ | - |  |
| phoneNumberDisabled | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| countryCode | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| onCountryChange | `((params: { countryCode: string; isoCode: string; }) =&gt; void)` | ❌ | - |  |
| onChange | `((params: { isValid: boolean; countryCode: string; phoneNumber: string; phoneNumberFormatted: string; isoCode: string; parsedPhoneNumber: any; }) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| draftMode | `boolean` | ❌ | - |  |
| showErrorUntouched | `boolean` | ❌ | - |  |
| memoField | `boolean` | ❌ | - |  |
| dependsOn | `DependsOn` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| simulateTabOnChange | `boolean` | ❌ | - |  |
| customRef | `RefObject&lt;any&gt;` | ❌ | - |  |

---

## PieChart

**File:** `charts/PieChart/PieChart.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `WidgetTypes.PIE_CHART` | ✅ | - |  |
| layout | `undefined` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| id | `string` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;Props&gt;[]` | ✅ | - |  |
| legendProps | `any` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| data | `ChartData` | ✅ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## PinEntry

**File:** `pinEntry/PinEntry.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| length | `number` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| initialValue | `string[]` | ❌ | - |  |
| secret | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| focusIndex | `number` | ❌ | - |  |
| autoSelect | `boolean` | ❌ | - |  |
| regexCriteria | `any` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| pinInputSize | `enum` | ❌ | - |  |
| onChange | `((value: string, index: number) =&gt; void)` | ❌ | - |  |
| onComplete | `((value: string) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## ProcurementRequestTable

**File:** `dataGrid/mocks/Request.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## ProgressArrow

**File:** `ArrowProgressBar/components/ProgressArrow.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| isDragging | `boolean` | ✅ | - |  |
| isFirst | `boolean` | ✅ | - |  |
| isLast | `boolean` | ✅ | - |  |
| step | `ProgressStepProps&lt;any&gt;` | ✅ | - |  |
| progressBarType | `enum` | ❌ | - |  |
| onDelete | `((step: ProgressStepProps&lt;any&gt;) =&gt; void)` | ❌ | - |  |
| onClick | `((stepId: string) =&gt; void)` | ❌ | - |  |
| style | `CSSProperties` | ❌ | - |  |
| isScrolling | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## QuickFilters

**File:** `dataGrid/filters/quick_filters.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| filterRef | `MutableRefObject&lt;any&gt;` | ❌ | - |  |
| customFieldName | `string` | ✅ | - |  |
| filterType | `enum` | ✅ | - |  |
| pinned | `boolean` | ❌ | - |  |
| freeText | `boolean` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| id | `string` | ✅ | - |  |
| type | `string` | ❌ | - |  |
| apiRef | `any` | ✅ | - |  |
| label | `string` | ✅ | - |  |
| field | `string` | ✅ | - | The column identifier. It's used to map with [[GridRowModel]] values. |
| rows | `any` | ✅ | - |  |
| columns | `any` | ✅ | - |  |
| options | `SelectOption[]` | ❌ | - |  |
| getOptions | `(() =&gt; Promise&lt;any&gt;)` | ❌ | - |  |
| filterProps | `any` | ✅ | - |  |
| filterModel | `any` | ✅ | - |  |
| triggerOnChange | `boolean` | ❌ | - |  |
| onFilterChanged | `((filterModel: GridFilterModel, inputEl?: HTMLInputElement \| null) =&gt; void)` | ❌ | - |  |
| getFilterModel | `() =&gt; any` | ✅ | - |  |
| quickFilter | `QuickFiltersConfig` | ❌ | - |  |
| iconProps | `IconProps` | ❌ | - |  |
| headerProps | `HeaderProps` | ❌ | - |  |
| dateProps | `DateProps` | ❌ | - |  |
| selectProps | `GridSelectProps` | ❌ | - |  |
| textProps | `TextProps` | ❌ | - |  |
| numberProps | `NumberProps` | ❌ | - |  |
| currencyProps | `CurrencyProps` | ❌ | - |  |
| linkProps | `LinkProps` | ❌ | - |  |
| getter | `enum` | ❌ | - |  |
| ignoreCellClick | `boolean` | ❌ | - |  |
| isFirst | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| boldText | `boolean` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| autoGeneratedOptions | `boolean` | ❌ | - |  |
| popper | `Element` | ❌ | - |  |
| badge | `boolean` | ❌ | - |  |
| tooltip | `boolean` | ❌ | - |  |
| inputAutoEvents | `InputAutoEvents` | ❌ | - |  |
| searchFilter | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| visible | `boolean` | ❌ | - |  |
| hideIfEmpty | `boolean` | ❌ | - |  |
| hideOnMobile | `boolean` | ❌ | - |  |
| mobile | `ColumnMobileConfig` | ❌ | - |  |
| allowBulkEdit | `boolean` | ❌ | - |  |
| onClick | `((row: any, params?: any) =&gt; void)` | ❌ | - |  |
| onChange | `((row: any, props: any, apiRef: any) =&gt; void)` | ❌ | - |  |
| validateInput | `((props: any) =&gt; ValidationResult)` | ❌ | - |  |
| preProcessProps | `((props: any) =&gt; any)` | ❌ | - |  |
| searchProps | `{ columnsToHide?: string[]; renderCellContent?: ((params: any) =&gt; Element); commitRowChange?: ((params: any) =&gt; void) \| undefined; onChangeText?: ((search: string, params?: { ...; } \| undefined) =&gt; Promise&lt;...&gt;) \| undefined; renderFooter?: ((row: any) =&gt; any) \| undefined; } \| undefined` | ❌ | - |  |

---

## QuickSearch

**File:** `dataGrid/components/QuickSearch.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| placeholder | `string` | ❌ | - |  |
| columns | `any` | ✅ | - |  |
| rows | `any` | ✅ | - |  |
| setFilteredRows | `any` | ✅ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| setLoading | `((loading: boolean) =&gt; void)` | ❌ | - |  |
| onSearchTextChange | `((newSearchText: string) =&gt; void)` | ❌ | - |  |
| initialSearchText | `string` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## QuickSearchContainer

**File:** `dataGrid/components/QuickSearch.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| fullWidth | `boolean` | ❌ | - |  |

---

## QuickSearchTextArea

**File:** `dataGrid/components/QuickSearch.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `string` | ❌ | - | The label content. |
| mask | `any` | ❌ | - |  |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| dir | `enum` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| tabIndex | `number` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| inputType | `enum` | ❌ | - |  |
| inputSize | `enum` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onFocus" \| "onBlur" \| "onChange"; }` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## RTELinkDialog

**File:** `inputs/RichTextEditor/RTELinkDialog.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| open | `boolean` | ✅ | - |  |
| onClose | `() =&gt; void` | ✅ | - |  |
| onInsert | `(url: string, text?: string \| undefined, previewData?: LinkPreviewData \| undefined) =&gt; void` | ✅ | - |  |
| initialUrl | `string` | ❌ | - |  |
| initialText | `string` | ❌ | - |  |
| editorName | `string` | ✅ | - |  |
| onLinkPreview | `((url: string) =&gt; Promise&lt;LinkPreviewData \| null&gt;)` | ❌ | - |  |

---

## Radio

**File:** `inputs/radio/Radio.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - | Name attribute of the `input` element. |
| values | `RadioValuesProps[]` | ✅ | - |  |
| withGroup | `boolean` | ❌ | - |  |
| groupLabel | `string` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. |
| groupRowDirection | `boolean` | ❌ | - |  |
| InputProps | `{ [key: string]: string \| number; }` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| labelPlacement | `enum` | ❌ | - |  |
| checked | `boolean` | ❌ | - | If `true`, the component is checked. |
| value | `string \| null` | ❌ | - | The value of the component. The DOM API casts this to a string. |
| htmlFor | `string` | ❌ | - |  |
| radioGroupTextSize | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## RadioFilter

**File:** `dashboards/components/filters/RadioFilter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onFilterChange | `((params: any) =&gt; void)` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| cb | `((value: any, name: string) =&gt; void)` | ❌ | - |  |
| index | `number` | ❌ | - |  |
| position | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| filterType | `WidgetFilterTypes.RADIO` | ✅ | - |  |
| filterProps | `Omit&lt;RadioProps, "onChange"&gt;` | ✅ | - |  |

---

## RangeCalendarHeader

**File:** `pickers/components/RangeCalendarHeader.tsx`

*No props documented*

---

## ReadOnlyText

**File:** `form/components/FieldItem/fields/ReadOnlyText.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| type | `enum` | ✅ | - |  |
| fieldProps | `any` | ✅ | - |  |
| value | `any` | ❌ | - |  |
| displayFieldAsError | `boolean` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |

---

## Ready2PayCustomFooter

**File:** `pickers/components/Ready2PayCustomFooter.tsx`

*No props documented*

---

## ReadyToPayTemplate

ReadyToPay Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## RecurringInvoicesTemplate

RecurringInvoices Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Request

**File:** `dataGrid/mocks/Request.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## RichTextEditor

**File:** `inputs/RichTextEditor/RichTextEditor.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ✅ | - |  |
| label | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| options | `any` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| customToolbar | `ReactNode` | ❌ | - |  |
| onChange | `((content: any, files: FileInfo[]) =&gt; void)` | ❌ | - |  |
| onFileUpload | `((file: File) =&gt; Promise&lt;FileUploadResponse&gt;)` | ❌ | - |  |
| onFileRemove | `((fileId: string) =&gt; void)` | ❌ | - |  |
| onSubmit | `((content: any, files: FileInfo[]) =&gt; void)` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| maxHeight | `string` | ❌ | - |  |
| minHeight | `string` | ❌ | - |  |
| uploadMultiple | `boolean` | ❌ | - |  |
| acceptedFileTypes | `string[]` | ❌ | - |  |
| initialValue | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| onLinkPreview | `((url: string) =&gt; Promise&lt;LinkPreviewData \| null&gt;)` | ❌ | - |  |
| disabledToolbarButtons | `ToolbarButtonName[]` | ❌ | - |  |
| previewLine | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## RightMenuFilter

**File:** `dataList/components/RightMenuFilter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columns | `ColumnDef[]` | ✅ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| filterModel | `any` | ❌ | - |  |
| setFilterModel | `((newModel: GridFilterModel) =&gt; void)` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |

---

## RightMenuSorting

**File:** `dataList/components/RightMenuSorting.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columns | `ColumnDef[]` | ✅ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| sortModel | `GridSortModel` | ❌ | - |  |
| setSortModel | `((newModel: GridSortModel) =&gt; void)` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |

---

## SccIssueCardTemplate

SccIssueCard Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SccPendingTemplate

SccPending Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SccTransactionTemplate

SccTransaction Template

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| apiRef | `any` | ❌ | - | The ref object that allows grid manipulation. Can be instantiated with [[useGridApiRef()]]. |
| key | `any` | ❌ | - |  |
| gridMode | `enum` | ❌ | - |  |
| savingMode | `enum` | ❌ | - |  |
| forceSessionDataFilters | `boolean` | ❌ | - |  |
| enableUrlQueryFilter | `boolean` | ❌ | - |  |
| filterModel | `CustomFilterModel` | ❌ | - | Set the filter model of the grid. |
| sortModel | `GridSortModel` | ❌ | - | Set the sort model of the grid. |
| gridState | `GridState` | ❌ | - |  |
| columnVisibilityModel | `GridColumnVisibilityModel` | ❌ | - | Set the column visibility model of the grid. If defined, the grid will ignore the `hide` property in [[GridColDef]]. |
| headerModel | `HeaderModel` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| name | `string` | ✅ | - |  |
| id | `string` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| loadingText | `string` | ❌ | - |  |
| noResultMessage | `string \| null` | ❌ | - |  |
| noResultSubMessage | `string \| null` | ❌ | - |  |
| zeroStateCustomContent | `Element` | ❌ | - |  |
| columns | `ColumnDef[]` | ✅ | - | Set of columns of type [[GridColumns]]. |
| quickFilters | `QuickFiltersConfig[]` | ❌ | - |  |
| rows | `any[]` | ✅ | - | Set of rows of type [[GridRowsProp]]. |
| pageSizeOptions | `number[]` | ❌ | - | MUI X v6 alias for rowsPerPageOptions (kept for backward compatibility) |
| searchable | `boolean` | ❌ | - |  |
| disableColumnFilter | `boolean` | ❌ | - | If `true`, column filters are disabled. |
| disableColumnMenu | `boolean` | ❌ | - | If `true`, the column menu is disabled. |
| storageKey | `string` | ❌ | - |  |
| rowHeight | `enum` | ❌ | - | Set the height in pixel of a row in the grid. |
| rowLines | `enum` | ❌ | - |  |
| disableRowSelectionOnClick | `boolean` | ❌ | - | MUI X v6 alias for disableSelectionOnClick (kept for backward compatibility) |
| customActions | `GridAction[]` | ❌ | - |  |
| customElements | `CustomElements` | ❌ | - |  |
| shortcutEvents | `ShortcutEvents` | ❌ | - |  |
| bottomNotificationText | `string \| Element` | ❌ | - |  |
| dataListRowsFooterComponent | `ComponentType&lt;{}&gt;` | ❌ | - |  |
| footer | `FooterProps` | ❌ | - |  |
| hideToolbar | `boolean` | ❌ | - |  |
| hideFooter | `boolean` | ❌ | - | If `true`, the footer component is hidden. |
| dataListHideSelectAll | `boolean` | ❌ | - |  |
| hideToolbarButtons | `boolean` | ❌ | - |  |
| toolbarAnchor | `string \| number` | ❌ | - |  |
| resetGrid | `boolean` | ❌ | - |  |
| hasDrillDown | `boolean` | ❌ | - |  |
| ignoreSort | `boolean` | ❌ | - |  |
| enableInfinitScroll | `boolean` | ❌ | - |  |
| withRowActions | `boolean` | ❌ | - |  |
| withRowDeletion | `boolean` | ❌ | - |  |
| getIsRowDeletingUseCheckBoxFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| getRowDeletingIsCheckedFunc | `((row: any) =&gt; boolean)` | ❌ | - |  |
| onRowDeletionChecked | `((row: any, isChecked: boolean) =&gt; void)` | ❌ | - |  |
| isRowDeletingCheckAllEnabled | `boolean` | ❌ | - |  |
| isRowDeletingCheckAllChecked | `boolean` | ❌ | - |  |
| onRowDeletionCheckedAll | `((isChecked: boolean) =&gt; void)` | ❌ | - |  |
| withRowDeletionTooltipText | `string` | ❌ | - |  |
| allowDynamicRowHeight | `boolean` | ❌ | - |  |
| clearSessionData | `boolean` | ❌ | - |  |
| wrapGridHeaderLabels | `boolean` | ❌ | - |  |
| disableSessionDataFilters | `boolean` | ❌ | - |  |
| treeDataKeyPath | `string` | ❌ | - |  |
| hideTreeDataHeader | `boolean` | ❌ | - |  |
| hideChildSelection | `boolean` | ❌ | - |  |
| paintChildrenWithParent | `boolean` | ❌ | - |  |
| rowEditMode | `boolean` | ❌ | - |  |
| disabledRowOnSelection | `boolean` | ❌ | - |  |
| ignoreCellsOnDisable | `string[]` | ❌ | - |  |
| leftPinnedColumns | `string[]` | ❌ | - |  |
| rowReordering | `boolean` | ❌ | - | If `true`, the reordering of rows is enabled. |
| gridCustomStyle | `{ toolbar?: "default" \| "inline"; footer?: "default" \| "inline"; } \| undefined` | ❌ | - |  |
| onRowSelection | `((rows: any) =&gt; void)` | ❌ | - |  |
| onRowClick | `((row: any) =&gt; void)` | ❌ | - | Callback fired when a row is clicked. Not called if the target clicked is an interactive element added by the built-in columns. |
| onSelectionModelChange | `((newSelectionModel: any) =&gt; void)` | ❌ | - | Callback fired when the selection state of one or multiple rows changes. |
| onFilterModelChange | `((filterModel: GridFilterModel) =&gt; void)` | ❌ | - | Callback fired when the Filter model changes before the filters are applied. |
| onSortModelChange | `((sortModel: GridSortModel) =&gt; void)` | ❌ | - | Callback fired when the sort model changes before a column is sorted. |
| onGridStateChange | `((state: GridState, event?: string) =&gt; void)` | ❌ | - |  |
| onGridStateReset | `((gridState: GridState) =&gt; void)` | ❌ | - |  |
| gridEventLog | `((params: EventLogParams) =&gt; void)` | ❌ | - |  |
| onVisibleRowsChange | `((visibleRows: any) =&gt; void)` | ❌ | - |  |
| onGridUrlParams | `((readOnlyState: ReadOnlyState) =&gt; void)` | ❌ | - |  |
| onCellClick | `((params: any) =&gt; void)` | ❌ | - | Callback fired when any cell is clicked. |
| onMouseEnterRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onMouseLeaveRow | `((event: any, row: any) =&gt; void)` | ❌ | - |  |
| onDelete | `((row: any) =&gt; Promise&lt;boolean&gt;)` | ❌ | - |  |
| onRowOrderChange | `((params: { oldIndex: number; targetIndex: number; row: any; }) =&gt; void)` | ❌ | - | Callback fired when a row is being reordered. |
| dataListMode | `enum` | ❌ | - |  |
| withDataListInlineSearch | `boolean` | ❌ | - |  |
| getDataListConfigFunc | `((row: any, isSelected?: boolean) =&gt; MobileDataListRowData)` | ❌ | - |  |
| onDataListImageClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListInitialSortModel | `GridSortModel` | ❌ | - |  |
| dataListInitialFilterModel | `GridFilterModel` | ❌ | - |  |
| dataListTopNotifications | `DataListTag[]` | ❌ | - |  |
| dataListWithoutInlineScroll | `boolean` | ❌ | - |  |
| dataListWithSpecialScrollBehavior | `boolean` | ❌ | - |  |
| dataListWithImageDownloadTries | `boolean` | ❌ | - |  |
| dataListZeroStateType | `enum` | ❌ | - |  |
| dataListZeroStateCustomContent | `Element` | ❌ | - |  |
| dataListNoResultMessage | `string \| null` | ❌ | - |  |
| dataListNoResultSubMessage | `string \| null` | ❌ | - |  |
| dataListOptionalRowsList | `string[]` | ❌ | - | When supplied, a list of template names that will be forwarded to the underlying mobile DataList component so the user can create new rows from these templates. |
| dataListOnOptionalRowSelected | `((rowName: string) =&gt; void)` | ❌ | - | Function that returns the default row object when creating a new line from a template name. |
| dataListCanAddNewLine | `boolean` | ❌ | - |  |
| onAfterEditGridLastRowAndLastCell | `(() =&gt; void)` | ❌ | - |  |
| dataListSetTableField | `((row: any, field: string, value: any) =&gt; any)` | ❌ | - |  |
| dataListOnEnterEditMode | `(() =&gt; void)` | ❌ | - |  |
| dataListOnRevertEditMode | `(() =&gt; void)` | ❌ | - |  |
| isMobileApp | `boolean` | ❌ | - |  |
| dataListOnDeleteRowClick | `((row: any) =&gt; void)` | ❌ | - |  |
| dataListWithEditMode | `boolean` | ❌ | - |  |
| maxVisibleColumns | `number` | ❌ | - |  |
| enablePinnedColumns | `boolean` | ❌ | - |  |
| bulkEdit | `boolean` | ❌ | - |  |
| bulkEditValidation | `BulkEditValidator[]` | ❌ | - |  |
| onBulkEditApply | `((values: Record&lt;string, any&gt;, selectedRows: any[]) =&gt; boolean \| Promise&lt;boolean&gt;)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SearchBasicEditRenderer

**File:** `dataGrid/renderers/search/search_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SearchEditRenderer

**File:** `dataGrid/renderers/search/search_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Select

**File:** `select/Select.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| multiple | `boolean` | ❌ | - | If `true`, `value` must be an array and the menu will support multiple selections. |
| canAddValues | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| name | `string` | ❌ | - |  |
| ref | `any` | ❌ | - |  |
| inputValue | `any` | ❌ | - | The input value. |
| options | `SelectOption[]` | ✅ | - | Array of options. |
| getOptions | `(() =&gt; Promise&lt;any&gt;)` | ❌ | - |  |
| onGetOptions | `((options: SelectOption[]) =&gt; void)` | ❌ | - |  |
| forceGetOption | `boolean` | ❌ | - |  |
| validationForAddedValues | `((value: SelectValueType) =&gt; { isValid: boolean; failMessage?: string; })` | ❌ | - |  |
| onChange | `((newValue: any, event?: ChangeEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - | Callback fired when the value changes. |
| onAddValue | `((newValue: SelectOption) =&gt; void)` | ❌ | - |  |
| onDelete | `((newValue: string \| SelectOption \| SelectOption[] \| null, event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((newValue: SelectOption \| SelectOption[] \| null, event?: ChangeEvent&lt;HTMLInputElement&gt;) =&gt; void) \| undefined` | ❌ | - |  |
| onBlur | `((newValue: SelectOption \| SelectOption[] \| null, event?: ChangeEvent&lt;HTMLInputElement&gt;) =&gt; void) \| undefined` | ❌ | - |  |
| onClose | `((value: SelectOption \| SelectOption[] \| null) =&gt; void)` | ❌ | - | Callback fired when the popup requests to be closed. Use in controlled mode (see open). |
| renderInput | `((params: AutocompleteRenderInputParams) =&gt; ReactNode)` | ❌ | - | Render the input. |
| label | `string` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| valueProp | `SelectOption \| SelectOption[] \| null` | ❌ | - |  |
| inputInitialValue | `string` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| disableClearable | `boolean` | ❌ | - | If `true`, the input can't be cleared. |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| hidePopupIcon | `boolean` | ❌ | - |  |
| open | `boolean` | ❌ | - | If `true`, the component is shown. |
| isFilter | `boolean` | ❌ | - |  |
| styleProps | `any` | ❌ | - |  |
| numberOfOptionsToDisplay | `number` | ❌ | - |  |
| error | `string` | ❌ | - |  |
| maxWidth | `number` | ❌ | - |  |
| selectSize | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| limitSelectedOptions | `number` | ❌ | - |  |
| hideInput | `boolean` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - | If `true`, the component becomes readonly. It is also supported for multiple tags where the tag cannot be deleted. |
| tabIndex | `number` | ❌ | - |  |
| highlightedText | `boolean` | ❌ | - |  |
| highlightedTextColor | `string` | ❌ | - |  |
| enableSelectAll | `boolean` | ❌ | - |  |
| enableSelectAllText | `string` | ❌ | - |  |
| sortByLabel | `boolean` | ❌ | `true` | Sorts options alphabetically by label. @note Only one sorting option can be used at a time (sortByLabel, sortByLabelWithTop, or sortByKeyAndLabel) |
| sortByLabelWithTop | `boolean` | ❌ | `false` | Sorts options alphabetically but keeps topSorting items at the top. @note Only one sorting option can be used at a time (sortByLabel, sortByLabelWithTop, or sortByKeyAndLabel) |
| sortByKeyAndLabel | `boolean` | ❌ | `false` | Sorts options alphanumerically by key + label combined (e.g., "A001 Widget" before "B002 Gadget"). Useful when options display a key/code alongside the label. @note Only one sorting option can be used at a time (sortByLabel, sortByLabelWithTop, or sortByKeyAndLabel) |
| ignoreAddValueLabel | `boolean` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| descriptionTextAsSubText | `boolean` | ❌ | - |  |
| filterByMultipleWords | `boolean` | ❌ | - |  |
| serverSide | `UseSelectProps` | ❌ | - |  |
| hideTags | `boolean` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| startIcon | `IconProps` | ❌ | - |  |
| endAction | `Element` | ❌ | - |  |
| clearValueOnClose | `boolean` | ❌ | - |  |
| density | `string` | ❌ | - |  |
| disableSetValueOnReset | `boolean` | ❌ | - |  |
| preventVirtualized | `boolean` | ❌ | - |  |
| isFormElement | `boolean` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| distinctLabels | `boolean` | ❌ | - |  |
| preventCloseOnBlur | `boolean` | ❌ | - | When true, prevent closing on blur/toggleInput if input has focus (used by filters). |
| onClick | `((event: MouseEvent&lt;HTMLInputElement, MouseEvent&gt;) =&gt; void)` | ❌ | - | Optional click handler for input; forwarded to the underlying input element. |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SelectAllSection

**File:** `dataGrid/components/QuickSearch.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| style | `CSSProperties` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| onClick | `((e: any) =&gt; void)` | ❌ | - |  |
| onMouseEnter | `((e: any) =&gt; void)` | ❌ | - |  |
| onMouseLeave | `((e: any) =&gt; void)` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| direction | `enum` | ❌ | - |  |
| alignItems | `enum` | ❌ | - |  |
| justifyContent | `enum` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| flex | `number \| "unset"` | ❌ | - |  |
| customStyle | `any` | ❌ | - |  |
| gap | `number` | ❌ | - |  |

---

## SelectBasicEditCellRenderer

**File:** `dataGrid/renderers/select/select_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| filterProps | `FilterProps` | ✅ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SelectEditCellRenderer

**File:** `dataGrid/renderers/select/select_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| filterProps | `FilterProps` | ✅ | - |  |
| showLabel | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SelectField

**File:** `form/components/FieldItem/fields/SelectField.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| isLoading | `boolean` | ❌ | - |  |
| testProps | `any` | ❌ | - |  |
| displayFieldAsError | `boolean` | ❌ | - |  |
| showUpdateFlag | `boolean` | ❌ | - |  |
| multiple | `boolean` | ❌ | - | If `true`, `value` must be an array and the menu will support multiple selections. |
| canAddValues | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| name | `string` | ❌ | - |  |
| ref | `any` | ❌ | - |  |
| inputValue | `any` | ❌ | - | The input value. |
| options | `SelectOption[]` | ✅ | - | Array of options. |
| getOptions | `(() =&gt; Promise&lt;any&gt;)` | ❌ | - |  |
| onGetOptions | `((options: SelectOption[]) =&gt; void)` | ❌ | - |  |
| forceGetOption | `boolean` | ❌ | - |  |
| validationForAddedValues | `((value: SelectValueType) =&gt; { isValid: boolean; failMessage?: string; })` | ❌ | - |  |
| onChange | `((newValue: any, event?: ChangeEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - | Callback fired when the value changes. |
| onAddValue | `((newValue: SelectOption) =&gt; void)` | ❌ | - |  |
| onDelete | `((newValue: string \| SelectOption \| SelectOption[] \| null, event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((newValue: SelectOption \| SelectOption[] \| null, event?: ChangeEvent&lt;HTMLInputElement&gt;) =&gt; void) \| undefined` | ❌ | - |  |
| onBlur | `((newValue: SelectOption \| SelectOption[] \| null, event?: ChangeEvent&lt;HTMLInputElement&gt;) =&gt; void) \| undefined` | ❌ | - |  |
| onClose | `((value: SelectOption \| SelectOption[] \| null) =&gt; void)` | ❌ | - | Callback fired when the popup requests to be closed. Use in controlled mode (see open). |
| renderInput | `((params: AutocompleteRenderInputParams) =&gt; ReactNode)` | ❌ | - | Render the input. |
| label | `string` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| valueProp | `SelectOption \| SelectOption[] \| null` | ❌ | - |  |
| inputInitialValue | `string` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| disableClearable | `boolean` | ❌ | - | If `true`, the input can't be cleared. |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| hidePopupIcon | `boolean` | ❌ | - |  |
| open | `boolean` | ❌ | - | If `true`, the component is shown. |
| isFilter | `boolean` | ❌ | - |  |
| styleProps | `any` | ❌ | - |  |
| numberOfOptionsToDisplay | `number` | ❌ | - |  |
| error | `string` | ❌ | - |  |
| maxWidth | `number` | ❌ | - |  |
| selectSize | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| limitSelectedOptions | `number` | ❌ | - |  |
| hideInput | `boolean` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - | If `true`, the component becomes readonly. It is also supported for multiple tags where the tag cannot be deleted. |
| tabIndex | `number` | ❌ | - |  |
| highlightedText | `boolean` | ❌ | - |  |
| highlightedTextColor | `string` | ❌ | - |  |
| enableSelectAll | `boolean` | ❌ | - |  |
| enableSelectAllText | `string` | ❌ | - |  |
| sortByLabel | `boolean` | ❌ | `true` | Sorts options alphabetically by label. @note Only one sorting option can be used at a time (sortByLabel, sortByLabelWithTop, or sortByKeyAndLabel) |
| sortByLabelWithTop | `boolean` | ❌ | `false` | Sorts options alphabetically but keeps topSorting items at the top. @note Only one sorting option can be used at a time (sortByLabel, sortByLabelWithTop, or sortByKeyAndLabel) |
| sortByKeyAndLabel | `boolean` | ❌ | `false` | Sorts options alphanumerically by key + label combined (e.g., "A001 Widget" before "B002 Gadget"). Useful when options display a key/code alongside the label. @note Only one sorting option can be used at a time (sortByLabel, sortByLabelWithTop, or sortByKeyAndLabel) |
| ignoreAddValueLabel | `boolean` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| descriptionTextAsSubText | `boolean` | ❌ | - |  |
| filterByMultipleWords | `boolean` | ❌ | - |  |
| serverSide | `UseSelectProps` | ❌ | - |  |
| hideTags | `boolean` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| startIcon | `IconProps` | ❌ | - |  |
| endAction | `Element` | ❌ | - |  |
| clearValueOnClose | `boolean` | ❌ | - |  |
| density | `string` | ❌ | - |  |
| disableSetValueOnReset | `boolean` | ❌ | - |  |
| preventVirtualized | `boolean` | ❌ | - |  |
| isFormElement | `boolean` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| distinctLabels | `boolean` | ❌ | - |  |
| preventCloseOnBlur | `boolean` | ❌ | - | When true, prevent closing on blur/toggleInput if input has focus (used by filters). |
| onClick | `((event: MouseEvent&lt;HTMLInputElement, MouseEvent&gt;) =&gt; void)` | ❌ | - | Optional click handler for input; forwarded to the underlying input element. |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SelectFilter

**File:** `dataGrid/filters/select_filter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| filterRef | `MutableRefObject&lt;any&gt;` | ❌ | - |  |
| customFieldName | `string` | ✅ | - |  |
| filterType | `enum` | ✅ | - |  |
| pinned | `boolean` | ❌ | - |  |
| freeText | `boolean` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| id | `string` | ✅ | - |  |
| type | `string` | ❌ | - |  |
| apiRef | `any` | ✅ | - |  |
| label | `string` | ✅ | - |  |
| field | `string` | ✅ | - | The column identifier. It's used to map with [[GridRowModel]] values. |
| rows | `any` | ✅ | - |  |
| columns | `any` | ✅ | - |  |
| options | `SelectOption[]` | ❌ | - |  |
| getOptions | `(() =&gt; Promise&lt;any&gt;)` | ❌ | - |  |
| filterProps | `any` | ✅ | - |  |
| filterModel | `any` | ✅ | - |  |
| triggerOnChange | `boolean` | ❌ | - |  |
| onFilterChanged | `((filterModel: GridFilterModel, inputEl?: HTMLInputElement \| null) =&gt; void)` | ❌ | - |  |
| getFilterModel | `() =&gt; any` | ✅ | - |  |
| quickFilter | `QuickFiltersConfig` | ❌ | - |  |
| iconProps | `IconProps` | ❌ | - |  |
| headerProps | `HeaderProps` | ❌ | - |  |
| dateProps | `DateProps` | ❌ | - |  |
| selectProps | `GridSelectProps` | ❌ | - |  |
| textProps | `TextProps` | ❌ | - |  |
| numberProps | `NumberProps` | ❌ | - |  |
| currencyProps | `CurrencyProps` | ❌ | - |  |
| linkProps | `LinkProps` | ❌ | - |  |
| getter | `enum` | ❌ | - |  |
| ignoreCellClick | `boolean` | ❌ | - |  |
| isFirst | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| boldText | `boolean` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| autoGeneratedOptions | `boolean` | ❌ | - |  |
| popper | `Element` | ❌ | - |  |
| badge | `boolean` | ❌ | - |  |
| tooltip | `boolean` | ❌ | - |  |
| inputAutoEvents | `InputAutoEvents` | ❌ | - |  |
| searchFilter | `boolean` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| visible | `boolean` | ❌ | - |  |
| hideIfEmpty | `boolean` | ❌ | - |  |
| hideOnMobile | `boolean` | ❌ | - |  |
| mobile | `ColumnMobileConfig` | ❌ | - |  |
| allowBulkEdit | `boolean` | ❌ | - |  |
| onClick | `((row: any, params?: any) =&gt; void)` | ❌ | - |  |
| onChange | `((row: any, props: any, apiRef: any) =&gt; void)` | ❌ | - |  |
| validateInput | `((props: any) =&gt; ValidationResult)` | ❌ | - |  |
| preProcessProps | `((props: any) =&gt; any)` | ❌ | - |  |
| searchProps | `{ columnsToHide?: string[]; renderCellContent?: ((params: any) =&gt; Element); commitRowChange?: ((params: any) =&gt; void) \| undefined; onChangeText?: ((search: string, params?: { ...; } \| undefined) =&gt; Promise&lt;...&gt;) \| undefined; renderFooter?: ((row: any) =&gt; any) \| undefined; } \| undefined` | ❌ | - |  |

---

## SelectFilterBase

**File:** `select/SelectFilterBase.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| SelectComponent | `any` | ❌ | - | The select component to render |
| valueProp | `SelectOption \| SelectOption[]` | ❌ | - | Current selected value |
| options | `SelectOption[]` | ✅ | - | Available options |
| onChange | `(value: SelectOption \| SelectOption[] \| null, event?: ChangeEvent&lt;HTMLInputElement&gt; \| undefined) =&gt; void` | ✅ | - | Callback when value changes |
| onKeyDown | `((value: any, event: any) =&gt; void)` | ❌ | - | Callback when key is pressed |
| multiple | `boolean` | ❌ | - | Whether this is a multiple select |
| label | `string` | ✅ | - | Label for the filter |
| field | `string` | ✅ | - | Field name |
| selectProps | `any` | ❌ | - | Props to pass to the Select component |
| sortByLabel | `boolean` | ❌ | - | Sort options by label |
| testIdPrefix | `string` | ❌ | - | Test ID prefix |
| filterType | `string` | ❌ | - | Filter type for width computation |
| getOptions | `(() =&gt; Promise&lt;any&gt;)` | ❌ | - | Get options dynamically |

---

## SelectFilterSearchTextArea

**File:** `dataGrid/components/QuickSearch.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `string` | ❌ | - | The label content. |
| mask | `any` | ❌ | - |  |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| dir | `enum` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| tabIndex | `number` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| inputType | `enum` | ❌ | - |  |
| inputSize | `enum` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onFocus" \| "onBlur" \| "onChange"; }` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SelectMenu

**File:** `select-menu/SelectMenu.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| buttonProps | `Omit&lt;ButtonProps, "onClick"&gt;` | ✅ | - |  |
| selectProps | `SelectProps` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| enableToggle | `boolean` | ❌ | - |  |
| onToggle | `((toggled: boolean) =&gt; void)` | ❌ | - |  |
| toggleButtonProps | `Partial&lt;ButtonProps&gt;` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SelectRenderer

**File:** `dataList/renderers/select/select_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## ServerFormBox

**File:** `form/demos/ServerFormBox.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| formStyle | `CSSProperties` | ❌ | - |  |
| getInputsRefs | `((inputsRefs: any) =&gt; void)` | ❌ | - |  |
| onChange | `((element: any, inputsRefs?: any, formikForm?: any) =&gt; void)` | ❌ | - |  |
| formSchemaSections | `FormSchemaSection[]` | ✅ | - |  |
| onSubmit | `(values: FormikValues, formikHelpers?: FormikHelpers&lt;FormikValues&gt; \| undefined) =&gt; void \| Promise&lt;any&gt;` | ✅ | - | Submission handler |
| footer | `FormFooterProps` | ❌ | - |  |
| customSchema | `any` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| validate | `((values: FormikValues, refs?: any) =&gt; void \| object \| Promise&lt;FormikErrors&lt;FormikValues&gt;&gt;)` | ❌ | - | Validation function. Must return an error object or promise that throws an error object where that object keys map to corresponding value. |
| gridDirection | `enum` | ❌ | - |  |
| numberOfSkeletonFields | `number` | ❌ | - |  |
| formError | `boolean` | ❌ | - |  |
| fieldsWrapperStyle | `CSSProperties` | ❌ | - |  |
| variation | `enum` | ❌ | - |  |
| boxProps | `BoxProps` | ❌ | - |  |
| asWizard | `boolean` | ❌ | - |  |
| wizardProps | `{ asTabs?: boolean; tabsProps?: Partial&lt;TabsProps&gt;; currentStep?: number \| undefined; onStepChange?: ((step: number) =&gt; void) \| undefined; withStepper?: boolean \| undefined; } \| undefined` | ❌ | - |  |

---

## SideMenuFilters

**File:** `dataGrid/components/filters/SideMenuFilters.tsx`

*No props documented*

---

## SidePanel

**File:** `sidePanel/SidePanel.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| list | `SidePanelMenuItem[]` | ❌ | - |  |
| selectedListItem | `SidePanelMenuItem` | ❌ | - |  |
| children | `((Element \| Element[]) & (boolean \| ReactChild \| ReactFragment \| ReactPortal \| null))` | ❌ | - | The content of the component. |
| drawerWidth | `number` | ❌ | - |  |
| onListItemClick | `((item: SidePanelMenuItem) =&gt; void)` | ❌ | - |  |
| open | `boolean` | ❌ | - | If `true`, the component is shown. |
| anchor | `enum` | ❌ | - |  |
| offsetTop | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SimpleBarChart

**File:** `SimpleBarChart/SimpleBarChart.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| segments | `CommonSegmentProps[]` | ✅ | - |  |
| title | `{ label: string; textColor?: TextColor; }` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| customColors | `string[]` | ❌ | - |  |
| withExpendCollapse | `boolean` | ❌ | - |  |
| initiallyExpanded | `boolean` | ❌ | - |  |
| numberAreaFormat | `enum` | ✅ | - |  |

---

## Skeleton

**File:** `skeleton/Skeleton.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SkeletonChart

**File:** `charts/SkeletonChart.tsx`

*No props documented*

---

## Snackbar

**File:** `snackbar/Snackbar.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| action | `Element` | ❌ | - | The action to display. It renders after the message, at the end of the snackbar. |
| message | `string \| Element` | ✅ | - | The message to display. |
| snackbarType | `enum` | ❌ | - |  |
| autoHideDuration | `number \| null` | ❌ | - | The number of milliseconds to wait before automatically calling the `onClose` function. `onClose` should then set the state of the `open` prop to hide the Snackbar. This behavior is disabled by default with the `null` value. |
| actionType | `enum` | ❌ | - |  |
| buttonLabel | `string` | ❌ | - |  |
| buttonProgressbar | `boolean` | ❌ | - |  |
| progressbar | `boolean` | ❌ | - |  |
| progressbarCount | `number \| null` | ❌ | - |  |
| anchorPosition | `enum` | ❌ | - |  |
| open | `boolean` | ❌ | - | If `true`, the component is shown. |
| error | `boolean` | ❌ | - |  |
| onClose | `((event?: Event \| SyntheticEvent&lt;any, Event&gt;, reason?: string) =&gt; void) \| undefined` | ❌ | - | Callback fired when the component requests to be closed. Typically `onClose` is used to set state in the parent component, which is used to control the `Snackbar` `open` prop. The `reason` parameter can optionally be used to control the response to `onClose`, for example ignoring `clickaway`. |
| onOpen | `((event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| onActionButtonClick | `((event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SortableDraggableItem

A reusable component that provides drag-and-drop and pinning functionality.
Can be used with any content (checkboxes, filters, etc.)

**File:** `dataGrid/components/SortableDraggableItem.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ✅ | - | Unique identifier for the draggable item |
| children | `ReactNode` | ❌ | - | The main content to render (checkbox, filter, etc.) |
| isPinnedLeft | `boolean` | ❌ | - | Whether the item is pinned to the left |
| isPinnedRight | `boolean` | ❌ | - | Whether the item is pinned to the right |
| onPin | `((id: string, side: "left" \| "right") =&gt; void)` | ❌ | - | Callback when pinning an item |
| onUnpin | `((id: string) =&gt; void)` | ❌ | - | Callback when unpinning an item |
| pinDisabled | `boolean` | ❌ | `false` | Whether the pin button is disabled |
| pinTooltip | `string` | ❌ | - | Custom tooltip text for pin button |
| showPinButton | `boolean` | ❌ | `true` | Whether to show the pin button |
| draggable | `boolean` | ❌ | `true` | Whether the item is draggable (must be within SortableContext if true) |
| type | `enum` | ❌ | - | The type of the item (column, filter, etc.) |

---

## SortableProgressArrow

**File:** `ArrowProgressBar/components/SortableProgressArrow.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| step | `ProgressStepProps&lt;any&gt;` | ✅ | - |  |
| index | `number` | ✅ | - |  |
| isFirst | `boolean` | ✅ | - |  |
| isLast | `boolean` | ✅ | - |  |
| progressBarType | `enum` | ❌ | - |  |
| onDelete | `((step: ProgressStepProps&lt;any&gt;) =&gt; void)` | ❌ | - |  |
| onClick | `((stepId: string) =&gt; void)` | ❌ | - |  |
| isScrolling | `boolean` | ❌ | - |  |

---

## Spinner

**File:** `spinner/Spinner.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| text | `string` | ❌ | - |  |
| size | `number` | ❌ | `50` |  |
| type | `enum` | ❌ | `gradient` |  |
| withOverlay | `boolean` | ❌ | `false` |  |
| position | `enum` | ❌ | `center` |  |
| color | `enum` | ❌ | `neutral_80` |  |
| hideToolbar | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Status

**File:** `status/Status.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| status | `enum` | ✅ | - |  |
| text | `string` | ✅ | - |  |
| mobileContent | `Element` | ✅ | - |  |
| customIcon | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## StatusRenderer

**File:** `dataGrid/renderers/status/status_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |

---

## StatusTag

**File:** `statusTag/StatusTag.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| status | `enum` | ✅ | - |  |
| text | `string` | ✅ | - |  |
| customIcon | `string` | ❌ | - |  |
| size | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| isAccordion | `boolean` | ❌ | - |  |
| moreInfo | `MoreInfoSection[]` | ❌ | - |  |
| defaultExpanded | `boolean` | ❌ | - |  |
| maxVisibleSections | `number` | ❌ | - |  |
| maxVisibleLines | `number` | ❌ | - |  |
| onDismissLink | `LinkProps` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## StickyDialog

**File:** `StickyDialog/StickyDialog.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| open | `boolean` | ❌ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| children | `ReactNode` | ❌ | - | Dialog children, usually the included sub-components. |
| anchorId | `string` | ❌ | - |  |
| anchorEl | `HTMLElement \| null` | ❌ | - |  |
| anchorOrigin | `PopoverOrigin` | ❌ | - |  |
| transformOrigin | `PopoverOrigin` | ❌ | - |  |
| maxWidth | `string \| number` | ❌ | - |  |
| minWidth | `string \| number` | ❌ | - |  |
| padding | `string \| number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| content | `any` | ❌ | - |  |
| type | `enum` | ❌ | - |  |
| titleProps | `Omit&lt;TextProps, "children" \| "ref"&gt;` | ❌ | - |  |
| titlePosition | `enum` | ❌ | - |  |
| subTitle | `string` | ❌ | - |  |
| buttons | `DialogButtonsProps` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| minHeight | `number` | ❌ | - |  |
| maxHeight | `number` | ❌ | - |  |
| contentAlignment | `enum` | ❌ | - |  |
| onCloseCb | `(() =&gt; void)` | ❌ | - |  |
| onSave | `(() =&gt; void)` | ❌ | - |  |
| onReject | `(() =&gt; void)` | ❌ | - |  |
| closeOnBackDropClick | `boolean` | ❌ | - |  |
| disableCloseButton | `boolean` | ❌ | - |  |
| legacyUI | `boolean` | ❌ | - |  |
| bgImage | `string` | ❌ | - |  |
| mobileTopGap | `number` | ❌ | - |  |
| customStyleDialogContent | `CSSProperties` | ❌ | - |  |
| drawerProps | `Omit&lt;DrawerProps, "dir"&gt;` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## StickyMenuPopup

**File:** `mobile/stickyMenuPopup/StickyMenuPopup.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| show | `boolean` | ✅ | - |  |
| title | `string` | ❌ | - |  |
| items | `MenuAction[]` | ❌ | - |  |
| onClose | `(() =&gt; void)` | ❌ | - |  |
| notifyOnClick | `(() =&gt; void)` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| hideTitle | `boolean` | ❌ | - |  |
| showCloseButton | `boolean` | ❌ | - |  |
| drawerProps | `Omit&lt;DrawerProps, "dir"&gt;` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## StyledDatePicker

**File:** `dataGrid/renderers/date/date_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| footer | `any` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| title | `string` | ❌ | - |  |
| mask | `string` | ❌ | - | Props applied to input text element. @deprecated sending mask is no longer needed. |
| onChange | `(date: Date, keyboardInputValue?: string \| undefined) =&gt; void` | ✅ | - |  |
| onError | `((reason: string, value: string) =&gt; void)` | ❌ | - |  |
| shouldDisableDate | `((date: Date \| null) =&gt; boolean)` | ❌ | - |  |
| onClose | `((value?: TDate) =&gt; void)` | ❌ | - |  |
| onAccept | `((value: TDate) =&gt; void)` | ❌ | - |  |
| disableFuture | `boolean` | ❌ | - | If `true`, disable values after the current date for date components, time for time components and both for date time components. |
| className | `string` | ❌ | - | Class name applied to the root element. |
| readOnly | `boolean` | ❌ | - |  |
| inputRef | `any` | ❌ | - | Pass a ref to the `input` element. |
| name | `string` | ❌ | - | Name attribute used by the `input` element in the Field. |
| onOpen | `(() =&gt; void)` | ❌ | - | Callback fired when the popup requests to be opened. Use in controlled mode (see `open`). |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| startRange | `TDate` | ❌ | - |  |
| endRange | `TDate` | ❌ | - |  |
| inputFormat | `enum` | ❌ | - |  |
| displayFormat | `enum` | ❌ | - |  |
| monthAndYearView | `DatePickerView[]` | ❌ | - |  |
| dateFormat | `string` | ❌ | - | Props applied to previous dateFormat is no longer needed. @deprecated Use inputFormat instead. |
| timeSpecific | `string` | ❌ | - |  |
| initialValue | `TDate` | ❌ | - |  |
| monthYearView | `boolean` | ❌ | - |  |
| disableWeekends | `boolean` | ❌ | - |  |
| holidays | `TDate[]` | ❌ | - |  |
| enablePast | `boolean` | ❌ | - |  |
| disableCloseOnSelect | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| startOrEndOfTheMonth | `enum` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| shortYear | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| popperRef | `any` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| isFilter | `boolean` | ❌ | - |  |
| skipPickerButtonOnFocus | `boolean` | ❌ | - |  |
| hidePickerIcon | `boolean` | ❌ | - |  |
| onApply | `((value: Date) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onEnter | `((value: TDate) =&gt; void)` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| pickerType | `enum` | ❌ | - |  |
| pickerSize | `enum` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| inlineLabel | `Element` | ❌ | - |  |
| $focused | `boolean` | ❌ | - |  |

---

## StyledPickersDay

**File:** `pickers/components/CustomDay.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| isFirstDay | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| isLastDay | `boolean` | ❌ | - |  |
| isInRange | `boolean` | ❌ | - |  |
| isDisabled | `boolean` | ❌ | - |  |
| disableMargin | `boolean` | ❌ | - | If `true`, days are rendering without margin. Useful for displaying linked range of days. |

---

## StyledSelect

**File:** `dataGrid/renderers/select/select_edit.tsx`

*No props documented*

---

## StyledText

**File:** `dataGrid/renderers/text/text_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `string` | ❌ | - | The label content. |
| mask | `any` | ❌ | - |  |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| ref | `any` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| tabIndex | `number` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| inputType | `enum` | ❌ | - |  |
| inputSize | `enum` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onFocus" \| "onBlur" \| "onChange"; }` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## StyledTextInput

**File:** `dataGrid/renderers/currency/currency_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `string` | ❌ | - | The label content. |
| mask | `any` | ❌ | - |  |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| dir | `enum` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| tabIndex | `number` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| inputType | `enum` | ❌ | - |  |
| inputSize | `enum` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| withForm | `boolean` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onFocus" \| "onBlur" \| "onChange"; }` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## StyledZeroStateMainIcon

**File:** `ZeroState/ZeroState.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| $width | `number` | ✅ | - |  |
| $height | `number` | ✅ | - |  |

---

## Swiper

**File:** `swiper/Swiper.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ✅ | - |  |
| slides | `SwiperSlideProps[]` | ✅ | - |  |
| alignNavigationButtons | `enum` | ❌ | - |  |
| slideToSelectedSlide | `boolean` | ❌ | - |  |
| navigationButtonsBackground | `enum` | ❌ | - |  |
| showSwiper | `boolean` | ❌ | - |  |
| onSlideChange | `((swiper?: any) =&gt; any)` | ❌ | - | Event will be fired when currently active slide is changed |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SwiperNavigationBtn

**File:** `swiper/components/SwiperNavigationBtn.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| type | `enum` | ✅ | - |  |
| selectedSlide | `SelectedSlideType` | ❌ | - |  |
| alignNavigationButtons | `enum` | ❌ | - |  |
| navigationButtonsBackground | `enum` | ❌ | - |  |
| setShowSwiper | `(show: boolean) =&gt; void` | ✅ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Switch

**File:** `switch/Switch.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `string` | ❌ | - |  |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| checkedIcon | `string` | ❌ | - |  |
| icon | `string` | ❌ | - |  |
| switchType | `enum` | ❌ | - |  |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| offLabel | `string` | ❌ | - |  |
| onLabel | `string` | ❌ | - |  |
| defaultChecked | `boolean` | ❌ | - | The default checked state. Use when the component is not controlled. |
| labelPlacement | `enum` | ❌ | - |  |
| groupRowDirection | `boolean` | ❌ | - |  |
| values | `SwitchValue[]` | ❌ | - |  |
| checked | `boolean` | ❌ | - | If `true`, the component is checked. |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, value?: boolean \| SwitchValue[]) =&gt; void)` | ❌ | - | Callback fired when the state is changed. |
| inputProps | `any` | ❌ | - | [Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Attributes) applied to the `input` element. |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## SwitchFilter

**File:** `dashboards/components/filters/SwitchFilter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onFilterChange | `((params: any) =&gt; void)` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| cb | `((value: any, name: string) =&gt; void)` | ❌ | - |  |
| index | `number` | ❌ | - |  |
| position | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| filterType | `DashboardFilterTypes.SWITCH` | ✅ | - |  |
| filterProps | `Omit&lt;SwitchProps, "onChange"&gt;` | ✅ | - |  |

---

## Tab

**File:** `tabs/Tab/Tab.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | `string` | ✅ | - |  |
| selected | `boolean` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| content | `Element` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| index | `number` | ❌ | - |  |
| counter | `number` | ❌ | - |  |
| counterType | `enum` | ❌ | - |  |
| counterTooltip | `{ title?: string \| Element; }` | ❌ | - |  |
| onClick | `((event: MouseEvent&lt;HTMLDivElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| ref | `any` | ❌ | - |  |
| tabsType | `enum` | ❌ | - |  |
| orientation | `enum` | ❌ | - |  |
| icon | `string \| Element` | ❌ | - |  |
| href | `string` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| beforeAndAfterMobileSpace | `string` | ❌ | - |  |
| actions | `ButtonProps[]` | ❌ | - |  |
| tabHeader | `string` | ❌ | - |  |
| tabTextColor | `enum` | ❌ | - |  |
| showWarnings | `boolean` | ❌ | - |  |
| infoTooltip | `TooltipProps` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TabPanel

**File:** `tabs/TabPanel/TabPanel.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| tab | `TabProps` | ✅ | - |  |
| className | `string` | ❌ | - |  |
| index | `number \| null` | ✅ | - |  |
| value | `number \| null` | ✅ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Table

**File:** `dashboards/widgets/Table/Table.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| ref | `any` | ❌ | - |  |
| id | `string` | ❌ | - |  |
| widgetStamp | `string` | ❌ | - |  |
| type | `enum` | ✅ | - |  |
| name | `string` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| titleJSX | `ReactNode` | ❌ | - | Optional custom content rendered directly under the title row. Useful for dynamic KPIs like a bold number summary (e.g., 70). |
| titleTooltip | `TooltipProps` | ❌ | - |  |
| subTitle | `string` | ❌ | - |  |
| rightTitle | `string` | ❌ | - |  |
| widgetFilters | `WidgetFilter&lt;WidgetFiltersProps&gt;[]` | ❌ | - | Deprecated: use `filters` instead |
| filters | `WidgetFilter&lt;WidgetFiltersProps&gt;[] \| { items: WidgetFilter&lt;WidgetFiltersProps&gt;[]; }` | ❌ | - | Widget-level filters (e.g., View By) Supports new object shape with items, and legacy array for backward compatibility. |
| withPreview | `boolean` | ❌ | - |  |
| pending | `boolean` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| orientation | `enum` | ❌ | - |  |
| legendProps | `any` | ❌ | - |  |
| applyFilters | `((params: any) =&gt; void)` | ❌ | - |  |
| onWidgetFilterChange | `((filters: Record&lt;string, any&gt;, current?: { name: string; value: any; }) =&gt; any)` | ❌ | - | Called whenever a widget filter changes. Return partial widget props to re-render (same pattern as `widgetTypes.onChangeType`). |
| showAsTableClick | `((params: any) =&gt; void)` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| isWidget | `boolean` | ❌ | - |  |
| widgetTypes | `{ options: ToggleOption[]; value?: string; onChangeType?: ((index: number, value: string) =&gt; any); disabled?: boolean \| undefined; size?: "small" \| "medium" \| "large" \| undefined; fullWidth?: boolean \| undefined; } \| undefined` | ❌ | - | Optional toggle to switch widget types/configurations. When provided, a Toggle will render in the widget header and call onChangeType. |
| autoEnabledCustumization | `boolean` | ❌ | - | Internal flag to suppress edit-mode highlight when auto customization is enabled |
| onWidgetTypeChange | `((widget: any, id: string, value: string) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level onChange handler for widget type changes (only called if widget doesn't have its own onChangeType) |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| data | `KpiBoxData[] \| ChartData \| Props` | ✅ | - |  |
| layout | `enum` | ❌ | - |  |
| groups | `undefined` | ❌ | - |  |
| className | `string` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| xAxis | `XAxisCustomProps` | ❌ | - |  |
| yAxis | `YAxisCustomProps` | ❌ | - |  |
| dataConfig | `ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[] \| ChartDataConfig&lt;Props&gt;[]` | ❌ | - |  |
| customCss | `any` | ❌ | - |  |
| formater | `((value: number) =&gt; string)` | ❌ | - |  |
| onClick | `((info: ChartBarClickInfo) =&gt; void)` | ❌ | - | Fired when a user clicks a bar/segment in bar charts |

---

## Tabs

**File:** `tabs/Tabs.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onChange | `((event: SyntheticEvent&lt;Element, Event&gt;, newValue: number) =&gt; void)` | ❌ | - | Callback fired when the value changes. |
| onClick | `((event: MouseEvent&lt;HTMLDivElement, MouseEvent&gt;, tab: TabProps) =&gt; boolean \| void)` | ❌ | - |  |
| tabsMainWrapperStyle | `CSSProperties` | ❌ | - |  |
| tabsPanelStyle | `CSSProperties` | ❌ | - |  |
| tabsStyle | `CSSProperties` | ❌ | - |  |
| offsetTop | `number` | ❌ | - |  |
| verticalTabsPanelWidth | `number` | ❌ | - |  |
| selectedTabIndex | `number \| null` | ❌ | - |  |
| preventTabSwitch | `boolean` | ❌ | - |  |
| tabsPanelHeader | `Element` | ❌ | - |  |
| tabsPanelFooter | `Element` | ❌ | - |  |
| mobileMode | `enum` | ❌ | - |  |
| showArrowsInMobileMode | `boolean` | ❌ | - |  |
| beforeAndAfterMobileSpace | `string` | ❌ | - |  |
| tabButtonDirection | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| tabsType | `enum` | ❌ | - |  |
| tabs | `TabGroup[] \| TabProps[]` | ✅ | - |  |

---

## Template

**File:** `dashboards/stories/Template.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| header | `HeaderProps` | ✅ | - |  |
| content | `Element` | ❌ | - |  |
| widgets | `Widget[]` | ❌ | - |  |
| widgetsOrder | `WidgetOrder[]` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| onWidgetTypeChange | `((widget: WidgetData, id: string, value: string) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Called when a widget type changes (via widget toggle). Parent should fetch new data and update widgets prop. Dashboard will automatically sync props to internal Redux store. Only triggered if widget doesn't have its own onChangeType handler. |
| onSaveWidgetsOrder | `((order: WidgetOrder[]) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Persist widgets order when in edit mode |
| onWidgetsOrderChange | `((order: WidgetOrder[]) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Fired on every widgets order change (drag end) |
| onHeaderFilterChange | `((filters: Map&lt;string, any&gt;, currentFilter: any) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Header filters change callback |
| onHeaderFilterApply | `((filters: Map&lt;string, any&gt;) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Header filters apply callback |
| onWidgetFilterChange | `((filters: Record&lt;string, any&gt;, current?: { name: string; value: any; }) =&gt; any)` | ❌ | - | Root-level: Widget-level filters change callback (used if widget doesn't provide its own) May return partial widget props to re-render; supports Promise. |
| onResetWidgetsOrder | `(() =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Reset widgets order to default |
| onDownloadPdf | `(() =&gt; void)` | ❌ | - | Root-level: Download PDF action |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |

---

## TemplateForProcurement

**File:** `dashboards/stories/TemplateForProcurement.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| header | `HeaderProps` | ✅ | - |  |
| content | `Element` | ❌ | - |  |
| widgets | `Widget[]` | ❌ | - |  |
| widgetsOrder | `WidgetOrder[]` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| onWidgetTypeChange | `((widget: WidgetData, id: string, value: string) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Called when a widget type changes (via widget toggle). Parent should fetch new data and update widgets prop. Dashboard will automatically sync props to internal Redux store. Only triggered if widget doesn't have its own onChangeType handler. |
| onSaveWidgetsOrder | `((order: WidgetOrder[]) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Persist widgets order when in edit mode |
| onWidgetsOrderChange | `((order: WidgetOrder[]) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Fired on every widgets order change (drag end) |
| onHeaderFilterChange | `((filters: Map&lt;string, any&gt;, currentFilter: any) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Header filters change callback |
| onHeaderFilterApply | `((filters: Map&lt;string, any&gt;) =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Header filters apply callback |
| onWidgetFilterChange | `((filters: Record&lt;string, any&gt;, current?: { name: string; value: any; }) =&gt; any)` | ❌ | - | Root-level: Widget-level filters change callback (used if widget doesn't provide its own) May return partial widget props to re-render; supports Promise. |
| onResetWidgetsOrder | `(() =&gt; void \| Promise&lt;void&gt;)` | ❌ | - | Root-level: Reset widgets order to default |
| onDownloadPdf | `(() =&gt; void)` | ❌ | - | Root-level: Download PDF action |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| className | `string` | ❌ | - |  |

---

## Testing

**File:** `testing/Testing.tsx`

*No props documented*

---

## Text

**File:** `text/Text.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| children | `ReactNode` | ❌ | - | The content of the component. |
| component | `ElementType&lt;any&gt;` | ❌ | - |  |
| textType | `enum` | ❌ | - |  |
| textColor | `enum` | ❌ | - |  |
| htmlFor | `string` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| underline | `boolean` | ❌ | - |  |
| textTransform | `enum` | ❌ | - |  |
| enableOverflowTooltip | `boolean` | ❌ | - |  |
| rowLines | `number` | ❌ | - |  |
| allowMultiTooltip | `boolean` | ❌ | - |  |
| isLineThrough | `boolean` | ❌ | - |  |
| selectable | `boolean` | ❌ | - |  |
| contentAlignment | `enum` | ❌ | - |  |
| onClickTooltip | `any` | ❌ | - |  |
| mask | `any[]` | ❌ | - |  |
| parseHtml | `boolean` | ❌ | - |  |
| bold | `boolean` | ❌ | - |  |
| color | `string` | ❌ | - |  |
| detectUrl | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| border | `ResponsiveStyleValue&lt;number \| (string & {}) \| "inset" \| "hidden" \| "inherit" \| "-moz-initial" \| "initial" \| "revert" \| "revert-layer" \| "unset" \| "medium" \| "thick" \| "thin" \| "dashed" \| "dotted" \| ... 184 more ...&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderTop | `ResponsiveStyleValue&lt;BorderTop&lt;string \| number&gt; \| readonly NonNullable&lt;BorderTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderRight | `ResponsiveStyleValue&lt;BorderRight&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderBottom | `ResponsiveStyleValue&lt;BorderBottom&lt;string \| number&gt; \| readonly NonNullable&lt;BorderBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderLeft | `ResponsiveStyleValue&lt;BorderLeft&lt;string \| number&gt; \| readonly NonNullable&lt;BorderLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| borderColor | `ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;BorderColor \| readonly string[]&gt;)` | ❌ | - |  |
| borderRadius | `ResponsiveStyleValue&lt;BorderRadius&lt;string \| number&gt; \| readonly NonNullable&lt;BorderRadius&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| display | `ResponsiveStyleValue&lt;readonly string[] \| Display&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Display&gt;)` | ❌ | - |  |
| displayPrint | `ResponsiveStyleValue&lt;readonly string[] \| Display&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Display&gt;)` | ❌ | - |  |
| overflow | `ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| Overflow&gt;)` | ❌ | - |  |
| textOverflow | `ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| TextOverflow&gt;)` | ❌ | - |  |
| visibility | `ResponsiveStyleValue&lt;Visibility \| readonly NonNullable&lt;Visibility&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| whiteSpace | `ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| WhiteSpace&gt;)` | ❌ | - |  |
| flexBasis | `ResponsiveStyleValue&lt;FlexBasis&lt;string \| number&gt; \| readonly NonNullable&lt;FlexBasis&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexDirection | `ResponsiveStyleValue&lt;FlexDirection \| readonly NonNullable&lt;FlexDirection&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexWrap | `ResponsiveStyleValue&lt;FlexWrap \| readonly NonNullable&lt;FlexWrap&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| justifyContent | `ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyContent&gt;)` | ❌ | - |  |
| alignItems | `ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignItems&gt;)` | ❌ | - |  |
| alignContent | `ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignContent&gt;)` | ❌ | - |  |
| order | `ResponsiveStyleValue&lt;Order \| readonly NonNullable&lt;Order&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;Order \| readonly NonNullable&lt;...&gt;[] \| undefined&gt;)` | ❌ | - |  |
| flex | `ResponsiveStyleValue&lt;Flex&lt;string \| number&gt; \| readonly NonNullable&lt;Flex&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexGrow | `ResponsiveStyleValue&lt;FlexGrow \| readonly NonNullable&lt;FlexGrow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| flexShrink | `ResponsiveStyleValue&lt;FlexShrink \| readonly NonNullable&lt;FlexShrink&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| alignSelf | `ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| AlignSelf&gt;)` | ❌ | - |  |
| justifyItems | `ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifyItems&gt;)` | ❌ | - |  |
| justifySelf | `ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| JustifySelf&gt;)` | ❌ | - |  |
| gap | `ResponsiveStyleValue&lt;Gap&lt;string \| number&gt; \| readonly NonNullable&lt;Gap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| columnGap | `ResponsiveStyleValue&lt;ColumnGap&lt;string \| number&gt; \| readonly NonNullable&lt;ColumnGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| rowGap | `ResponsiveStyleValue&lt;RowGap&lt;string \| number&gt; \| readonly NonNullable&lt;RowGap&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridColumn | `ResponsiveStyleValue&lt;GridColumn \| readonly NonNullable&lt;GridColumn&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridRow | `ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;GridRow&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;GridRow \| readonly NonNullable&lt;...&gt;[] \| undefined&gt;)` | ❌ | - |  |
| gridAutoFlow | `ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridAutoFlow&gt;)` | ❌ | - |  |
| gridAutoColumns | `ResponsiveStyleValue&lt;GridAutoColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridAutoRows | `ResponsiveStyleValue&lt;GridAutoRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridAutoRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateColumns | `ResponsiveStyleValue&lt;GridTemplateColumns&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateColumns&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateRows | `ResponsiveStyleValue&lt;GridTemplateRows&lt;string \| number&gt; \| readonly NonNullable&lt;GridTemplateRows&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| gridTemplateAreas | `ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| GridTemplateAreas&gt;)` | ❌ | - |  |
| gridArea | `ResponsiveStyleValue&lt;GridArea \| readonly NonNullable&lt;GridArea&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bgcolor | `ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| BackgroundColor&gt;)` | ❌ | - |  |
| zIndex | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| position | `ResponsiveStyleValue&lt;Position \| readonly NonNullable&lt;Position&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| top | `ResponsiveStyleValue&lt;Top&lt;string \| number&gt; \| readonly NonNullable&lt;Top&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| right | `ResponsiveStyleValue&lt;Right&lt;string \| number&gt; \| readonly NonNullable&lt;Right&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| bottom | `ResponsiveStyleValue&lt;Bottom&lt;string \| number&gt; \| readonly NonNullable&lt;Bottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| left | `ResponsiveStyleValue&lt;Left&lt;string \| number&gt; \| readonly NonNullable&lt;Left&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxShadow | `ResponsiveStyleValue&lt;number \| BoxShadow&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;number \| BoxShadow&gt;)` | ❌ | - |  |
| width | `ResponsiveStyleValue&lt;Width&lt;string \| number&gt; \| readonly NonNullable&lt;Width&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxWidth | `ResponsiveStyleValue&lt;MaxWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MaxWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minWidth | `ResponsiveStyleValue&lt;MinWidth&lt;string \| number&gt; \| readonly NonNullable&lt;MinWidth&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| height | `ResponsiveStyleValue&lt;Height&lt;string \| number&gt; \| readonly NonNullable&lt;Height&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| maxHeight | `ResponsiveStyleValue&lt;MaxHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MaxHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| minHeight | `ResponsiveStyleValue&lt;MinHeight&lt;string \| number&gt; \| readonly NonNullable&lt;MinHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| boxSizing | `ResponsiveStyleValue&lt;BoxSizing \| readonly NonNullable&lt;BoxSizing&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| m | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mt | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mr | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mb | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| ml | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| mx | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| my | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| p | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pt | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pr | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pb | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| pl | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| px | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| py | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| margin | `ResponsiveStyleValue&lt;Margin&lt;string \| number&gt; \| readonly NonNullable&lt;Margin&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginTop | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginRight | `ResponsiveStyleValue&lt;MarginRight&lt;string \| number&gt; \| readonly NonNullable&lt;MarginRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBottom | `ResponsiveStyleValue&lt;MarginBottom&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginLeft | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginX | `ResponsiveStyleValue&lt;MarginLeft&lt;string \| number&gt; \| readonly NonNullable&lt;MarginLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginY | `ResponsiveStyleValue&lt;MarginTop&lt;string \| number&gt; \| readonly NonNullable&lt;MarginTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInline | `ResponsiveStyleValue&lt;MarginInline&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineStart | `ResponsiveStyleValue&lt;MarginInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginInlineEnd | `ResponsiveStyleValue&lt;MarginInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlock | `ResponsiveStyleValue&lt;MarginBlock&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockStart | `ResponsiveStyleValue&lt;MarginBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| marginBlockEnd | `ResponsiveStyleValue&lt;MarginBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;MarginBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| padding | `ResponsiveStyleValue&lt;Padding&lt;string \| number&gt; \| readonly NonNullable&lt;Padding&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingTop | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingRight | `ResponsiveStyleValue&lt;PaddingRight&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingRight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBottom | `ResponsiveStyleValue&lt;PaddingBottom&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBottom&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingLeft | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingX | `ResponsiveStyleValue&lt;PaddingLeft&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingLeft&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingY | `ResponsiveStyleValue&lt;PaddingTop&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingTop&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInline | `ResponsiveStyleValue&lt;PaddingInline&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInline&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineStart | `ResponsiveStyleValue&lt;PaddingInlineStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingInlineEnd | `ResponsiveStyleValue&lt;PaddingInlineEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingInlineEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlock | `ResponsiveStyleValue&lt;PaddingBlock&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlock&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockStart | `ResponsiveStyleValue&lt;PaddingBlockStart&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockStart&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| paddingBlockEnd | `ResponsiveStyleValue&lt;PaddingBlockEnd&lt;string \| number&gt; \| readonly NonNullable&lt;PaddingBlockEnd&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| typography | `ResponsiveStyleValue&lt;string&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string&gt;)` | ❌ | - |  |
| fontFamily | `ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontFamily&gt;)` | ❌ | - |  |
| fontSize | `ResponsiveStyleValue&lt;FontSize&lt;string \| number&gt; \| readonly NonNullable&lt;FontSize&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| fontStyle | `ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;readonly string[] \| FontStyle&gt;)` | ❌ | - |  |
| fontWeight | `ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;string \| (string & {}) \| (number & {})&gt;)` | ❌ | - |  |
| letterSpacing | `ResponsiveStyleValue&lt;LetterSpacing&lt;string \| number&gt; \| readonly NonNullable&lt;LetterSpacing&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| lineHeight | `ResponsiveStyleValue&lt;LineHeight&lt;string \| number&gt; \| readonly NonNullable&lt;LineHeight&lt;string \| number&gt;&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |
| textAlign | `ResponsiveStyleValue&lt;TextAlign \| readonly NonNullable&lt;TextAlign&gt;[]&gt; \| ((theme: Theme) =&gt; ResponsiveStyleValue&lt;...&gt;)` | ❌ | - |  |

---

## TextArea

**File:** `inputs/textArea/TextArea.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - |  |
| maxRows | `number` | ❌ | - | Maximum number of rows to display. |
| minRows | `number` | ❌ | - | Minimum number of rows to display. |
| disabled | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| resizeable | `boolean` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| label | `string` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| withUndoButton | `boolean` | ❌ | - |  |
| ref | `any` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLTextAreaElement&gt;) =&gt; void)` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TextBasicEditRenderer

**File:** `dataGrid/renderers/text/text_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TextEditRenderer

**File:** `dataGrid/renderers/text/text_edit.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TextField

**File:** `form/components/FieldItem/fields/TextField.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| currencyProps | `SelectProps` | ❌ | - |  |
| onChangeCurrency | `((e: ChangeEvent&lt;HTMLInputElement&gt;, value: any) =&gt; void)` | ❌ | - |  |
| errors | `string[]` | ❌ | - |  |
| setErrors | `((errors: string[]) =&gt; void)` | ❌ | - |  |
| testProps | `any` | ❌ | - |  |
| displayFieldAsError | `boolean` | ❌ | - |  |
| showUpdateFlag | `boolean` | ❌ | - |  |
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| inputType | `enum` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| inputSize | `enum` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| withForm | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| ref | `any` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| mask | `any` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onFocus" \| "onBlur" \| "onChange"; }` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TextFilter

**File:** `textFilter/TextFilter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onChange | `(value: string) =&gt; void` | ✅ | - |  |
| onKeyPress | `((event: any) =&gt; void)` | ❌ | - |  |
| onClear | `((text: string) =&gt; void)` | ❌ | - |  |
| title | `string` | ❌ | `null` |  |
| value | `string` | ❌ | - |  |
| placeholder | `string` | ❌ | `Search...` |  |
| delayInMs | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TextInput

**File:** `inputs/textInput/TextInput.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - | Name attribute of the `input` element. |
| inputType | `enum` | ❌ | - |  |
| id | `string` | ❌ | - | The id of the `input` element. Use this prop to make `label` and `helperText` accessible for screen readers. |
| type | `enum` | ❌ | - | Type of the `input` element. It should be [a valid HTML5 input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types). |
| fullWidth | `boolean` | ❌ | - | If `true`, the input will take up the full width of its container. |
| inputSize | `enum` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| placeholder | `string` | ❌ | - | The short hint displayed in the `input` before the user enters a value. |
| disabled | `boolean` | ❌ | - | If `true`, the component is disabled. |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - | If `true`, the label is displayed in an error state. |
| InputProps | `object` | ❌ | - |  |
| withIcon | `boolean` | ❌ | - |  |
| withActionButton | `boolean` | ❌ | - |  |
| iconPosition | `enum` | ❌ | - |  |
| iconName | `string` | ❌ | - |  |
| iconType | `enum` | ❌ | - |  |
| checkedIconName | `string` | ❌ | - |  |
| checkedIconType | `enum` | ❌ | - |  |
| value | `TextInputValueTypes` | ❌ | - | The value of the `input` element, required for a controlled component. |
| withForm | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - | If `true`, the label is displayed as required and the `input` element is required. |
| ref | `any` | ❌ | - |  |
| togglePassword | `boolean` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| multiLineError | `boolean` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| search | `boolean` | ❌ | - |  |
| withRef | `InputAutoEvents` | ❌ | - |  |
| hasFocus | `boolean` | ❌ | - |  |
| fillColor | `boolean` | ❌ | - |  |
| fillBorder | `boolean` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isSensitiveField | `boolean` | ❌ | - |  |
| formWrapperStyles | `CSSProperties` | ❌ | - |  |
| mask | `any` | ❌ | - |  |
| removeMaskOnTyping | `boolean` | ❌ | - |  |
| formatNumber | `boolean` | ❌ | - |  |
| stringAsNumberWithCalculation | `{ formatNumber?: boolean; maxDigitsAfterDecimalPointIfRequire?: number; formatNumberProps?: NumberFormatProps&lt;InputAttributes&gt; \| undefined; numberAreaFormat: NumberAreaFormat; } \| undefined` | ❌ | - |  |
| suffix | `string` | ❌ | - |  |
| formatNumberProps | `NumberFormatProps&lt;InputAttributes&gt;` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| minValue | `number` | ❌ | - |  |
| maxValue | `number` | ❌ | - |  |
| limitChars | `number` | ❌ | - |  |
| onChange | `((event: ChangeEvent&lt;HTMLInputElement&gt;, params?: any) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyPress | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| iconButtonClick | `((event: MouseEvent&lt;HTMLElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| validator | `((value: TextInputValueTypes) =&gt; boolean)` | ❌ | - |  |
| formatter | `{ func: (value: TextInputValueTypes) =&gt; TextInputValueTypes; eventType: "onFocus" \| "onBlur" \| "onChange"; }` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TextLineRenderer

**File:** `dataList/renderers/text/text_line_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| columnDef | `ColumnDef` | ✅ | - |  |
| row | `any` | ✅ | - |  |
| field | `string` | ✅ | - |  |

---

## TextRenderer

**File:** `dataGrid/renderers/text/text_view.tsx`

*No props documented*

---

## Texts

**File:** `designSystem/text/Texts.tsx`

*No props documented*

---

## Tile

**File:** `tiles/tile/Tile.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| titleLine1 | `ReactNode` | ✅ | - |  |
| titleLine2 | `ReactNode` | ❌ | - |  |
| titleTooltip | `TooltipProps` | ❌ | - |  |
| text | `ReactNode` | ❌ | - |  |
| onClick | `() =&gt; void` | ✅ | - |  |
| img | `string` | ✅ | - |  |
| disabled | `boolean` | ❌ | - |  |
| icon | `IconProps` | ❌ | - |  |
| years | `string[]` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Tiles

**File:** `tiles/Tiles.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| tiles | `TileProps[]` | ✅ | - |  |
| tileInRow | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## TimePicker

**File:** `pickers/timePicker/TimePicker.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | `string` | ❌ | - | Name attribute used by the `input` element in the Field. |
| inputRef | `any` | ❌ | - | Pass a ref to the `input` element. |
| className | `string` | ❌ | - | Class name applied to the root element. |
| placeholder | `string` | ❌ | - |  |
| label | `string` | ❌ | - | The label content. |
| multiLineLabel | `boolean` | ❌ | - |  |
| title | `string` | ❌ | - |  |
| startRange | `TDate` | ❌ | - |  |
| endRange | `TDate` | ❌ | - |  |
| inputFormat | `enum` | ❌ | - |  |
| displayFormat | `enum` | ❌ | - |  |
| monthAndYearView | `DatePickerView[]` | ❌ | - |  |
| dateFormat | `string` | ❌ | - | Props applied to previous dateFormat is no longer needed. @deprecated Use inputFormat instead. |
| timeSpecific | `string` | ❌ | - |  |
| initialValue | `TDate` | ❌ | - |  |
| monthYearView | `boolean` | ❌ | - |  |
| disableWeekends | `boolean` | ❌ | - |  |
| holidays | `TDate[]` | ❌ | - |  |
| enablePast | `boolean` | ❌ | - |  |
| disableFuture | `boolean` | ❌ | - | If `true`, disable values after the current date for date components, time for time components and both for date time components. |
| disableCloseOnSelect | `boolean` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| required | `boolean` | ❌ | - |  |
| errorText | `string` | ❌ | - |  |
| error | `boolean` | ❌ | - |  |
| startOrEndOfTheMonth | `enum` | ❌ | - |  |
| withLabelTooltip | `WithLabelTooltip` | ❌ | - |  |
| mask | `string` | ❌ | - | Props applied to input text element. @deprecated sending mask is no longer needed. |
| shortYear | `boolean` | ❌ | - |  |
| clearable | `boolean` | ❌ | - |  |
| popperRef | `any` | ❌ | - |  |
| inputProps | `any` | ❌ | - |  |
| readOnly | `boolean` | ❌ | - |  |
| isFilter | `boolean` | ❌ | - |  |
| skipPickerButtonOnFocus | `boolean` | ❌ | - |  |
| hidePickerIcon | `boolean` | ❌ | - |  |
| shouldDisableDate | `((date: Date \| null) =&gt; boolean)` | ❌ | - |  |
| onChange | `(date: Date, keyboardInputValue?: string \| undefined) =&gt; void` | ✅ | - |  |
| onError | `((reason: string, value: string) =&gt; void)` | ❌ | - |  |
| onApply | `((value: Date) =&gt; void)` | ❌ | - |  |
| onBlur | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onOpen | `(() =&gt; void)` | ❌ | - | Callback fired when the popup requests to be opened. Use in controlled mode (see `open`). |
| onClose | `((value?: TDate) =&gt; void)` | ❌ | - |  |
| onAccept | `((value: TDate) =&gt; void)` | ❌ | - |  |
| onClear | `(() =&gt; void)` | ❌ | - |  |
| onFocus | `((event: FocusEvent&lt;HTMLInputElement, Element&gt;) =&gt; void)` | ❌ | - |  |
| onKeyDown | `((event: KeyboardEvent&lt;HTMLInputElement&gt;) =&gt; void)` | ❌ | - |  |
| onEnter | `((value: TDate) =&gt; void)` | ❌ | - |  |
| footer | `any` | ❌ | - |  |
| isInsideTable | `boolean` | ❌ | - |  |
| pickerType | `enum` | ❌ | - |  |
| pickerSize | `enum` | ❌ | - |  |
| debounce | `number` | ❌ | - |  |
| tabIndex | `number` | ❌ | - |  |
| descriptionText | `string` | ❌ | - |  |
| inputType | `enum` | ❌ | - |  |
| customWidth | `string` | ❌ | - |  |
| hideValue | `boolean` | ❌ | - |  |
| inlineLabel | `Element` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Toggle

**File:** `Toggle/Toggle.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| className | `string` | ❌ | - |  |
| options | `ToggleOption[]` | ✅ | - |  |
| value | `string` | ❌ | - |  |
| onChange | `((index: number, value: string) =&gt; void)` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| size | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| name | `string` | ❌ | - | Optional radio group name; defaults to a unique per-instance name |
| style | `CSSProperties` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## Toolbar

**File:** `pickers/components/Toolbar.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| date | `Date \| null` | ❌ | - |  |
| minDate | `Date` | ❌ | - |  |
| maxDate | `Date` | ❌ | - |  |
| setDate | `(date: Date \| null \| undefined) =&gt; object` | ✅ | - |  |
| setView | `(view: DatePickerView) =&gt; object` | ✅ | - |  |

---

## Tooltip

**File:** `tooltip/Tooltip.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| title | `string \| Element` | ✅ | - | Tooltip title. Zero-length titles string, undefined, null and false are never displayed. |
| className | `string` | ❌ | - |  |
| placement | `enum` | ❌ | - | Tooltip placement. |
| tooltipType | `enum` | ❌ | - |  |
| tooltipAnimation | `enum` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| displayOnOpen | `boolean` | ❌ | - |  |
| onOpenContent | `(() =&gt; string \| Element)` | ❌ | - |  |
| linkData | `LinkData` | ❌ | - |  |
| maxContent | `boolean` | ❌ | - |  |
| dynamicWidth | `boolean` | ❌ | - |  |
| copyClipboard | `CopyToClipboardProps` | ❌ | - |  |
| showCopyToClipboard | `boolean` | ❌ | - |  |
| openOnClick | `boolean` | ❌ | - |  |
| tooltipClickable | `boolean` | ❌ | - |  |
| onTooltipClick | `((event: MouseEvent&lt;HTMLDivElement, MouseEvent&gt;) =&gt; void)` | ❌ | - |  |
| value | `any` | ❌ | - |  |
| clipboardClassName | `string` | ❌ | - |  |
| display | `enum` | ❌ | - |  |
| keepOpen | `boolean` | ❌ | - |  |

---

## TopBarFilters

**File:** `dataGrid/components/filters/TopBarFilters.tsx`

*No props documented*

---

## TypeRenderer

**File:** `dataGrid/renderers/type/type_view.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |

---

## VendorField

**File:** `form/components/FieldItem/fields/VendorField.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onChange | `(value: any) =&gt; void` | ✅ | - |  |
| vendorFields | `FieldItemProps&lt;FieldType&gt;[]` | ✅ | - |  |
| required | `boolean` | ❌ | - |  |
| expanded | `boolean` | ❌ | - |  |
| placeholder | `string` | ❌ | - |  |
| statusIcon | `Element` | ❌ | - |  |
| tooltipInfo | `string \| Element` | ❌ | - |  |
| tooltipInfoDisabled | `boolean` | ❌ | - |  |
| labelTooltipText | `string` | ❌ | - |  |
| selectProps | `SelectProps` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| errorFields | `ErrorField` | ❌ | - |  |
| warningFields | `WarningField` | ❌ | - |  |
| updatedFields | `UpdatedField` | ❌ | - |  |
| labelMaxWidth | `number` | ❌ | - |  |
| onClick | `(value: SelectOption) =&gt; void` | ✅ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| onUpdateList | `(event?: MouseEvent&lt;HTMLButtonElement, MouseEvent&gt; \| undefined) =&gt; any` | ✅ | - |  |
| vendorProps | `{ disableFields: VendorFields; requiredFields: VendorFields; }` | ✅ | - |  |
| showUpdateFlag | `boolean` | ❌ | - |  |

---

## ViewByFilter

**File:** `dashboards/components/filters/ViewByFilter.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| onFilterChange | `((params: any) =&gt; void)` | ❌ | - |  |
| order | `number` | ❌ | - |  |
| cb | `((value: any, name: string) =&gt; void)` | ❌ | - |  |
| index | `number` | ❌ | - |  |
| position | `enum` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |
| filterType | `WidgetFilterTypes.VIEW_BY` | ✅ | - |  |
| filterProps | `Omit&lt;SelectProps, "onChange"&gt; & { name?: string \| undefined; label?: string \| undefined; }` | ✅ | - | Uses Select under the hood. Options default to Days/Weeks/Months/Quarters but can be overridden. |

---

## WidgetTypeToggle

**File:** `dashboards/components/WidgetTypeToggle.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| options | `ToggleOption[]` | ✅ | - |  |
| value | `string` | ❌ | - |  |
| onChangeType | `((index: number, value: string) =&gt; void)` | ❌ | - |  |
| disabled | `boolean` | ❌ | - |  |
| size | `enum` | ❌ | - |  |
| fullWidth | `boolean` | ❌ | - |  |
| name | `string` | ❌ | - |  |

---

## WizardFormDemoPage

**File:** `form/demos/WizardFormDemoPage.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| formStyle | `CSSProperties` | ❌ | - |  |
| getInputsRefs | `((inputsRefs: any) =&gt; void)` | ❌ | - |  |
| onChange | `((element: any, inputsRefs?: any, formikForm?: any) =&gt; void)` | ❌ | - |  |
| formSchemaSections | `FormSchemaSection[]` | ✅ | - |  |
| onSubmit | `(values: FormikValues, formikHelpers?: FormikHelpers&lt;FormikValues&gt; \| undefined) =&gt; void \| Promise&lt;any&gt;` | ✅ | - | Submission handler |
| footer | `FormFooterProps` | ❌ | - |  |
| customSchema | `any` | ❌ | - |  |
| loading | `boolean` | ❌ | - |  |
| validate | `((values: FormikValues, refs?: any) =&gt; void \| object \| Promise&lt;FormikErrors&lt;FormikValues&gt;&gt;)` | ❌ | - | Validation function. Must return an error object or promise that throws an error object where that object keys map to corresponding value. |
| gridDirection | `enum` | ❌ | - |  |
| numberOfSkeletonFields | `number` | ❌ | - |  |
| formError | `boolean` | ❌ | - |  |
| fieldsWrapperStyle | `CSSProperties` | ❌ | - |  |
| variation | `enum` | ❌ | - |  |
| boxProps | `BoxProps` | ❌ | - |  |
| asWizard | `boolean` | ❌ | - |  |
| wizardProps | `{ asTabs?: boolean; tabsProps?: Partial&lt;TabsProps&gt;; currentStep?: number \| undefined; onStepChange?: ((step: number) =&gt; void) \| undefined; withStepper?: boolean \| undefined; } \| undefined` | ❌ | - |  |

---

## ZeroState

**File:** `ZeroState/ZeroState.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| message | `string \| null` | ❌ | - |  |
| subMessage | `string \| null` | ❌ | - |  |
| customContent | `Element` | ❌ | - |  |
| textType | `enum` | ❌ | - |  |
| isLoading | `boolean` | ❌ | - |  |
| showWithDelay | `boolean` | ❌ | - |  |
| bottomCustomJsx | `Element` | ❌ | - |  |
| width | `number` | ❌ | - |  |
| height | `number` | ❌ | - |  |
| multiLineLabel | `boolean` | ❌ | - |  |
| textAlign | `any` | ❌ | - |  |
| zeroStateType | `enum` | ❌ | - |  |
| inline | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## buildText

**File:** `dataGrid/helpers/storyHelper.tsx`

*No props documented*

---

## calculateRowHeight

Calculates the row height based on subContent items
Only applies dynamic height when rowLines > 1 (multi-line rows)

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## clearEditFieldFromSort

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## createSortComperator

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## currencybasic

**File:** `dataGrid/renderers/currency/currency_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## datebasic

**File:** `dataGrid/renderers/date/date_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| showFromNow | `boolean` | ❌ | - |  |
| showLabel | `boolean` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## enforceMaxVisibleColumns

Enforces maxVisibleColumns limit by hiding extra visible columns

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## footerLabels

Footer labels helper

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

*No props documented*

---

## getBulkEditErrorMessage

Helper function to map technical reasons to user-friendly error messages

**File:** `dataGrid/helpers/bulkEdit.helper.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowId | `string \| number` | ✅ | - |  |
| field | `string` | ✅ | - |  |
| fieldName | `string` | ✅ | - |  |
| selectedValue | `any` | ✅ | - |  |
| selectedValueLabel | `string` | ❌ | - |  |
| reason | `string` | ✅ | - |  |
| columnType | `string` | ❌ | - |  |

---

## getColor

**File:** `dataGrid/helpers/custom_filters.tsx`

*No props documented*

---

## getColumnOrder

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## getColumnResize

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## getDataGridRows

**File:** `dataGrid/helpers/storyHelper.tsx`

*No props documented*

---

## getFilterOperators

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## getFooter

Get footer helper function

**File:** `dataGrid/mocks/StampliTableTemplates.tsx`

*No props documented*

---

## getGridRowSelectors

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## getGridVisibleRows

**File:** `dataGrid/helpers/grid.helper.tsx`

*No props documented*

---

## getOptionsPO

**File:** `dataGrid/helpers/storyData.tsx`

*No props documented*

---

## getPaymentMethodSubContent

**File:** `dataGrid/helpers/storyHelper.tsx`

*No props documented*

---

## getServerOptionsForPO

**File:** `dataGrid/helpers/storyData.tsx`

*No props documented*

---

## getSortComparatorByType

**File:** `dataList/helpers/list.helper.tsx`

*No props documented*

---

## getVendorOptions

**File:** `dataGrid/helpers/storyData.tsx`

*No props documented*

---

## inxpoc

**File:** `accordion/poc/inx_poc.tsx`

*No props documented*

---

## markRowConflicts

Marks conflicts on rows by adding _bulkEditConflictFields and error props
IMPORTANT: Merges with existing conflict fields instead of replacing them

**File:** `dataGrid/helpers/bulkEdit.helper.tsx`

*No props documented*

---

## numberbasic

**File:** `dataGrid/renderers/number/number_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| showLabel | `boolean` | ❌ | - |  |

---

## processBulkEditRows

Processes rows by applying form values and calling onChange handlers

**File:** `dataGrid/helpers/bulkEdit.helper.tsx`

*No props documented*

---

## processFieldChange

**File:** `dataGrid/helpers/custom_renderers.tsx`

*No props documented*

---

## renderFilters

**File:** `dataGrid/components/filters/filters.tsx`

*No props documented*

---

## searchbox

**File:** `dataGrid/renderers/search/search_box.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| id | `string` | ❌ | - |  |
| role | `string \| (string & {})` | ❌ | - |  |
| selectSize | `enum` | ✅ | - |  |
| width | `number` | ✅ | - |  |

---

## searchinput

**File:** `dataGrid/renderers/search/search_input.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| api | `any` | ✅ | - | GridApi that let you manipulate the grid. |
| colDef | `ColumnDef` | ✅ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |

---

## searchtabsinput

**File:** `dataGrid/renderers/search/search_tabs_input.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| api | `any` | ✅ | - | GridApi that let you manipulate the grid. |
| colDef | `ColumnDef` | ✅ | - |  |
| inputType | `enum` | ❌ | - |  |
| tabs | `Record&lt;string, string&gt;` | ❌ | - |  |
| defaultTab | `number` | ❌ | - |  |
| defaultSelectedTab | `number` | ❌ | - |  |
| itemKeyPath | `string` | ❌ | - |  |
| fetchPerTab | `boolean` | ❌ | - |  |

---

## simulateArrowDown

**File:** `dataGrid/helpers/custom_renderers.tsx`

*No props documented*

---

## textbasic

**File:** `dataGrid/renderers/text/text_basic.tsx`

### Props

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| rowLines | `number` | ❌ | - |  |
| dir | `enum` | ❌ | - |  |
| intro | `IntroProps` | ❌ | - |  |
| dataTestId | `string` | ❌ | - |  |
| testIdPrefix | `string` | ❌ | - |  |
| hideOnFS | `boolean` | ❌ | - |  |
| isFiltered | `boolean` | ❌ | - |  |

---

## triggerEditCell

**File:** `dataGrid/helpers/custom_renderers.tsx`

*No props documented*

---

## withEditRenderer

**File:** `dataGrid/renderers/withEditRenderer.tsx`

*No props documented*

---

## withFilterRenderer

**File:** `dataGrid/filters/withFilterRenderer.tsx`

*No props documented*

---

## withProps

**File:** `withProps.tsx`

*No props documented*

---

## withRenderer

**File:** `dataGrid/renderers/withRenderer.tsx`

*No props documented*

---


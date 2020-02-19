This is a collection of snippets for development of prequalifiction logic in Sublime 3

## Installation
```cd "C:\Users\YOUR_USERNAME\AppData\Roaming\Sublime Text 3\Packages\User"```

```git clone https://github.com/AlexandraKim/PrequalificationSnippets.git```

## Snippet Listing
### [all] AllAreTrueRule
```xml
<AllAreTrueRule>
	$0
</AllAreTrueRule>
```

### [any] AnyoneIsTrueRule
```xml
<AnyoneIsTrueRule>
	$0
</AnyoneIsTrueRule>
```

### [ansr] Policy:AnswerChangeRule
```xml
<Policy:AnswerChangeRule AnswerMap="$1" Value="$2" />$0
```

### [ansre] Policy:AnswerChangeRule _expanded
```xml
<Policy:AnswerChangeRule AnswerMap="$1">
	<Policy:AnswerChangeRule.SetValue>
		$0
	</Policy:AnswerChangeRule.SetValue>
</Policy:AnswerChangeRule>
```

### [cnd] ConditionedAnalysisChain
```xml
<ConditionedAnalysisChain>
	$0
</ConditionedAnalysisChain>
```

### [cndc] ConditionedAnalysisChain.Condition
```xml
<ConditionedAnalysisChain Condition="$1">
	$0
</ConditionedAnalysisChain>
```

### [cnde] ConditionedAnalysisChain _expanded
```xml
<ConditionedAnalysisChain>
	<ConditionedAnalysisChain.Condition>
		$0
	</ConditionedAnalysisChain.Condition>
	
</ConditionedAnalysisChain>
```

### [countdtm] CountDatumKey
```xml
<CountDatumKey ComplexMap="$0" />
```

### [count] CountRule
```xml
<CountRule>
	<CountRule.Expression>
		$0
	</CountRule.Expression>
	<ArrayDatumKey AnswerMap="$1" Collection="$2" />
</CountRule>
```

### [custom] CustomQuestionBindingRule
```xml
<Policy:CustomQuestionBindingRule AnswerMap="$1" CustomDropdown="True">
	<Policy:CustomQuestionBindingRule.Options>
		<System:String>$2</System:String>
	</Policy:CustomQuestionBindingRule.Options>${0:
	<Policy:CustomQuestionBindingRule.DatumKeyOptions>
		<DatumKey Map="" />
	</Policy:CustomQuestionBindingRule.DatumKeyOptions>}
</Policy:CustomQuestionBindingRule>
```

### [dtm] DatumKey
```xml
<DatumKey Map="$1" />$0
```

### [dtmc] DatumKey.ComplexMap
```xml
<DatumKey ComplexMap="$1" />$0
```

### [equalbool] EqualityRule > BooleanConstDatumKey
```xml
<EqualityRule>
	<DatumKey Map="$1" />
	<BooleanConstDatumKey Value="${2:True}" />
</EqualityRule>$0
```

### [equalconst] EqualityRule > ConstDatumKey
```xml
<EqualityRule>
	<DatumKey Map="$1" />
	<ConstDatumKey Value="$2" />
</EqualityRule>$0
```

### [inset] IsValueInSetRule
```xml
<IsValueInSetRule AnswerMap="$1">
	<IsValueInSetRule.Values>
		<System:String>$2</System:String>
	</IsValueInSetRule.Values>
</IsValueInSetRule>
$0
```

### [numc] NumericalComparison
```xml
<NumericalComparison AnswerMap="$1" ${2:Min="$3"} ${4:Max="$0"} CanBeEqualToMinimum="${5:True}" CanBeEqualToMaximum="${6:True}"/>
```

### [numce] NumericalComparison _expanded
```xml
<NumericalComparison ${1:Min="$2"} ${3:Max="$4"} CanBeEqualToMinimum="${5:True}" CanBeEqualToMaximum="${6:True}" >
	<NumericalComparison.AnswerMap>
		$0
	</NumericalComparison.AnswerMap>
</NumericalComparison>
```

### [numr] NumericalRule
```xml
<NumericalRule>	
	<NumericalRule.AnswerMap>
		<CountDatumKey ComplexMap="$1" />
	</NumericalRule.AnswerMap>
	<Range Max="$2" Result="${3:N}" />
	<NumericalRule.Signals>
		<SignalCase Condition="${3:N}">
			<ResultExplanation>$0</ResultExplanation>
		</SignalCase>
	</NumericalRule.Signals>
</NumericalRule>
```

### [ref] Reference
```xml
<x:Reference Name="$0" />
```

### [rqr] RequiredAnswerRule
```xml
<RequiredAnswerRule AnswerMap="$1" Absent="${2:N}" />
$0
```

### [rqre] RequiredAnswerRule _expanded
```xml
<RequiredAnswerRule AnswerMap="$1" ${2:Absent="${3:N}"} Present="$4">
	<SignalCase Condition="$4">
		<ResultExplanation>$5</ResultExplanation>
	</SignalCase>
</RequiredAnswerRule>
$0
```

### [subtr] SubtractionDatumKey
```xml
<SubtractionDatumKey UseZeroForNulls="True" Left="$1" Right="$0" />
```

### [subtre] SubtractionDatumKey _expanded
```xml
<SubtractionDatumKey UseZeroForNulls="True">
	<SubtractionDatumKey.Left>
		$0
	</SubtractionDatumKey.Left>
	<SubtractionDatumKey.Right>
		
	</SubtractionDatumKey.Right>
</SubtractionDatumKey>
```

### [sum] SumDatumKey
```xml
<SumDatumKey UseZeroForNulls="True" Left="$1" Right="$0" />
```

### [sume] SumDatumKey _expanded
```xml
<SumDatumKey UseZeroForNulls="True">
	<SumDatumKey.Left>
		$0
	</SumDatumKey.Left>
	<SumDatumKey.Right>
		
	</SumDatumKey.Right>
</SumDatumKey>
```

### [vsb] VisibilityRulesGroup
```xml
<Forms:VisibilityRulesGroup IsVisible="$1">
	<Forms:VisibilityRule Question="$2" />
</Forms:VisibilityRulesGroup>
$0
```

### [vsbe] VisibilityRulesGroup _expanded
```xml
<Forms:VisibilityRulesGroup>
	<Forms:VisibilityRulesGroup.IsVisible>
		$1
	</Forms:VisibilityRulesGroup.IsVisible>
	<Forms:VisibilityRule Question="$0" />
</Forms:VisibilityRulesGroup>
```

### [yn] YesNoRule
```xml
<YesNoRule AnswerMap="$1" LeaveBlankVariant="${2:N}" />$0
```

### [ynn] YesNoRule.NoVariant
```xml
<YesNoRule AnswerMap="$1" NoVariant="$2" LeaveBlankVariant="${3:N}"> 
	<SignalCase Condition="$2">
		<ResultExplanation>$4</ResultExplanation>
	</SignalCase>
</YesNoRule>
$0
```

### [ynne] YesNoRule.NoVariant _expanded
```xml
<YesNoRule NoVariant="$1"> 
	<YesNoRule.AnswerMap>
		$0
	</YesNoRule.AnswerMap>
	<SignalCase Condition="$1">
		<ResultExplanation>$2</ResultExplanation>
	</SignalCase>
</YesNoRule>
```

### [yny] YesNoRule.YesVariant
```xml
<YesNoRule AnswerMap="$1" YesVariant="$2" LeaveBlankVariant="${3:N}"> 
	<SignalCase Condition="$2">
		<ResultExplanation>$4</ResultExplanation>
	</SignalCase>
</YesNoRule>
$0
```

### [ynye] YesNoRule.YesVariant _expanded
```xml
<YesNoRule YesVariant="$1"> 
	<YesNoRule.AnswerMap>
		$0
	</YesNoRule.AnswerMap>
	<SignalCase Condition="$1">
		<ResultExplanation>$2</ResultExplanation>
	</SignalCase>
</YesNoRule>
```

### [ynyn] YesNoRule.YesVariant U YesNoRule.NoVariant
```xml
<YesNoRule AnswerMap="$1" YesVariant="$2" NoVariant="$3" LeaveBlankVariant="${4:N}"> 
	<SignalCase Condition="$2">
		<ResultExplanation>$5</ResultExplanation>
	</SignalCase>
	<SignalCase Condition="$3">
		<ResultExplanation>$6</ResultExplanation>
	</SignalCase>
</YesNoRule>
$0
```

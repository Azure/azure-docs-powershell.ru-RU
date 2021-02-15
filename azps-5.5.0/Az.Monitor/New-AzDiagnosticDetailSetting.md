---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237265"
---
# <span data-ttu-id="f7984-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="f7984-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="f7984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7984-102">SYNOPSIS</span></span>
<span data-ttu-id="f7984-103">Создание объекта PSDiagnosticDetailSetting, тип может быть метрическим или журналом</span><span class="sxs-lookup"><span data-stu-id="f7984-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="f7984-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7984-104">SYNTAX</span></span>

### <span data-ttu-id="f7984-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7984-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7984-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7984-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7984-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7984-107">DESCRIPTION</span></span>
<span data-ttu-id="f7984-108">Создание объекта PSMetricSettings или PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="f7984-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="f7984-109">Категории можно получить с помощью `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="f7984-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="f7984-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7984-110">EXAMPLES</span></span>

### <span data-ttu-id="f7984-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7984-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="f7984-112">Создание объекта PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="f7984-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="f7984-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f7984-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="f7984-114">Создание объекта PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="f7984-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="f7984-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7984-115">PARAMETERS</span></span>

### <span data-ttu-id="f7984-116">-Category</span><span class="sxs-lookup"><span data-stu-id="f7984-116">-Category</span></span>
<span data-ttu-id="f7984-117">Категория параметра</span><span class="sxs-lookup"><span data-stu-id="f7984-117">Category of setting</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7984-118">-DefaultProfile</span></span>
<span data-ttu-id="f7984-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7984-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="f7984-120">-Enabled</span></span>
<span data-ttu-id="f7984-121">Включить параметр</span><span class="sxs-lookup"><span data-stu-id="f7984-121">Enable the setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-122">-Log</span><span class="sxs-lookup"><span data-stu-id="f7984-122">-Log</span></span>
<span data-ttu-id="f7984-123">Создание параметра журнала</span><span class="sxs-lookup"><span data-stu-id="f7984-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-124">-Метрическая</span><span class="sxs-lookup"><span data-stu-id="f7984-124">-Metric</span></span>
<span data-ttu-id="f7984-125">Создание параметра метрики</span><span class="sxs-lookup"><span data-stu-id="f7984-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="f7984-126">-RetentionEnabled</span></span>
<span data-ttu-id="f7984-127">Включить политику хранения</span><span class="sxs-lookup"><span data-stu-id="f7984-127">Enable Retention policy</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f7984-128">-RetentionInDays</span></span>
<span data-ttu-id="f7984-129">Дни хранения для политики хранения</span><span class="sxs-lookup"><span data-stu-id="f7984-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="f7984-130">-TimeGrain</span></span>
<span data-ttu-id="f7984-131">TimeGrain for metric setting</span><span class="sxs-lookup"><span data-stu-id="f7984-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7984-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7984-132">CommonParameters</span></span>
<span data-ttu-id="f7984-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7984-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7984-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7984-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7984-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7984-135">INPUTS</span></span>

### <span data-ttu-id="f7984-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f7984-136">System.String</span></span>

## <span data-ttu-id="f7984-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7984-137">OUTPUTS</span></span>

### <span data-ttu-id="f7984-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="f7984-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="f7984-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7984-139">NOTES</span></span>

## <span data-ttu-id="f7984-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7984-140">RELATED LINKS</span></span>

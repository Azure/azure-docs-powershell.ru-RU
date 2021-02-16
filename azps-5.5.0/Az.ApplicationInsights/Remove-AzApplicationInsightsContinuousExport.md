---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244304"
---
# <span data-ttu-id="6d41e-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="6d41e-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="6d41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d41e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d41e-103">Удаление конфигурации непрерывного экспорта для ресурса аналитики приложения</span><span class="sxs-lookup"><span data-stu-id="6d41e-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6d41e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d41e-104">SYNTAX</span></span>

### <span data-ttu-id="6d41e-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d41e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d41e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d41e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d41e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d41e-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d41e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d41e-108">DESCRIPTION</span></span>
<span data-ttu-id="6d41e-109">Удаление конфигурации непрерывного экспорта для ресурса аналитики приложения</span><span class="sxs-lookup"><span data-stu-id="6d41e-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6d41e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d41e-110">EXAMPLES</span></span>

### <span data-ttu-id="6d41e-111">Пример 1. Удаление непрерывной конфигурации экспорта для ресурса аналитики приложения</span><span class="sxs-lookup"><span data-stu-id="6d41e-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="6d41e-112">Удаление аналитики приложения с непрерывным экспортом с ид "uGOoki0jQsyEs3IdQ83Q4QsNr4=" для ресурса с именем "test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="6d41e-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="6d41e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d41e-113">PARAMETERS</span></span>

### <span data-ttu-id="6d41e-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6d41e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6d41e-115">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="6d41e-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d41e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d41e-116">-DefaultProfile</span></span>
<span data-ttu-id="6d41e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d41e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d41e-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="6d41e-118">-ExportId</span></span>
<span data-ttu-id="6d41e-119">ИД непрерывного экспорта в Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6d41e-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d41e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6d41e-120">-Name</span></span>
<span data-ttu-id="6d41e-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6d41e-121">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d41e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d41e-122">-PassThru</span></span>
<span data-ttu-id="6d41e-123">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="6d41e-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6d41e-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6d41e-124">This parameter is optional.</span></span> <span data-ttu-id="6d41e-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="6d41e-125">Default value is false.</span></span>

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

### <span data-ttu-id="6d41e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d41e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6d41e-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d41e-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d41e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d41e-128">-ResourceId</span></span>
<span data-ttu-id="6d41e-129">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6d41e-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d41e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d41e-130">-Confirm</span></span>
<span data-ttu-id="6d41e-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6d41e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d41e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d41e-132">-WhatIf</span></span>
<span data-ttu-id="6d41e-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d41e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d41e-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6d41e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d41e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d41e-135">CommonParameters</span></span>
<span data-ttu-id="6d41e-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d41e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d41e-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d41e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d41e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d41e-138">INPUTS</span></span>

### <span data-ttu-id="6d41e-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6d41e-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6d41e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6d41e-140">System.String</span></span>

## <span data-ttu-id="6d41e-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d41e-141">OUTPUTS</span></span>

### <span data-ttu-id="6d41e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d41e-142">System.Boolean</span></span>

## <span data-ttu-id="6d41e-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d41e-143">NOTES</span></span>

## <span data-ttu-id="6d41e-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d41e-144">RELATED LINKS</span></span>

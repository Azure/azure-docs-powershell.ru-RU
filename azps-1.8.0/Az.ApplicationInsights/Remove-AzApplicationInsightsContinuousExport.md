---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 0265a273cb575d2cc3a165afae8f7a2090499cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731655"
---
# <span data-ttu-id="31ed9-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="31ed9-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="31ed9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="31ed9-103">Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="31ed9-103">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="31ed9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31ed9-104">SYNTAX</span></span>

### <span data-ttu-id="31ed9-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31ed9-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31ed9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31ed9-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31ed9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31ed9-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ed9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31ed9-108">DESCRIPTION</span></span>
<span data-ttu-id="31ed9-109">Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="31ed9-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="31ed9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31ed9-110">EXAMPLES</span></span>

### <span data-ttu-id="31ed9-111">Пример 1. Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="31ed9-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="31ed9-112">Удаление конфигурации "непрерывное экспортное приложение" с идентификатором экспорта "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="31ed9-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="31ed9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31ed9-113">PARAMETERS</span></span>

### <span data-ttu-id="31ed9-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="31ed9-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="31ed9-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31ed9-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="31ed9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ed9-116">-DefaultProfile</span></span>
<span data-ttu-id="31ed9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31ed9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ed9-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="31ed9-118">-ExportId</span></span>
<span data-ttu-id="31ed9-119">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31ed9-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="31ed9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31ed9-120">-Name</span></span>
<span data-ttu-id="31ed9-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31ed9-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="31ed9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31ed9-122">-PassThru</span></span>
<span data-ttu-id="31ed9-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="31ed9-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="31ed9-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="31ed9-124">This parameter is optional.</span></span> <span data-ttu-id="31ed9-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="31ed9-125">Default value is false.</span></span>

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

### <span data-ttu-id="31ed9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ed9-126">-ResourceGroupName</span></span>
<span data-ttu-id="31ed9-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31ed9-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="31ed9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31ed9-128">-ResourceId</span></span>
<span data-ttu-id="31ed9-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31ed9-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="31ed9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31ed9-130">-Confirm</span></span>
<span data-ttu-id="31ed9-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31ed9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ed9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ed9-132">-WhatIf</span></span>
<span data-ttu-id="31ed9-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31ed9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31ed9-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31ed9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ed9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ed9-135">CommonParameters</span></span>
<span data-ttu-id="31ed9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31ed9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ed9-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ed9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ed9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31ed9-138">INPUTS</span></span>

### <span data-ttu-id="31ed9-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="31ed9-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="31ed9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="31ed9-140">System.String</span></span>

## <span data-ttu-id="31ed9-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31ed9-141">OUTPUTS</span></span>

### <span data-ttu-id="31ed9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31ed9-142">System.Boolean</span></span>

## <span data-ttu-id="31ed9-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="31ed9-143">NOTES</span></span>

## <span data-ttu-id="31ed9-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31ed9-144">RELATED LINKS</span></span>

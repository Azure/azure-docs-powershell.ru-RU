---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249720"
---
# <span data-ttu-id="e7764-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="e7764-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="e7764-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7764-102">SYNOPSIS</span></span>
<span data-ttu-id="e7764-103">Удаление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="e7764-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="e7764-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7764-104">SYNTAX</span></span>

### <span data-ttu-id="e7764-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7764-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7764-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7764-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7764-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7764-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7764-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7764-108">DESCRIPTION</span></span>
<span data-ttu-id="e7764-109">Удаление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="e7764-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="e7764-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7764-110">EXAMPLES</span></span>

### <span data-ttu-id="e7764-111">Пример 1. Удаление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="e7764-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="e7764-112">Удаление конфигурации "непрерывное экспортное приложение" с идентификатором экспорта "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="e7764-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="e7764-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7764-113">PARAMETERS</span></span>

### <span data-ttu-id="e7764-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e7764-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e7764-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e7764-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="e7764-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7764-116">-DefaultProfile</span></span>
<span data-ttu-id="e7764-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7764-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7764-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="e7764-118">-ExportId</span></span>
<span data-ttu-id="e7764-119">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e7764-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="e7764-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7764-120">-Name</span></span>
<span data-ttu-id="e7764-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e7764-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="e7764-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7764-122">-PassThru</span></span>
<span data-ttu-id="e7764-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="e7764-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="e7764-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e7764-124">This parameter is optional.</span></span> <span data-ttu-id="e7764-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="e7764-125">Default value is false.</span></span>

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

### <span data-ttu-id="e7764-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7764-126">-ResourceGroupName</span></span>
<span data-ttu-id="e7764-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7764-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e7764-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7764-128">-ResourceId</span></span>
<span data-ttu-id="e7764-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e7764-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e7764-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7764-130">-Confirm</span></span>
<span data-ttu-id="e7764-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7764-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7764-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7764-132">-WhatIf</span></span>
<span data-ttu-id="e7764-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7764-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7764-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7764-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7764-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7764-135">CommonParameters</span></span>
<span data-ttu-id="e7764-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7764-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7764-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7764-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7764-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7764-138">INPUTS</span></span>

### <span data-ttu-id="e7764-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e7764-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="e7764-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e7764-140">System.String</span></span>

## <span data-ttu-id="e7764-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7764-141">OUTPUTS</span></span>

### <span data-ttu-id="e7764-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7764-142">System.Boolean</span></span>

## <span data-ttu-id="e7764-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7764-143">NOTES</span></span>

## <span data-ttu-id="e7764-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7764-144">RELATED LINKS</span></span>
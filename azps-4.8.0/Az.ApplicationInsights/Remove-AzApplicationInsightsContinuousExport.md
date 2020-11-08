---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242660"
---
# <span data-ttu-id="85acf-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="85acf-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="85acf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85acf-102">SYNOPSIS</span></span>
<span data-ttu-id="85acf-103">Удаление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="85acf-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="85acf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85acf-104">SYNTAX</span></span>

### <span data-ttu-id="85acf-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85acf-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85acf-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85acf-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85acf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85acf-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85acf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85acf-108">DESCRIPTION</span></span>
<span data-ttu-id="85acf-109">Удаление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="85acf-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="85acf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85acf-110">EXAMPLES</span></span>

### <span data-ttu-id="85acf-111">Пример 1. Удаление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="85acf-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="85acf-112">Удаление конфигурации "непрерывное экспортное приложение" с идентификатором экспорта "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="85acf-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="85acf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85acf-113">PARAMETERS</span></span>

### <span data-ttu-id="85acf-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="85acf-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="85acf-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="85acf-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="85acf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85acf-116">-DefaultProfile</span></span>
<span data-ttu-id="85acf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85acf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85acf-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="85acf-118">-ExportId</span></span>
<span data-ttu-id="85acf-119">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="85acf-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="85acf-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85acf-120">-Name</span></span>
<span data-ttu-id="85acf-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="85acf-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="85acf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85acf-122">-PassThru</span></span>
<span data-ttu-id="85acf-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="85acf-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="85acf-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="85acf-124">This parameter is optional.</span></span> <span data-ttu-id="85acf-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="85acf-125">Default value is false.</span></span>

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

### <span data-ttu-id="85acf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85acf-126">-ResourceGroupName</span></span>
<span data-ttu-id="85acf-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85acf-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="85acf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85acf-128">-ResourceId</span></span>
<span data-ttu-id="85acf-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="85acf-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="85acf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85acf-130">-Confirm</span></span>
<span data-ttu-id="85acf-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85acf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85acf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85acf-132">-WhatIf</span></span>
<span data-ttu-id="85acf-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85acf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85acf-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85acf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85acf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85acf-135">CommonParameters</span></span>
<span data-ttu-id="85acf-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85acf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85acf-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85acf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85acf-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85acf-138">INPUTS</span></span>

### <span data-ttu-id="85acf-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="85acf-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="85acf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="85acf-140">System.String</span></span>

## <span data-ttu-id="85acf-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85acf-141">OUTPUTS</span></span>

### <span data-ttu-id="85acf-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85acf-142">System.Boolean</span></span>

## <span data-ttu-id="85acf-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="85acf-143">NOTES</span></span>

## <span data-ttu-id="85acf-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85acf-144">RELATED LINKS</span></span>

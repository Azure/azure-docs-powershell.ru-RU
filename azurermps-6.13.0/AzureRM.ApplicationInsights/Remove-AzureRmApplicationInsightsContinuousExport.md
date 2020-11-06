---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: b9a26a1279b89609728837def1997ac5735ddaea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561208"
---
# <span data-ttu-id="4e345-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="4e345-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="4e345-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e345-102">SYNOPSIS</span></span>
<span data-ttu-id="4e345-103">Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="4e345-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e345-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e345-104">SYNTAX</span></span>

### <span data-ttu-id="4e345-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e345-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e345-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e345-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e345-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e345-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e345-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e345-108">DESCRIPTION</span></span>
<span data-ttu-id="4e345-109">Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="4e345-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="4e345-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e345-110">EXAMPLES</span></span>

### <span data-ttu-id="4e345-111">Пример 1. Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="4e345-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="4e345-112">Удаление конфигурации "непрерывное экспортное приложение" с идентификатором экспорта "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="4e345-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="4e345-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e345-113">PARAMETERS</span></span>

### <span data-ttu-id="4e345-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4e345-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4e345-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4e345-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4e345-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e345-116">-DefaultProfile</span></span>
<span data-ttu-id="4e345-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e345-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="4e345-118">-ExportId</span></span>
<span data-ttu-id="4e345-119">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4e345-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="4e345-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e345-120">-Name</span></span>
<span data-ttu-id="4e345-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4e345-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="4e345-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e345-122">-PassThru</span></span>
<span data-ttu-id="4e345-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="4e345-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="4e345-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4e345-124">This parameter is optional.</span></span> <span data-ttu-id="4e345-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="4e345-125">Default value is false.</span></span>

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

### <span data-ttu-id="4e345-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e345-126">-ResourceGroupName</span></span>
<span data-ttu-id="4e345-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e345-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e345-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e345-128">-ResourceId</span></span>
<span data-ttu-id="4e345-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4e345-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4e345-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e345-130">-Confirm</span></span>
<span data-ttu-id="4e345-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e345-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e345-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e345-132">-WhatIf</span></span>
<span data-ttu-id="4e345-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e345-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e345-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e345-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e345-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e345-135">CommonParameters</span></span>
<span data-ttu-id="4e345-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e345-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e345-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e345-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e345-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e345-138">INPUTS</span></span>

### <span data-ttu-id="4e345-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4e345-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="4e345-140">Параметры: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e345-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="4e345-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4e345-141">System.String</span></span>

## <span data-ttu-id="4e345-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e345-142">OUTPUTS</span></span>

### <span data-ttu-id="4e345-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e345-143">System.Boolean</span></span>

## <span data-ttu-id="4e345-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e345-144">NOTES</span></span>

## <span data-ttu-id="4e345-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e345-145">RELATED LINKS</span></span>

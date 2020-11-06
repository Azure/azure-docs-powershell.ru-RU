---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: ccccfe4ba17fe9d5fc9f35f6604f5f7bb9263d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567484"
---
# <span data-ttu-id="344cd-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="344cd-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="344cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="344cd-102">SYNOPSIS</span></span>
<span data-ttu-id="344cd-103">Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="344cd-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="344cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="344cd-104">SYNTAX</span></span>

### <span data-ttu-id="344cd-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="344cd-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="344cd-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="344cd-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344cd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="344cd-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="344cd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="344cd-108">DESCRIPTION</span></span>
<span data-ttu-id="344cd-109">Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="344cd-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="344cd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="344cd-110">EXAMPLES</span></span>

### <span data-ttu-id="344cd-111">Пример 1. Удаление конфигурации экспорта cotinuous в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="344cd-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="344cd-112">Удаление конфигурации "непрерывное экспортное приложение" с идентификатором экспорта "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="344cd-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="344cd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="344cd-113">PARAMETERS</span></span>

### <span data-ttu-id="344cd-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="344cd-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="344cd-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="344cd-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="344cd-116">-Confirm</span></span>
<span data-ttu-id="344cd-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="344cd-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344cd-118">-DefaultProfile</span></span>
<span data-ttu-id="344cd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="344cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="344cd-120">-ExportId</span></span>
<span data-ttu-id="344cd-121">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="344cd-121">Application Insights Continuous Export ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="344cd-122">-Name</span></span>
<span data-ttu-id="344cd-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="344cd-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="344cd-124">-PassThru</span></span>
<span data-ttu-id="344cd-125">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="344cd-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="344cd-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="344cd-126">This parameter is optional.</span></span> <span data-ttu-id="344cd-127">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="344cd-127">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="344cd-128">-ResourceGroupName</span></span>
<span data-ttu-id="344cd-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="344cd-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="344cd-130">-ResourceId</span></span>
<span data-ttu-id="344cd-131">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="344cd-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="344cd-132">-WhatIf</span></span>
<span data-ttu-id="344cd-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="344cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="344cd-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="344cd-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344cd-135">CommonParameters</span></span>
<span data-ttu-id="344cd-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="344cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344cd-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="344cd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344cd-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="344cd-138">INPUTS</span></span>

### <span data-ttu-id="344cd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="344cd-139">System.String</span></span>

## <span data-ttu-id="344cd-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="344cd-140">OUTPUTS</span></span>

### <span data-ttu-id="344cd-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="344cd-141">System.Object</span></span>

## <span data-ttu-id="344cd-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="344cd-142">NOTES</span></span>

## <span data-ttu-id="344cd-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="344cd-143">RELATED LINKS</span></span>


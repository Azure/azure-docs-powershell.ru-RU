---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: 72a5affb91cbd2c1dfbe78cc7ee86da799b6ae50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556911"
---
# <span data-ttu-id="8dabe-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8dabe-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="8dabe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dabe-102">SYNOPSIS</span></span>
<span data-ttu-id="8dabe-103">Удаление ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="8dabe-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dabe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dabe-104">SYNTAX</span></span>

### <span data-ttu-id="8dabe-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dabe-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dabe-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dabe-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dabe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dabe-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dabe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dabe-108">DESCRIPTION</span></span>
<span data-ttu-id="8dabe-109">Удаление ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="8dabe-109">Remove an application insights resource</span></span>

## <span data-ttu-id="8dabe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dabe-110">EXAMPLES</span></span>

### <span data-ttu-id="8dabe-111">Пример 1. Удалите ресурс Application Insights</span><span class="sxs-lookup"><span data-stu-id="8dabe-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="8dabe-112">Удаление ресурса Insights applciation с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="8dabe-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8dabe-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dabe-113">PARAMETERS</span></span>

### <span data-ttu-id="8dabe-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8dabe-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8dabe-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8dabe-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8dabe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dabe-116">-DefaultProfile</span></span>
<span data-ttu-id="8dabe-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dabe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dabe-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dabe-118">-Name</span></span>
<span data-ttu-id="8dabe-119">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8dabe-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8dabe-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dabe-120">-PassThru</span></span>
<span data-ttu-id="8dabe-121">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="8dabe-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="8dabe-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8dabe-122">This parameter is optional.</span></span> <span data-ttu-id="8dabe-123">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="8dabe-123">Default value is false.</span></span>

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

### <span data-ttu-id="8dabe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dabe-124">-ResourceGroupName</span></span>
<span data-ttu-id="8dabe-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dabe-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8dabe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dabe-126">-ResourceId</span></span>
<span data-ttu-id="8dabe-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8dabe-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8dabe-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dabe-128">-Confirm</span></span>
<span data-ttu-id="8dabe-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dabe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dabe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dabe-130">-WhatIf</span></span>
<span data-ttu-id="8dabe-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dabe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dabe-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dabe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dabe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dabe-133">CommonParameters</span></span>
<span data-ttu-id="8dabe-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dabe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dabe-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dabe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dabe-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dabe-136">INPUTS</span></span>

### <span data-ttu-id="8dabe-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8dabe-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="8dabe-138">Параметры: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8dabe-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="8dabe-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8dabe-139">System.String</span></span>

## <span data-ttu-id="8dabe-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dabe-140">OUTPUTS</span></span>

### <span data-ttu-id="8dabe-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8dabe-141">System.Boolean</span></span>

## <span data-ttu-id="8dabe-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dabe-142">NOTES</span></span>

## <span data-ttu-id="8dabe-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dabe-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: fdd51d73b121feddaf20bbbe48184cc7f565d458
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727897"
---
# <span data-ttu-id="981ef-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="981ef-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="981ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="981ef-102">SYNOPSIS</span></span>
<span data-ttu-id="981ef-103">Удаление ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="981ef-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="981ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="981ef-104">SYNTAX</span></span>

### <span data-ttu-id="981ef-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="981ef-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="981ef-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="981ef-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="981ef-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="981ef-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="981ef-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="981ef-108">DESCRIPTION</span></span>
<span data-ttu-id="981ef-109">Удаление ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="981ef-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="981ef-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="981ef-110">EXAMPLES</span></span>

### <span data-ttu-id="981ef-111">Пример 1. Удалите ключ API Application Insights для ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="981ef-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="981ef-112">Удалите определенный API Application Insights с идентификатором "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" для ресурса "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="981ef-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="981ef-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="981ef-113">PARAMETERS</span></span>

### <span data-ttu-id="981ef-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="981ef-114">-ApiKeyId</span></span>
<span data-ttu-id="981ef-115">Идентификатор ключа API Application Insights.</span><span class="sxs-lookup"><span data-stu-id="981ef-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="981ef-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="981ef-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="981ef-117">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="981ef-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="981ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981ef-118">-DefaultProfile</span></span>
<span data-ttu-id="981ef-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="981ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="981ef-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="981ef-120">-Name</span></span>
<span data-ttu-id="981ef-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="981ef-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="981ef-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="981ef-122">-PassThru</span></span>
<span data-ttu-id="981ef-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="981ef-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="981ef-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="981ef-124">This parameter is optional.</span></span> <span data-ttu-id="981ef-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="981ef-125">Default value is false.</span></span>

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

### <span data-ttu-id="981ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="981ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="981ef-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="981ef-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="981ef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="981ef-128">-ResourceId</span></span>
<span data-ttu-id="981ef-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="981ef-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="981ef-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="981ef-130">-Confirm</span></span>
<span data-ttu-id="981ef-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="981ef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="981ef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="981ef-132">-WhatIf</span></span>
<span data-ttu-id="981ef-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="981ef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="981ef-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="981ef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="981ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981ef-135">CommonParameters</span></span>
<span data-ttu-id="981ef-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="981ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981ef-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981ef-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981ef-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="981ef-138">INPUTS</span></span>

### <span data-ttu-id="981ef-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="981ef-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="981ef-140">System. String</span><span class="sxs-lookup"><span data-stu-id="981ef-140">System.String</span></span>

## <span data-ttu-id="981ef-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="981ef-141">OUTPUTS</span></span>

### <span data-ttu-id="981ef-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="981ef-142">System.Boolean</span></span>

## <span data-ttu-id="981ef-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="981ef-143">NOTES</span></span>

## <span data-ttu-id="981ef-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="981ef-144">RELATED LINKS</span></span>

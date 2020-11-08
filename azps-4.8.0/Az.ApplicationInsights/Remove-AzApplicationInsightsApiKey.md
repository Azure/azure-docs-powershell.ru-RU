---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235128"
---
# <span data-ttu-id="ce123-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ce123-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="ce123-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce123-102">SYNOPSIS</span></span>
<span data-ttu-id="ce123-103">Удаление ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ce123-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="ce123-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce123-104">SYNTAX</span></span>

### <span data-ttu-id="ce123-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce123-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce123-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce123-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce123-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce123-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce123-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce123-108">DESCRIPTION</span></span>
<span data-ttu-id="ce123-109">Удаление ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ce123-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="ce123-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce123-110">EXAMPLES</span></span>

### <span data-ttu-id="ce123-111">Пример 1. Удалите ключ API Application Insights для ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ce123-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="ce123-112">Удалите определенный API Application Insights с идентификатором "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" для ресурса "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="ce123-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="ce123-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce123-113">PARAMETERS</span></span>

### <span data-ttu-id="ce123-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="ce123-114">-ApiKeyId</span></span>
<span data-ttu-id="ce123-115">Идентификатор ключа API Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ce123-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="ce123-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ce123-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ce123-117">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ce123-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ce123-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce123-118">-DefaultProfile</span></span>
<span data-ttu-id="ce123-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce123-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce123-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce123-120">-Name</span></span>
<span data-ttu-id="ce123-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ce123-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ce123-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce123-122">-PassThru</span></span>
<span data-ttu-id="ce123-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="ce123-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="ce123-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ce123-124">This parameter is optional.</span></span> <span data-ttu-id="ce123-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="ce123-125">Default value is false.</span></span>

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

### <span data-ttu-id="ce123-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce123-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce123-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce123-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ce123-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce123-128">-ResourceId</span></span>
<span data-ttu-id="ce123-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ce123-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ce123-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce123-130">-Confirm</span></span>
<span data-ttu-id="ce123-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce123-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce123-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce123-132">-WhatIf</span></span>
<span data-ttu-id="ce123-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce123-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce123-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce123-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce123-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce123-135">CommonParameters</span></span>
<span data-ttu-id="ce123-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce123-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce123-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce123-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce123-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce123-138">INPUTS</span></span>

### <span data-ttu-id="ce123-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ce123-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ce123-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ce123-140">System.String</span></span>

## <span data-ttu-id="ce123-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce123-141">OUTPUTS</span></span>

### <span data-ttu-id="ce123-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce123-142">System.Boolean</span></span>

## <span data-ttu-id="ce123-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce123-143">NOTES</span></span>

## <span data-ttu-id="ce123-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce123-144">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 7fbf269b43868724b015bd087536c49ccce71f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567489"
---
# <span data-ttu-id="9b533-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="9b533-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="9b533-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b533-102">SYNOPSIS</span></span>
<span data-ttu-id="9b533-103">Удаление ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="9b533-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b533-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b533-104">SYNTAX</span></span>

### <span data-ttu-id="9b533-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b533-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b533-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b533-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b533-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b533-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b533-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b533-108">DESCRIPTION</span></span>
<span data-ttu-id="9b533-109">Удаление ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="9b533-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="9b533-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b533-110">EXAMPLES</span></span>

### <span data-ttu-id="9b533-111">Пример 1. Удалите ключ API Application Insights для ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9b533-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="9b533-112">Удалите определенный API Application Insights с идентификатором "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" для ресурса "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="9b533-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="9b533-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b533-113">PARAMETERS</span></span>

### <span data-ttu-id="9b533-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="9b533-114">-ApiKeyId</span></span>
<span data-ttu-id="9b533-115">Идентификатор ключа API Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9b533-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="9b533-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9b533-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9b533-117">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9b533-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="9b533-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b533-118">-Confirm</span></span>
<span data-ttu-id="9b533-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b533-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b533-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b533-120">-DefaultProfile</span></span>
<span data-ttu-id="9b533-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b533-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b533-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b533-122">-Name</span></span>
<span data-ttu-id="9b533-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9b533-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="9b533-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b533-124">-PassThru</span></span>
<span data-ttu-id="9b533-125">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="9b533-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="9b533-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b533-126">This parameter is optional.</span></span> <span data-ttu-id="9b533-127">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="9b533-127">Default value is false.</span></span>

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

### <span data-ttu-id="9b533-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b533-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b533-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b533-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="9b533-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b533-130">-ResourceId</span></span>
<span data-ttu-id="9b533-131">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9b533-131">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9b533-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b533-132">-WhatIf</span></span>
<span data-ttu-id="9b533-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b533-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b533-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b533-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b533-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b533-135">CommonParameters</span></span>
<span data-ttu-id="9b533-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b533-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b533-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b533-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b533-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b533-138">INPUTS</span></span>

### <span data-ttu-id="9b533-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9b533-139">System.String</span></span>

## <span data-ttu-id="9b533-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b533-140">OUTPUTS</span></span>

### <span data-ttu-id="9b533-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="9b533-141">System.Object</span></span>

## <span data-ttu-id="9b533-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b533-142">NOTES</span></span>

## <span data-ttu-id="9b533-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b533-143">RELATED LINKS</span></span>


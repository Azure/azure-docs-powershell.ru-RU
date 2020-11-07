---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 9eb2d3a0dfa960ecd3b3b66ce44a01de64d7f5bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732201"
---
# <span data-ttu-id="bb6c6-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb6c6-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="bb6c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6c6-103">Отключает диагностику для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb6c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb6c6-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb6c6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb6c6-105">DESCRIPTION</span></span>
<span data-ttu-id="bb6c6-106">Командлет **Remove-AzureRmRedisCacheDiagnostics** отключает диагностику кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="bb6c6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb6c6-107">EXAMPLES</span></span>

### <span data-ttu-id="bb6c6-108">Пример 1: отключение диагностики</span><span class="sxs-lookup"><span data-stu-id="bb6c6-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="bb6c6-109">Эта команда отключает диагностику для указанного кэша Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>

<span data-ttu-id="bb6c6-110">Это отключает диагностику для всех кэшей Azure Redis в том же регионе для подписки.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="bb6c6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb6c6-111">PARAMETERS</span></span>

### <span data-ttu-id="bb6c6-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb6c6-112">-Name</span></span>
<span data-ttu-id="bb6c6-113">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-113">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6c6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6c6-114">-ResourceGroupName</span></span>
<span data-ttu-id="bb6c6-115">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-115">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6c6-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb6c6-116">-Confirm</span></span>
<span data-ttu-id="bb6c6-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6c6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6c6-118">-WhatIf</span></span>
<span data-ttu-id="bb6c6-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb6c6-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6c6-121">-DefaultProfile</span></span>
<span data-ttu-id="bb6c6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb6c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6c6-123">CommonParameters</span></span>
<span data-ttu-id="bb6c6-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb6c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6c6-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6c6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6c6-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb6c6-126">INPUTS</span></span>

### <span data-ttu-id="bb6c6-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="bb6c6-127">None</span></span>

## <span data-ttu-id="bb6c6-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb6c6-128">OUTPUTS</span></span>

### <span data-ttu-id="bb6c6-129">Заказы</span><span class="sxs-lookup"><span data-stu-id="bb6c6-129">Void</span></span>

## <span data-ttu-id="bb6c6-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb6c6-130">NOTES</span></span>
* <span data-ttu-id="bb6c6-131">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="bb6c6-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bb6c6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb6c6-132">RELATED LINKS</span></span>

[<span data-ttu-id="bb6c6-133">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb6c6-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)



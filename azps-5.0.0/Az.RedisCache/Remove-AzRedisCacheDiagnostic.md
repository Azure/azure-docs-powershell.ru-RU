---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316075"
---
# <span data-ttu-id="c79e5-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c79e5-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="c79e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c79e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c79e5-103">Отключает диагностику для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c79e5-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="c79e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c79e5-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c79e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c79e5-105">DESCRIPTION</span></span>
<span data-ttu-id="c79e5-106">Командлет **Remove-AzRedisCacheDiagnostic** отключает диагностику кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c79e5-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="c79e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c79e5-107">EXAMPLES</span></span>

### <span data-ttu-id="c79e5-108">Пример 1: отключение диагностики</span><span class="sxs-lookup"><span data-stu-id="c79e5-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="c79e5-109">Эта команда отключает диагностику для указанного кэша Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="c79e5-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="c79e5-110">Это отключает диагностику для всех кэшей Azure Redis в том же регионе для подписки.</span><span class="sxs-lookup"><span data-stu-id="c79e5-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="c79e5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c79e5-111">PARAMETERS</span></span>

### <span data-ttu-id="c79e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79e5-112">-DefaultProfile</span></span>
<span data-ttu-id="c79e5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c79e5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c79e5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c79e5-114">-Name</span></span>
<span data-ttu-id="c79e5-115">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="c79e5-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="c79e5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79e5-116">-ResourceGroupName</span></span>
<span data-ttu-id="c79e5-117">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="c79e5-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79e5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c79e5-118">-Confirm</span></span>
<span data-ttu-id="c79e5-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c79e5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c79e5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c79e5-120">-WhatIf</span></span>
<span data-ttu-id="c79e5-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c79e5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c79e5-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c79e5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c79e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79e5-123">CommonParameters</span></span>
<span data-ttu-id="c79e5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c79e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79e5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79e5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79e5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c79e5-126">INPUTS</span></span>

### <span data-ttu-id="c79e5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c79e5-127">System.String</span></span>

## <span data-ttu-id="c79e5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c79e5-128">OUTPUTS</span></span>

### <span data-ttu-id="c79e5-129">System. void</span><span class="sxs-lookup"><span data-stu-id="c79e5-129">System.Void</span></span>

## <span data-ttu-id="c79e5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c79e5-130">NOTES</span></span>
* <span data-ttu-id="c79e5-131">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="c79e5-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c79e5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c79e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="c79e5-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c79e5-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)



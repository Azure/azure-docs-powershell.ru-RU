---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559559"
---
# <span data-ttu-id="a1727-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a1727-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a1727-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1727-102">SYNOPSIS</span></span>
<span data-ttu-id="a1727-103">Удаление расписания исправлений.</span><span class="sxs-lookup"><span data-stu-id="a1727-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1727-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1727-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1727-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1727-105">DESCRIPTION</span></span>
<span data-ttu-id="a1727-106">Командлет **Remove-AzureRmRedisCachePatchSchedule** Удаляет расписание исправлений из кэша в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="a1727-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a1727-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1727-107">EXAMPLES</span></span>

### <span data-ttu-id="a1727-108">Пример 1: Удаление расписания исправлений</span><span class="sxs-lookup"><span data-stu-id="a1727-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a1727-109">Эта команда удаляет расписание исправлений из кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="a1727-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a1727-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1727-110">PARAMETERS</span></span>

### <span data-ttu-id="a1727-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1727-111">-Name</span></span>
<span data-ttu-id="a1727-112">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="a1727-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a1727-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1727-113">-ResourceGroupName</span></span>
<span data-ttu-id="a1727-114">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="a1727-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a1727-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1727-115">-Confirm</span></span>
<span data-ttu-id="a1727-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1727-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1727-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1727-117">-WhatIf</span></span>
<span data-ttu-id="a1727-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1727-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1727-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1727-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1727-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1727-120">-DefaultProfile</span></span>
<span data-ttu-id="a1727-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1727-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1727-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1727-122">CommonParameters</span></span>
<span data-ttu-id="a1727-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1727-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1727-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1727-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1727-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1727-125">INPUTS</span></span>

### <span data-ttu-id="a1727-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="a1727-126">None</span></span>
<span data-ttu-id="a1727-127">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="a1727-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a1727-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1727-128">OUTPUTS</span></span>

### <span data-ttu-id="a1727-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="a1727-129">None</span></span>

## <span data-ttu-id="a1727-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1727-130">NOTES</span></span>
* <span data-ttu-id="a1727-131">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="a1727-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a1727-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1727-132">RELATED LINKS</span></span>

[<span data-ttu-id="a1727-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a1727-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a1727-134">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a1727-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a1727-135">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a1727-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077674"
---
# <span data-ttu-id="06173-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06173-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="06173-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06173-102">SYNOPSIS</span></span>
<span data-ttu-id="06173-103">Добавление расписания исправлений.</span><span class="sxs-lookup"><span data-stu-id="06173-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="06173-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06173-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06173-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06173-105">DESCRIPTION</span></span>
<span data-ttu-id="06173-106">Командлет **New-AzRedisCachePatchSchedule** добавляет расписание исправлений в кэш в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="06173-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="06173-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06173-107">EXAMPLES</span></span>

### <span data-ttu-id="06173-108">Пример 1: создание и Добавление расписания исправлений в кэш</span><span class="sxs-lookup"><span data-stu-id="06173-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="06173-109">Эта команда добавляет расписание исправлений в кэш с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="06173-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="06173-110">Параметр "записи" принимает в качестве значения команду, которая использует **New-AzRedisCacheScheduleEntry** для создания расписания.</span><span class="sxs-lookup"><span data-stu-id="06173-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="06173-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06173-111">PARAMETERS</span></span>

### <span data-ttu-id="06173-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06173-112">-DefaultProfile</span></span>
<span data-ttu-id="06173-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06173-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06173-114">-Записи</span><span class="sxs-lookup"><span data-stu-id="06173-114">-Entries</span></span>
<span data-ttu-id="06173-115">Указывает массив расписаний, которые этот командлет задает для кэша.</span><span class="sxs-lookup"><span data-stu-id="06173-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="06173-116">Чтобы получить объект **PSScheduleEntry** , используйте командлет New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="06173-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06173-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06173-117">-Name</span></span>
<span data-ttu-id="06173-118">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="06173-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="06173-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06173-119">-ResourceGroupName</span></span>
<span data-ttu-id="06173-120">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="06173-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="06173-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06173-121">-Confirm</span></span>
<span data-ttu-id="06173-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06173-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06173-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06173-123">-WhatIf</span></span>
<span data-ttu-id="06173-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06173-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06173-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06173-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06173-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06173-126">CommonParameters</span></span>
<span data-ttu-id="06173-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06173-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06173-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06173-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06173-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06173-129">INPUTS</span></span>

### <span data-ttu-id="06173-130">System. String</span><span class="sxs-lookup"><span data-stu-id="06173-130">System.String</span></span>

### <span data-ttu-id="06173-131">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="06173-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="06173-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06173-132">OUTPUTS</span></span>

### <span data-ttu-id="06173-133">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="06173-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="06173-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="06173-134">NOTES</span></span>
* <span data-ttu-id="06173-135">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="06173-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="06173-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06173-136">RELATED LINKS</span></span>

[<span data-ttu-id="06173-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06173-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="06173-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="06173-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="06173-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06173-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


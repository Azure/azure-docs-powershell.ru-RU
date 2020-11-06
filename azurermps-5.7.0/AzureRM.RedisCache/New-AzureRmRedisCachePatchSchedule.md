---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557207"
---
# <span data-ttu-id="532a0-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="532a0-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="532a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="532a0-102">SYNOPSIS</span></span>
<span data-ttu-id="532a0-103">Добавление расписания исправлений.</span><span class="sxs-lookup"><span data-stu-id="532a0-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="532a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="532a0-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="532a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="532a0-105">DESCRIPTION</span></span>
<span data-ttu-id="532a0-106">Командлет **New-AzureRmRedisCachePatchSchedule** добавляет расписание исправлений в кэш в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="532a0-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="532a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="532a0-107">EXAMPLES</span></span>

### <span data-ttu-id="532a0-108">Пример 1: создание и Добавление расписания исправлений в кэш</span><span class="sxs-lookup"><span data-stu-id="532a0-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="532a0-109">Эта команда добавляет расписание исправлений в кэш с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="532a0-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="532a0-110">Параметр "записи" принимает в качестве значения команду, которая использует **New-AzureRmRedisCacheScheduleEntry** для создания расписания.</span><span class="sxs-lookup"><span data-stu-id="532a0-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="532a0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="532a0-111">PARAMETERS</span></span>

### <span data-ttu-id="532a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532a0-112">-DefaultProfile</span></span>
<span data-ttu-id="532a0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="532a0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="532a0-114">-Записи</span><span class="sxs-lookup"><span data-stu-id="532a0-114">-Entries</span></span>
<span data-ttu-id="532a0-115">Указывает массив расписаний, которые этот командлет задает для кэша.</span><span class="sxs-lookup"><span data-stu-id="532a0-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="532a0-116">Чтобы получить объект **PSScheduleEntry** , используйте командлет New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="532a0-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="532a0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="532a0-117">-Name</span></span>
<span data-ttu-id="532a0-118">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="532a0-118">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="532a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="532a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="532a0-120">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="532a0-120">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="532a0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="532a0-121">-Confirm</span></span>
<span data-ttu-id="532a0-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="532a0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="532a0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="532a0-123">-WhatIf</span></span>
<span data-ttu-id="532a0-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="532a0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="532a0-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="532a0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="532a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532a0-126">CommonParameters</span></span>
<span data-ttu-id="532a0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="532a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532a0-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="532a0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532a0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="532a0-129">INPUTS</span></span>

### <span data-ttu-id="532a0-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="532a0-130">None</span></span>
<span data-ttu-id="532a0-131">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="532a0-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="532a0-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="532a0-132">OUTPUTS</span></span>

### <span data-ttu-id="532a0-133">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="532a0-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="532a0-134">Этот командлет возвращает записи расписания исправлений, заданные в кэше.</span><span class="sxs-lookup"><span data-stu-id="532a0-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="532a0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="532a0-135">NOTES</span></span>
* <span data-ttu-id="532a0-136">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="532a0-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="532a0-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="532a0-137">RELATED LINKS</span></span>

[<span data-ttu-id="532a0-138">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="532a0-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="532a0-139">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="532a0-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="532a0-140">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="532a0-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)



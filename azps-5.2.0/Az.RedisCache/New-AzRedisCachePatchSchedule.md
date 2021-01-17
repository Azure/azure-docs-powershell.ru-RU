---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395407"
---
# <span data-ttu-id="8446f-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8446f-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="8446f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8446f-102">SYNOPSIS</span></span>
<span data-ttu-id="8446f-103">Добавляет расписание исправлений.</span><span class="sxs-lookup"><span data-stu-id="8446f-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="8446f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8446f-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8446f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8446f-105">DESCRIPTION</span></span>
<span data-ttu-id="8446f-106">Для **кэша в кэше Azure Redis Cache** добавляется расписание исправлений.</span><span class="sxs-lookup"><span data-stu-id="8446f-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="8446f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8446f-107">EXAMPLES</span></span>

### <span data-ttu-id="8446f-108">Пример 1. Создание и добавление графика исправлений в кэше</span><span class="sxs-lookup"><span data-stu-id="8446f-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="8446f-109">Эта команда добавляет расписание исправлений в кэш RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="8446f-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="8446f-110">Параметр Entries принимает в качестве значения команду, которая использует **New-AzRedisCacheScheduleEntry** для создания расписания.</span><span class="sxs-lookup"><span data-stu-id="8446f-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="8446f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8446f-111">PARAMETERS</span></span>

### <span data-ttu-id="8446f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8446f-112">-DefaultProfile</span></span>
<span data-ttu-id="8446f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8446f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8446f-114">-Entries</span><span class="sxs-lookup"><span data-stu-id="8446f-114">-Entries</span></span>
<span data-ttu-id="8446f-115">Задает массив расписанию, который этот cmdlet устанавливает в кэше.</span><span class="sxs-lookup"><span data-stu-id="8446f-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="8446f-116">Чтобы получить объект **PSScheduleEntry,** воспользуйтесь New-AzRedisCacheScheduleEntry..</span><span class="sxs-lookup"><span data-stu-id="8446f-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="8446f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8446f-117">-Name</span></span>
<span data-ttu-id="8446f-118">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="8446f-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="8446f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8446f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8446f-120">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="8446f-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="8446f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8446f-121">-Confirm</span></span>
<span data-ttu-id="8446f-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8446f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8446f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8446f-123">-WhatIf</span></span>
<span data-ttu-id="8446f-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8446f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8446f-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8446f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8446f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8446f-126">CommonParameters</span></span>
<span data-ttu-id="8446f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8446f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8446f-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8446f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8446f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8446f-129">INPUTS</span></span>

### <span data-ttu-id="8446f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8446f-130">System.String</span></span>

### <span data-ttu-id="8446f-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="8446f-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="8446f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8446f-132">OUTPUTS</span></span>

### <span data-ttu-id="8446f-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="8446f-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="8446f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8446f-134">NOTES</span></span>
* <span data-ttu-id="8446f-135">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, webapp, website</span><span class="sxs-lookup"><span data-stu-id="8446f-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8446f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8446f-136">RELATED LINKS</span></span>

[<span data-ttu-id="8446f-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8446f-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="8446f-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="8446f-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="8446f-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8446f-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)



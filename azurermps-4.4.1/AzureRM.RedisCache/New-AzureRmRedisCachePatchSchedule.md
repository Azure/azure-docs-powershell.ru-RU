---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732418"
---
# <span data-ttu-id="d6e3f-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d6e3f-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="d6e3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e3f-103">Добавление расписания исправлений.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6e3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6e3f-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6e3f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6e3f-105">DESCRIPTION</span></span>
<span data-ttu-id="d6e3f-106">Командлет **New-AzureRmRedisCachePatchSchedule** добавляет расписание исправлений в кэш в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="d6e3f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6e3f-107">EXAMPLES</span></span>

### <span data-ttu-id="d6e3f-108">Пример 1: создание и Добавление расписания исправлений в кэш</span><span class="sxs-lookup"><span data-stu-id="d6e3f-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="d6e3f-109">Эта команда добавляет расписание исправлений в кэш с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="d6e3f-110">Параметр "записи" принимает в качестве значения команду, которая использует **New-AzureRmRedisCacheScheduleEntry** для создания расписания.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="d6e3f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6e3f-111">PARAMETERS</span></span>

### <span data-ttu-id="d6e3f-112">-Записи</span><span class="sxs-lookup"><span data-stu-id="d6e3f-112">-Entries</span></span>
<span data-ttu-id="d6e3f-113">Указывает массив расписаний, которые этот командлет задает для кэша.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-113">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="d6e3f-114">Чтобы получить объект **PSScheduleEntry** , используйте командлет New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-114">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="d6e3f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6e3f-115">-Name</span></span>
<span data-ttu-id="d6e3f-116">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-116">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="d6e3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6e3f-118">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="d6e3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e3f-119">-DefaultProfile</span></span>
<span data-ttu-id="d6e3f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6e3f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e3f-121">CommonParameters</span></span>
<span data-ttu-id="d6e3f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e3f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6e3f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e3f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6e3f-124">INPUTS</span></span>

### <span data-ttu-id="d6e3f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6e3f-125">None</span></span>
<span data-ttu-id="d6e3f-126">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-126">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d6e3f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6e3f-127">OUTPUTS</span></span>

### <span data-ttu-id="d6e3f-128">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d6e3f-128">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="d6e3f-129">Этот командлет возвращает записи расписания исправлений, заданные в кэше.</span><span class="sxs-lookup"><span data-stu-id="d6e3f-129">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="d6e3f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6e3f-130">NOTES</span></span>
* <span data-ttu-id="d6e3f-131">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="d6e3f-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d6e3f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6e3f-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6e3f-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d6e3f-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="d6e3f-134">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d6e3f-134">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="d6e3f-135">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d6e3f-135">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)



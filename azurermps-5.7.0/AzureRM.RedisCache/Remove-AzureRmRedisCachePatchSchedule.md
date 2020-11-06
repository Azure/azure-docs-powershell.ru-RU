---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: dab4333907d50853474ff795d33263846af249b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566922"
---
# <span data-ttu-id="e3bf0-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e3bf0-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="e3bf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bf0-103">Удаление расписания исправлений.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3bf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3bf0-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3bf0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="e3bf0-106">Командлет **Remove-AzureRmRedisCachePatchSchedule** Удаляет расписание исправлений из кэша в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="e3bf0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3bf0-107">EXAMPLES</span></span>

### <span data-ttu-id="e3bf0-108">Пример 1: Удаление расписания исправлений</span><span class="sxs-lookup"><span data-stu-id="e3bf0-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="e3bf0-109">Эта команда удаляет расписание исправлений из кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="e3bf0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3bf0-110">PARAMETERS</span></span>

### <span data-ttu-id="e3bf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bf0-111">-DefaultProfile</span></span>
<span data-ttu-id="e3bf0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3bf0-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3bf0-113">-Name</span></span>
<span data-ttu-id="e3bf0-114">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="e3bf0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3bf0-115">-PassThru</span></span>
<span data-ttu-id="e3bf0-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="e3bf0-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e3bf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3bf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="e3bf0-118">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="e3bf0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3bf0-119">-Confirm</span></span>
<span data-ttu-id="e3bf0-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3bf0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bf0-121">-WhatIf</span></span>
<span data-ttu-id="e3bf0-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3bf0-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3bf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bf0-124">CommonParameters</span></span>
<span data-ttu-id="e3bf0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bf0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3bf0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bf0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3bf0-127">INPUTS</span></span>

### <span data-ttu-id="e3bf0-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="e3bf0-128">None</span></span>
<span data-ttu-id="e3bf0-129">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="e3bf0-129">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="e3bf0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3bf0-130">OUTPUTS</span></span>

### <span data-ttu-id="e3bf0-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="e3bf0-131">None</span></span>

## <span data-ttu-id="e3bf0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3bf0-132">NOTES</span></span>
* <span data-ttu-id="e3bf0-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="e3bf0-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e3bf0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3bf0-134">RELATED LINKS</span></span>

[<span data-ttu-id="e3bf0-135">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e3bf0-135">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="e3bf0-136">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e3bf0-136">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="e3bf0-137">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="e3bf0-137">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)



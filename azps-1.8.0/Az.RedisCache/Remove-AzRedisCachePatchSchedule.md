---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 83fab07a44dd85e000e86597881341cad6c641e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729527"
---
# <span data-ttu-id="30c7d-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="30c7d-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="30c7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="30c7d-103">Удаление расписания исправлений.</span><span class="sxs-lookup"><span data-stu-id="30c7d-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="30c7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30c7d-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="30c7d-106">Командлет **Remove-AzRedisCachePatchSchedule** Удаляет расписание исправлений из кэша в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="30c7d-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="30c7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30c7d-107">EXAMPLES</span></span>

### <span data-ttu-id="30c7d-108">Пример 1: Удаление расписания исправлений</span><span class="sxs-lookup"><span data-stu-id="30c7d-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="30c7d-109">Эта команда удаляет расписание исправлений из кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="30c7d-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="30c7d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30c7d-110">PARAMETERS</span></span>

### <span data-ttu-id="30c7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c7d-111">-DefaultProfile</span></span>
<span data-ttu-id="30c7d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30c7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c7d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30c7d-113">-Name</span></span>
<span data-ttu-id="30c7d-114">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="30c7d-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="30c7d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30c7d-115">-PassThru</span></span>
<span data-ttu-id="30c7d-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="30c7d-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="30c7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="30c7d-118">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="30c7d-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="30c7d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30c7d-119">-Confirm</span></span>
<span data-ttu-id="30c7d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30c7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c7d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c7d-121">-WhatIf</span></span>
<span data-ttu-id="30c7d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30c7d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c7d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30c7d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c7d-124">CommonParameters</span></span>
<span data-ttu-id="30c7d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30c7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c7d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c7d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c7d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30c7d-127">INPUTS</span></span>

### <span data-ttu-id="30c7d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="30c7d-128">System.String</span></span>

## <span data-ttu-id="30c7d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c7d-129">OUTPUTS</span></span>

### <span data-ttu-id="30c7d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30c7d-130">System.Boolean</span></span>

## <span data-ttu-id="30c7d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="30c7d-131">NOTES</span></span>
* <span data-ttu-id="30c7d-132">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="30c7d-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="30c7d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30c7d-133">RELATED LINKS</span></span>

[<span data-ttu-id="30c7d-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="30c7d-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="30c7d-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="30c7d-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="30c7d-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="30c7d-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)



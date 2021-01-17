---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406135"
---
# <span data-ttu-id="8c8bf-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8c8bf-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="8c8bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8bf-103">Удаляет расписание исправлений.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="8c8bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c8bf-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c8bf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c8bf-105">DESCRIPTION</span></span>
<span data-ttu-id="8c8bf-106">Cmdlet **Remove-AzRedisCachePatchSchedule** удаляет расписание исправлений из кэша в кэше Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="8c8bf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c8bf-107">EXAMPLES</span></span>

### <span data-ttu-id="8c8bf-108">Пример 1. Удаление расписания исправлений</span><span class="sxs-lookup"><span data-stu-id="8c8bf-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="8c8bf-109">Эта команда удаляет расписание исправлений из кэша RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="8c8bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c8bf-110">PARAMETERS</span></span>

### <span data-ttu-id="8c8bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8bf-111">-DefaultProfile</span></span>
<span data-ttu-id="8c8bf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c8bf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8c8bf-113">-Name</span></span>
<span data-ttu-id="8c8bf-114">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="8c8bf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c8bf-115">-PassThru</span></span>
<span data-ttu-id="8c8bf-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8c8bf-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8c8bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c8bf-118">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="8c8bf-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c8bf-119">-Confirm</span></span>
<span data-ttu-id="8c8bf-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c8bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c8bf-121">-WhatIf</span></span>
<span data-ttu-id="8c8bf-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c8bf-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c8bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8bf-124">CommonParameters</span></span>
<span data-ttu-id="8c8bf-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8bf-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c8bf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8bf-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c8bf-127">INPUTS</span></span>

### <span data-ttu-id="8c8bf-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8c8bf-128">System.String</span></span>

## <span data-ttu-id="8c8bf-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c8bf-129">OUTPUTS</span></span>

### <span data-ttu-id="8c8bf-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c8bf-130">System.Boolean</span></span>

## <span data-ttu-id="8c8bf-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c8bf-131">NOTES</span></span>
* <span data-ttu-id="8c8bf-132">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="8c8bf-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8c8bf-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c8bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="8c8bf-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8c8bf-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="8c8bf-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8c8bf-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="8c8bf-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="8c8bf-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)



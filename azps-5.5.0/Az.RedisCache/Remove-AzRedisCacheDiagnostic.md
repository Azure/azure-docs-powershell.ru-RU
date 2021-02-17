---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240184"
---
# <span data-ttu-id="7d6d6-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7d6d6-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="7d6d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6d6-103">Отключает диагностику в кэше Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="7d6d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d6d6-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6d6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d6d6-105">DESCRIPTION</span></span>
<span data-ttu-id="7d6d6-106">**Cmdlet Remove-AzRedisCacheDiagnostic** отключает диагностику в кэше Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="7d6d6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d6d6-107">EXAMPLES</span></span>

### <span data-ttu-id="7d6d6-108">Пример 1. Отключение диагностики</span><span class="sxs-lookup"><span data-stu-id="7d6d6-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="7d6d6-109">Эта команда отключает диагностику для указанного кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="7d6d6-110">Это отключает диагностику для всех кэшей Azure Redis в одном регионе для подписки.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="7d6d6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d6d6-111">PARAMETERS</span></span>

### <span data-ttu-id="7d6d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6d6-112">-DefaultProfile</span></span>
<span data-ttu-id="7d6d6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d6d6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7d6d6-114">-Name</span></span>
<span data-ttu-id="7d6d6-115">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="7d6d6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6d6-116">-ResourceGroupName</span></span>
<span data-ttu-id="7d6d6-117">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="7d6d6-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d6d6-118">-Confirm</span></span>
<span data-ttu-id="7d6d6-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6d6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6d6-120">-WhatIf</span></span>
<span data-ttu-id="7d6d6-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6d6-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6d6-123">CommonParameters</span></span>
<span data-ttu-id="7d6d6-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6d6-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6d6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6d6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d6d6-126">INPUTS</span></span>

### <span data-ttu-id="7d6d6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7d6d6-127">System.String</span></span>

## <span data-ttu-id="7d6d6-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d6d6-128">OUTPUTS</span></span>

### <span data-ttu-id="7d6d6-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="7d6d6-129">System.Void</span></span>

## <span data-ttu-id="7d6d6-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d6d6-130">NOTES</span></span>
* <span data-ttu-id="7d6d6-131">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="7d6d6-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7d6d6-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d6d6-132">RELATED LINKS</span></span>

[<span data-ttu-id="7d6d6-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7d6d6-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)



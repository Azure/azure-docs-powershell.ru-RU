---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220620"
---
# <span data-ttu-id="c291f-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c291f-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="c291f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c291f-102">SYNOPSIS</span></span>
<span data-ttu-id="c291f-103">Включает диагностику в кэше Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c291f-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="c291f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c291f-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c291f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c291f-105">DESCRIPTION</span></span>
<span data-ttu-id="c291f-106">Cmdlet **Set-AzRedisCacheDiagnostic** обеспечивает диагностику кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c291f-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="c291f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c291f-107">EXAMPLES</span></span>

### <span data-ttu-id="c291f-108">Пример 1. Включить диагностику</span><span class="sxs-lookup"><span data-stu-id="c291f-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="c291f-109">Эта команда обеспечивает диагностику кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c291f-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="c291f-110">Эта команда включает диагностику или обновляет учетную запись хранения для всех кэшей Azure Redis в одном регионе для подписки.</span><span class="sxs-lookup"><span data-stu-id="c291f-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="c291f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c291f-111">PARAMETERS</span></span>

### <span data-ttu-id="c291f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c291f-112">-DefaultProfile</span></span>
<span data-ttu-id="c291f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c291f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c291f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c291f-114">-Name</span></span>
<span data-ttu-id="c291f-115">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="c291f-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="c291f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c291f-116">-ResourceGroupName</span></span>
<span data-ttu-id="c291f-117">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="c291f-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="c291f-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c291f-118">-StorageAccountId</span></span>
<span data-ttu-id="c291f-119">Определяет ИД ресурса учетной записи хранения, используемой для хранения диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="c291f-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="c291f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c291f-120">-Confirm</span></span>
<span data-ttu-id="c291f-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c291f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c291f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c291f-122">-WhatIf</span></span>
<span data-ttu-id="c291f-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c291f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c291f-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c291f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c291f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c291f-125">CommonParameters</span></span>
<span data-ttu-id="c291f-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c291f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c291f-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c291f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c291f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c291f-128">INPUTS</span></span>

### <span data-ttu-id="c291f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c291f-129">System.String</span></span>

## <span data-ttu-id="c291f-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c291f-130">OUTPUTS</span></span>

### <span data-ttu-id="c291f-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="c291f-131">System.Void</span></span>

## <span data-ttu-id="c291f-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c291f-132">NOTES</span></span>
* <span data-ttu-id="c291f-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="c291f-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c291f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c291f-134">RELATED LINKS</span></span>

[<span data-ttu-id="c291f-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c291f-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235927"
---
# <span data-ttu-id="463a9-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="463a9-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="463a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="463a9-102">SYNOPSIS</span></span>
<span data-ttu-id="463a9-103">Включает диагностику для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="463a9-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="463a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="463a9-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="463a9-105">DESCRIPTION</span></span>
<span data-ttu-id="463a9-106">Командлет **Set-AzRedisCacheDiagnostic** включает диагностику для кэша Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="463a9-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="463a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="463a9-107">EXAMPLES</span></span>

### <span data-ttu-id="463a9-108">Пример 1: включение диагностики</span><span class="sxs-lookup"><span data-stu-id="463a9-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="463a9-109">Эта команда включает диагностику для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="463a9-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="463a9-110">Эта команда включит диагностику или обновить учетную запись хранения для всех кэшей Azure Redis в том же регионе для подписки.</span><span class="sxs-lookup"><span data-stu-id="463a9-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="463a9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="463a9-111">PARAMETERS</span></span>

### <span data-ttu-id="463a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463a9-112">-DefaultProfile</span></span>
<span data-ttu-id="463a9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="463a9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="463a9-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="463a9-114">-Name</span></span>
<span data-ttu-id="463a9-115">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="463a9-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="463a9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463a9-116">-ResourceGroupName</span></span>
<span data-ttu-id="463a9-117">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="463a9-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="463a9-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="463a9-118">-StorageAccountId</span></span>
<span data-ttu-id="463a9-119">Указывает ИД ресурса для учетной записи хранения, которая используется для хранения данных диагностики.</span><span class="sxs-lookup"><span data-stu-id="463a9-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="463a9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="463a9-120">-Confirm</span></span>
<span data-ttu-id="463a9-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="463a9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463a9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463a9-122">-WhatIf</span></span>
<span data-ttu-id="463a9-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="463a9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="463a9-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="463a9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463a9-125">CommonParameters</span></span>
<span data-ttu-id="463a9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="463a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463a9-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463a9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463a9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="463a9-128">INPUTS</span></span>

### <span data-ttu-id="463a9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="463a9-129">System.String</span></span>

## <span data-ttu-id="463a9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="463a9-130">OUTPUTS</span></span>

### <span data-ttu-id="463a9-131">System. void</span><span class="sxs-lookup"><span data-stu-id="463a9-131">System.Void</span></span>

## <span data-ttu-id="463a9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="463a9-132">NOTES</span></span>
* <span data-ttu-id="463a9-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="463a9-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="463a9-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="463a9-134">RELATED LINKS</span></span>

[<span data-ttu-id="463a9-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="463a9-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


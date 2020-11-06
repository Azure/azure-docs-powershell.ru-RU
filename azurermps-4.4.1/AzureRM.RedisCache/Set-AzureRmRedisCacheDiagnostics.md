---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568686"
---
# <span data-ttu-id="de95d-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="de95d-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="de95d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de95d-102">SYNOPSIS</span></span>
<span data-ttu-id="de95d-103">Включает диагностику для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="de95d-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de95d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de95d-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de95d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de95d-105">DESCRIPTION</span></span>
<span data-ttu-id="de95d-106">Командлет **Set-AzureRmRedisCacheDiagnostics** включает диагностику для кэша Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="de95d-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="de95d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de95d-107">EXAMPLES</span></span>

### <span data-ttu-id="de95d-108">Пример 1: включение диагностики</span><span class="sxs-lookup"><span data-stu-id="de95d-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="de95d-109">Эта команда включает диагностику для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="de95d-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="de95d-110">Эта команда включит диагностику или обновить учетную запись хранения для всех кэшей Azure Redis в том же регионе для подписки.</span><span class="sxs-lookup"><span data-stu-id="de95d-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="de95d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de95d-111">PARAMETERS</span></span>

### <span data-ttu-id="de95d-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de95d-112">-Name</span></span>
<span data-ttu-id="de95d-113">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="de95d-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="de95d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de95d-114">-ResourceGroupName</span></span>
<span data-ttu-id="de95d-115">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="de95d-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="de95d-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="de95d-116">-StorageAccountId</span></span>
<span data-ttu-id="de95d-117">Указывает ИД ресурса для учетной записи хранения, которая используется для хранения данных диагностики.</span><span class="sxs-lookup"><span data-stu-id="de95d-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="de95d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de95d-118">-DefaultProfile</span></span>
<span data-ttu-id="de95d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de95d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de95d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de95d-120">CommonParameters</span></span>
<span data-ttu-id="de95d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de95d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de95d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de95d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de95d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de95d-123">INPUTS</span></span>

### <span data-ttu-id="de95d-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="de95d-124">None</span></span>

## <span data-ttu-id="de95d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de95d-125">OUTPUTS</span></span>

### <span data-ttu-id="de95d-126">Заказы</span><span class="sxs-lookup"><span data-stu-id="de95d-126">Void</span></span>

## <span data-ttu-id="de95d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="de95d-127">NOTES</span></span>
* <span data-ttu-id="de95d-128">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="de95d-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="de95d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de95d-129">RELATED LINKS</span></span>

[<span data-ttu-id="de95d-130">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="de95d-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)



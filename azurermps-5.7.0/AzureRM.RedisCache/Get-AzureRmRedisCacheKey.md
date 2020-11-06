---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 67ec6bdcce5121c2a80e1f76ea1081f249f15682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563383"
---
# <span data-ttu-id="61d5a-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="61d5a-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="61d5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="61d5a-103">Возвращает клавиши доступа для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="61d5a-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61d5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61d5a-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61d5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="61d5a-106">Командлет **Get-AzureRmRedisCacheKey** получает ключи доступа для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="61d5a-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="61d5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61d5a-107">EXAMPLES</span></span>

### <span data-ttu-id="61d5a-108">Пример 1: получение клавиш доступа для кэша Redis</span><span class="sxs-lookup"><span data-stu-id="61d5a-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="61d5a-109">Эта команда получает клавиши доступа с именем MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="61d5a-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="61d5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61d5a-110">PARAMETERS</span></span>

### <span data-ttu-id="61d5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d5a-111">-DefaultProfile</span></span>
<span data-ttu-id="61d5a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61d5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61d5a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61d5a-113">-Name</span></span>
<span data-ttu-id="61d5a-114">Указывает имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="61d5a-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="61d5a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d5a-115">-ResourceGroupName</span></span>
<span data-ttu-id="61d5a-116">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="61d5a-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="61d5a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d5a-117">CommonParameters</span></span>
<span data-ttu-id="61d5a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61d5a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d5a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d5a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d5a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61d5a-120">INPUTS</span></span>

### <span data-ttu-id="61d5a-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="61d5a-121">None</span></span>
<span data-ttu-id="61d5a-122">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="61d5a-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="61d5a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d5a-123">OUTPUTS</span></span>

### <span data-ttu-id="61d5a-124">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="61d5a-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="61d5a-125">Этот командлет возвращает первичные и вторичные ключи доступа для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="61d5a-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="61d5a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="61d5a-126">NOTES</span></span>

## <span data-ttu-id="61d5a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61d5a-127">RELATED LINKS</span></span>

[<span data-ttu-id="61d5a-128">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="61d5a-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)



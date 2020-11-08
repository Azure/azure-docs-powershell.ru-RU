---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078067"
---
# <span data-ttu-id="3495c-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="3495c-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="3495c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3495c-102">SYNOPSIS</span></span>
<span data-ttu-id="3495c-103">Возвращает клавиши доступа для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="3495c-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="3495c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3495c-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3495c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3495c-105">DESCRIPTION</span></span>
<span data-ttu-id="3495c-106">Командлет **Get-AzRedisCacheKey** получает ключи доступа для кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="3495c-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="3495c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3495c-107">EXAMPLES</span></span>

### <span data-ttu-id="3495c-108">Пример 1: получение клавиш доступа для кэша Redis</span><span class="sxs-lookup"><span data-stu-id="3495c-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="3495c-109">Эта команда получает клавиши доступа с именем MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="3495c-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="3495c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3495c-110">PARAMETERS</span></span>

### <span data-ttu-id="3495c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3495c-111">-DefaultProfile</span></span>
<span data-ttu-id="3495c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3495c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3495c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3495c-113">-Name</span></span>
<span data-ttu-id="3495c-114">Указывает имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="3495c-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="3495c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3495c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3495c-116">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="3495c-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="3495c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3495c-117">CommonParameters</span></span>
<span data-ttu-id="3495c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3495c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3495c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3495c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3495c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3495c-120">INPUTS</span></span>

### <span data-ttu-id="3495c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="3495c-121">System.String</span></span>

## <span data-ttu-id="3495c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3495c-122">OUTPUTS</span></span>

### <span data-ttu-id="3495c-123">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3495c-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="3495c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="3495c-124">NOTES</span></span>

## <span data-ttu-id="3495c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3495c-125">RELATED LINKS</span></span>

[<span data-ttu-id="3495c-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="3495c-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)



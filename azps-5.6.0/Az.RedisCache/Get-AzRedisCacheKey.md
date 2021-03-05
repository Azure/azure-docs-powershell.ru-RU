---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 1d5f230070f8b8c269137e07b04af970f314d564
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987552"
---
# <span data-ttu-id="e6c1b-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="e6c1b-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="e6c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c1b-103">Ключи доступа для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="e6c1b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6c1b-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6c1b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c1b-106">Для кэша Azure Redis Возвращается клавиши доступа для **cmdlet Get-AzRedisCacheKey.**</span><span class="sxs-lookup"><span data-stu-id="e6c1b-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="e6c1b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="e6c1b-108">Пример 1. Получите ключи доступа для кэша Redis</span><span class="sxs-lookup"><span data-stu-id="e6c1b-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="e6c1b-109">Эта команда получает ключи доступа с именем MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="e6c1b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="e6c1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c1b-111">-DefaultProfile</span></span>
<span data-ttu-id="e6c1b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6c1b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e6c1b-113">-Name</span></span>
<span data-ttu-id="e6c1b-114">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="e6c1b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c1b-115">-ResourceGroupName</span></span>
<span data-ttu-id="e6c1b-116">Имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="e6c1b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c1b-117">CommonParameters</span></span>
<span data-ttu-id="e6c1b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c1b-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6c1b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c1b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6c1b-120">INPUTS</span></span>

### <span data-ttu-id="e6c1b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e6c1b-121">System.String</span></span>

## <span data-ttu-id="e6c1b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6c1b-122">OUTPUTS</span></span>

### <span data-ttu-id="e6c1b-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="e6c1b-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="e6c1b-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6c1b-124">NOTES</span></span>

## <span data-ttu-id="e6c1b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6c1b-125">RELATED LINKS</span></span>

[<span data-ttu-id="e6c1b-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="e6c1b-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)



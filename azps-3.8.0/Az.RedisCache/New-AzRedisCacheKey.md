---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065787"
---
# <span data-ttu-id="1b053-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1b053-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="1b053-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b053-102">SYNOPSIS</span></span>
<span data-ttu-id="1b053-103">Повторно создает клавишу доступа для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="1b053-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="1b053-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b053-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b053-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b053-105">DESCRIPTION</span></span>
<span data-ttu-id="1b053-106">Командлет **New-AzRedisCacheKey** заново создает ключ доступа кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="1b053-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="1b053-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b053-107">EXAMPLES</span></span>

### <span data-ttu-id="1b053-108">Пример 1: повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="1b053-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1b053-109">Эта команда повторно создает первичный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="1b053-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="1b053-110">Пример 2: повторное создание вторичного ключа</span><span class="sxs-lookup"><span data-stu-id="1b053-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1b053-111">Эта команда повторно создает вторичный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="1b053-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="1b053-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b053-112">PARAMETERS</span></span>

### <span data-ttu-id="1b053-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b053-113">-DefaultProfile</span></span>
<span data-ttu-id="1b053-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b053-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b053-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1b053-115">-Force</span></span>
<span data-ttu-id="1b053-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b053-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b053-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1b053-117">-KeyType</span></span>
<span data-ttu-id="1b053-118">Указывает, следует ли повторно создавать первичный или вторичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="1b053-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="1b053-119">Допустимые значения: Primary, Secondary.</span><span class="sxs-lookup"><span data-stu-id="1b053-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b053-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b053-120">-Name</span></span>
<span data-ttu-id="1b053-121">Указывает имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="1b053-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="1b053-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b053-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b053-123">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="1b053-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="1b053-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b053-124">-Confirm</span></span>
<span data-ttu-id="1b053-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1b053-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b053-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b053-126">-WhatIf</span></span>
<span data-ttu-id="1b053-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1b053-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b053-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1b053-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b053-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b053-129">CommonParameters</span></span>
<span data-ttu-id="1b053-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b053-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b053-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b053-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b053-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b053-132">INPUTS</span></span>

### <span data-ttu-id="1b053-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1b053-133">System.String</span></span>

## <span data-ttu-id="1b053-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b053-134">OUTPUTS</span></span>

### <span data-ttu-id="1b053-135">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1b053-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="1b053-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b053-136">NOTES</span></span>

## <span data-ttu-id="1b053-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b053-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b053-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1b053-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)



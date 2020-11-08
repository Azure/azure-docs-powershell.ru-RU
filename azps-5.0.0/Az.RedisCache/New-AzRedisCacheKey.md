---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249841"
---
# <span data-ttu-id="e9130-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="e9130-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="e9130-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9130-102">SYNOPSIS</span></span>
<span data-ttu-id="e9130-103">Повторно создает клавишу доступа для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="e9130-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="e9130-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9130-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9130-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9130-105">DESCRIPTION</span></span>
<span data-ttu-id="e9130-106">Командлет **New-AzRedisCacheKey** заново создает ключ доступа кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e9130-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="e9130-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9130-107">EXAMPLES</span></span>

### <span data-ttu-id="e9130-108">Пример 1: повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="e9130-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="e9130-109">Эта команда повторно создает первичный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="e9130-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="e9130-110">Пример 2: повторное создание вторичного ключа</span><span class="sxs-lookup"><span data-stu-id="e9130-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="e9130-111">Эта команда повторно создает вторичный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="e9130-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="e9130-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9130-112">PARAMETERS</span></span>

### <span data-ttu-id="e9130-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9130-113">-DefaultProfile</span></span>
<span data-ttu-id="e9130-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9130-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9130-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e9130-115">-Force</span></span>
<span data-ttu-id="e9130-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9130-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e9130-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e9130-117">-KeyType</span></span>
<span data-ttu-id="e9130-118">Указывает, следует ли повторно создавать первичный или вторичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="e9130-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="e9130-119">Допустимые значения: Primary, Secondary.</span><span class="sxs-lookup"><span data-stu-id="e9130-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="e9130-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9130-120">-Name</span></span>
<span data-ttu-id="e9130-121">Указывает имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="e9130-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="e9130-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9130-122">-ResourceGroupName</span></span>
<span data-ttu-id="e9130-123">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="e9130-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="e9130-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9130-124">-Confirm</span></span>
<span data-ttu-id="e9130-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9130-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9130-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9130-126">-WhatIf</span></span>
<span data-ttu-id="e9130-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9130-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9130-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9130-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9130-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9130-129">CommonParameters</span></span>
<span data-ttu-id="e9130-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9130-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9130-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9130-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9130-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9130-132">INPUTS</span></span>

### <span data-ttu-id="e9130-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e9130-133">System.String</span></span>

## <span data-ttu-id="e9130-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9130-134">OUTPUTS</span></span>

### <span data-ttu-id="e9130-135">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="e9130-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="e9130-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9130-136">NOTES</span></span>

## <span data-ttu-id="e9130-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9130-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9130-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="e9130-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)



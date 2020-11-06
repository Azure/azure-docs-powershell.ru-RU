---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: 51fff2f79435c6806b126fbc0a9c120ee8b8842e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557212"
---
# <span data-ttu-id="67e8b-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="67e8b-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="67e8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="67e8b-103">Повторно создает клавишу доступа для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="67e8b-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67e8b-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e8b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="67e8b-106">Командлет **New-AzureRmRedisCacheKey** заново создает ключ доступа кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="67e8b-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="67e8b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67e8b-107">EXAMPLES</span></span>

### <span data-ttu-id="67e8b-108">Пример 1: повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="67e8b-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="67e8b-109">Эта команда повторно создает первичный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="67e8b-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="67e8b-110">Пример 2: повторное создание вторичного ключа</span><span class="sxs-lookup"><span data-stu-id="67e8b-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="67e8b-111">Эта команда повторно создает вторичный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="67e8b-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="67e8b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67e8b-112">PARAMETERS</span></span>

### <span data-ttu-id="67e8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e8b-113">-DefaultProfile</span></span>
<span data-ttu-id="67e8b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67e8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e8b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="67e8b-115">-Force</span></span>
<span data-ttu-id="67e8b-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="67e8b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e8b-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="67e8b-117">-KeyType</span></span>
<span data-ttu-id="67e8b-118">Указывает, следует ли повторно создавать первичный или вторичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="67e8b-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="67e8b-119">Допустимые значения: Primary, Secondary.</span><span class="sxs-lookup"><span data-stu-id="67e8b-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e8b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67e8b-120">-Name</span></span>
<span data-ttu-id="67e8b-121">Указывает имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="67e8b-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="67e8b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e8b-122">-ResourceGroupName</span></span>
<span data-ttu-id="67e8b-123">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="67e8b-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="67e8b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67e8b-124">-Confirm</span></span>
<span data-ttu-id="67e8b-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67e8b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e8b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e8b-126">-WhatIf</span></span>
<span data-ttu-id="67e8b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67e8b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e8b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67e8b-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e8b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e8b-129">CommonParameters</span></span>
<span data-ttu-id="67e8b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67e8b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e8b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e8b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e8b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67e8b-132">INPUTS</span></span>

### <span data-ttu-id="67e8b-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="67e8b-133">None</span></span>
<span data-ttu-id="67e8b-134">Вы можете передавать входные данные командлету по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="67e8b-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="67e8b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67e8b-135">OUTPUTS</span></span>

### <span data-ttu-id="67e8b-136">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="67e8b-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="67e8b-137">Этот командлет возвращает основной и вторичный ключи доступа кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="67e8b-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="67e8b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="67e8b-138">NOTES</span></span>

## <span data-ttu-id="67e8b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67e8b-139">RELATED LINKS</span></span>

[<span data-ttu-id="67e8b-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="67e8b-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)



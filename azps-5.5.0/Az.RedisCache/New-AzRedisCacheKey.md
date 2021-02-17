---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240229"
---
# <span data-ttu-id="88915-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="88915-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="88915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88915-102">SYNOPSIS</span></span>
<span data-ttu-id="88915-103">Повторное сгенерирует ключ доступа кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="88915-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="88915-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88915-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88915-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88915-105">DESCRIPTION</span></span>
<span data-ttu-id="88915-106">Для повторного сгенерации ключа доступа кэша Azure Redis будет повторно сгенерироваться cmdlet **New-AzRedisCacheKey.**</span><span class="sxs-lookup"><span data-stu-id="88915-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="88915-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88915-107">EXAMPLES</span></span>

### <span data-ttu-id="88915-108">Пример 1. Повторное сгенерировать первичный ключ</span><span class="sxs-lookup"><span data-stu-id="88915-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="88915-109">Эта команда повторно сгенерирует первичный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="88915-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="88915-110">Пример 2. Повторное сгенерировать дополнительный ключ</span><span class="sxs-lookup"><span data-stu-id="88915-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="88915-111">Эта команда повторно сгенерирует дополнительный ключ кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="88915-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="88915-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88915-112">PARAMETERS</span></span>

### <span data-ttu-id="88915-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88915-113">-DefaultProfile</span></span>
<span data-ttu-id="88915-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88915-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88915-115">-Force</span><span class="sxs-lookup"><span data-stu-id="88915-115">-Force</span></span>
<span data-ttu-id="88915-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="88915-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88915-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="88915-117">-KeyType</span></span>
<span data-ttu-id="88915-118">Указывает, следует ли повторно сгенерировать первичный или дополнительный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="88915-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="88915-119">Допустимые значения: Первичный, Дополнительный.</span><span class="sxs-lookup"><span data-stu-id="88915-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="88915-120">-Name</span><span class="sxs-lookup"><span data-stu-id="88915-120">-Name</span></span>
<span data-ttu-id="88915-121">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="88915-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="88915-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88915-122">-ResourceGroupName</span></span>
<span data-ttu-id="88915-123">Имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="88915-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="88915-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88915-124">-Confirm</span></span>
<span data-ttu-id="88915-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="88915-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88915-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88915-126">-WhatIf</span></span>
<span data-ttu-id="88915-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88915-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88915-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="88915-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88915-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88915-129">CommonParameters</span></span>
<span data-ttu-id="88915-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88915-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88915-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88915-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88915-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88915-132">INPUTS</span></span>

### <span data-ttu-id="88915-133">System.String</span><span class="sxs-lookup"><span data-stu-id="88915-133">System.String</span></span>

## <span data-ttu-id="88915-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88915-134">OUTPUTS</span></span>

### <span data-ttu-id="88915-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="88915-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="88915-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88915-136">NOTES</span></span>

## <span data-ttu-id="88915-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88915-137">RELATED LINKS</span></span>

[<span data-ttu-id="88915-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="88915-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 1e9895b78bc61155f7cabfc63e6fb5e4cfbcd30d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729539"
---
# <span data-ttu-id="1a0e4-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a0e4-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="1a0e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0e4-103">Удаление кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="1a0e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a0e4-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a0e4-105">DESCRIPTION</span></span>
<span data-ttu-id="1a0e4-106">Командлет **Remove-AzRedisCache** удаляет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="1a0e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a0e4-107">EXAMPLES</span></span>

### <span data-ttu-id="1a0e4-108">Пример 1: Удаление кэша Redis и возврат результата</span><span class="sxs-lookup"><span data-stu-id="1a0e4-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="1a0e4-109">Эта команда удаляет кэш Redis и показывает, успешно ли выполнена операция.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="1a0e4-110">Пример 2: Удаление кэша Redis и не отображение результата</span><span class="sxs-lookup"><span data-stu-id="1a0e4-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="1a0e4-111">Эта команда удаляет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="1a0e4-112">Так как параметр *PassThru* не указан, результат операции не отображается.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="1a0e4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a0e4-113">PARAMETERS</span></span>

### <span data-ttu-id="1a0e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0e4-114">-DefaultProfile</span></span>
<span data-ttu-id="1a0e4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a0e4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1a0e4-116">-Force</span></span>
<span data-ttu-id="1a0e4-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1a0e4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a0e4-118">-Name</span></span>
<span data-ttu-id="1a0e4-119">Указывает имя кэша Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="1a0e4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a0e4-120">-PassThru</span></span>
<span data-ttu-id="1a0e4-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1a0e4-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1a0e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a0e4-124">Указывает имя группы ресурсов, содержащей кэш Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="1a0e4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a0e4-125">-Confirm</span></span>
<span data-ttu-id="1a0e4-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0e4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a0e4-127">-WhatIf</span></span>
<span data-ttu-id="1a0e4-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a0e4-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0e4-130">CommonParameters</span></span>
<span data-ttu-id="1a0e4-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0e4-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a0e4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0e4-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a0e4-133">INPUTS</span></span>

### <span data-ttu-id="1a0e4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1a0e4-134">System.String</span></span>

## <span data-ttu-id="1a0e4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a0e4-135">OUTPUTS</span></span>

### <span data-ttu-id="1a0e4-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a0e4-136">System.Boolean</span></span>

## <span data-ttu-id="1a0e4-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a0e4-137">NOTES</span></span>

## <span data-ttu-id="1a0e4-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a0e4-138">RELATED LINKS</span></span>

[<span data-ttu-id="1a0e4-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a0e4-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1a0e4-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a0e4-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1a0e4-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a0e4-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)



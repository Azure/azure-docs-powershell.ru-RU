---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505381"
---
# <span data-ttu-id="07b31-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="07b31-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="07b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b31-102">SYNOPSIS</span></span>
<span data-ttu-id="07b31-103">Удаляет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="07b31-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="07b31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07b31-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07b31-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07b31-105">DESCRIPTION</span></span>
<span data-ttu-id="07b31-106">Для **удаления кэша Azure Redis удаляется cmdlet Remove-AzRedisCache.**</span><span class="sxs-lookup"><span data-stu-id="07b31-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="07b31-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07b31-107">EXAMPLES</span></span>

### <span data-ttu-id="07b31-108">Пример 1. Удаление кэша Redis и возврат результата</span><span class="sxs-lookup"><span data-stu-id="07b31-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="07b31-109">Эта команда удаляет кэш Redis и показывает, успешно ли операция.</span><span class="sxs-lookup"><span data-stu-id="07b31-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="07b31-110">Пример 2. Удаление кэша Redis без отображения результата</span><span class="sxs-lookup"><span data-stu-id="07b31-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="07b31-111">Эта команда удаляет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="07b31-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="07b31-112">Так как *параметр PassThru* не указан, результат операции не отображается.</span><span class="sxs-lookup"><span data-stu-id="07b31-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="07b31-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07b31-113">PARAMETERS</span></span>

### <span data-ttu-id="07b31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b31-114">-DefaultProfile</span></span>
<span data-ttu-id="07b31-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07b31-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07b31-116">-Force</span><span class="sxs-lookup"><span data-stu-id="07b31-116">-Force</span></span>
<span data-ttu-id="07b31-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="07b31-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07b31-118">-Name</span><span class="sxs-lookup"><span data-stu-id="07b31-118">-Name</span></span>
<span data-ttu-id="07b31-119">Имя кэша Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="07b31-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="07b31-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07b31-120">-PassThru</span></span>
<span data-ttu-id="07b31-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="07b31-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="07b31-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="07b31-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="07b31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b31-123">-ResourceGroupName</span></span>
<span data-ttu-id="07b31-124">Имя группы ресурсов, которая содержит кэш Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="07b31-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="07b31-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07b31-125">-Confirm</span></span>
<span data-ttu-id="07b31-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07b31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b31-127">-WhatIf</span></span>
<span data-ttu-id="07b31-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07b31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b31-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="07b31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b31-130">CommonParameters</span></span>
<span data-ttu-id="07b31-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07b31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b31-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07b31-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b31-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07b31-133">INPUTS</span></span>

### <span data-ttu-id="07b31-134">System.String</span><span class="sxs-lookup"><span data-stu-id="07b31-134">System.String</span></span>

## <span data-ttu-id="07b31-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07b31-135">OUTPUTS</span></span>

### <span data-ttu-id="07b31-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07b31-136">System.Boolean</span></span>

## <span data-ttu-id="07b31-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07b31-137">NOTES</span></span>

## <span data-ttu-id="07b31-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07b31-138">RELATED LINKS</span></span>

[<span data-ttu-id="07b31-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="07b31-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="07b31-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="07b31-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="07b31-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="07b31-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)



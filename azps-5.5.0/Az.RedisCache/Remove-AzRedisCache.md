---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240189"
---
# <span data-ttu-id="bcfce-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bcfce-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="bcfce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcfce-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfce-103">Удаляет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="bcfce-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="bcfce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcfce-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcfce-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcfce-105">DESCRIPTION</span></span>
<span data-ttu-id="bcfce-106">Для **удаления кэша Azure Redis удаляется cmdlet Remove-AzRedisCache.**</span><span class="sxs-lookup"><span data-stu-id="bcfce-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="bcfce-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcfce-107">EXAMPLES</span></span>

### <span data-ttu-id="bcfce-108">Пример 1. Удаление кэша Redis и возврат результата</span><span class="sxs-lookup"><span data-stu-id="bcfce-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="bcfce-109">Эта команда удаляет кэш Redis и показывает, успешно ли операция.</span><span class="sxs-lookup"><span data-stu-id="bcfce-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="bcfce-110">Пример 2. Удаление кэша Redis без отображения результата</span><span class="sxs-lookup"><span data-stu-id="bcfce-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="bcfce-111">Эта команда удаляет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="bcfce-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="bcfce-112">Так как *параметр PassThru* не указан, результат операции не отображается.</span><span class="sxs-lookup"><span data-stu-id="bcfce-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="bcfce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcfce-113">PARAMETERS</span></span>

### <span data-ttu-id="bcfce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcfce-114">-DefaultProfile</span></span>
<span data-ttu-id="bcfce-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcfce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcfce-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bcfce-116">-Force</span></span>
<span data-ttu-id="bcfce-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bcfce-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcfce-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bcfce-118">-Name</span></span>
<span data-ttu-id="bcfce-119">Имя кэша Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bcfce-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="bcfce-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcfce-120">-PassThru</span></span>
<span data-ttu-id="bcfce-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="bcfce-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bcfce-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bcfce-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bcfce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcfce-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcfce-124">Имя группы ресурсов, которая содержит кэш Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bcfce-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="bcfce-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcfce-125">-Confirm</span></span>
<span data-ttu-id="bcfce-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bcfce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcfce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcfce-127">-WhatIf</span></span>
<span data-ttu-id="bcfce-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcfce-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcfce-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bcfce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcfce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfce-130">CommonParameters</span></span>
<span data-ttu-id="bcfce-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcfce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfce-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcfce-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfce-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcfce-133">INPUTS</span></span>

### <span data-ttu-id="bcfce-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bcfce-134">System.String</span></span>

## <span data-ttu-id="bcfce-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcfce-135">OUTPUTS</span></span>

### <span data-ttu-id="bcfce-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bcfce-136">System.Boolean</span></span>

## <span data-ttu-id="bcfce-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcfce-137">NOTES</span></span>

## <span data-ttu-id="bcfce-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcfce-138">RELATED LINKS</span></span>

[<span data-ttu-id="bcfce-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bcfce-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="bcfce-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bcfce-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="bcfce-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bcfce-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)



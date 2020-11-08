---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234909"
---
# <span data-ttu-id="95f94-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95f94-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="95f94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95f94-102">SYNOPSIS</span></span>
<span data-ttu-id="95f94-103">Удаляет частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="95f94-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="95f94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95f94-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95f94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f94-105">DESCRIPTION</span></span>
<span data-ttu-id="95f94-106">Командлет **Remove-AzPrivateEndpoint** удаляет закрытую конечную точку.</span><span class="sxs-lookup"><span data-stu-id="95f94-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="95f94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95f94-107">EXAMPLES</span></span>

### <span data-ttu-id="95f94-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95f94-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="95f94-109">В этом примере удаляется частная конечная точка с именем MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="95f94-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="95f94-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95f94-110">PARAMETERS</span></span>

### <span data-ttu-id="95f94-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95f94-111">-AsJob</span></span>
<span data-ttu-id="95f94-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="95f94-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95f94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f94-113">-DefaultProfile</span></span>
<span data-ttu-id="95f94-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95f94-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95f94-115">-Force</span><span class="sxs-lookup"><span data-stu-id="95f94-115">-Force</span></span>
<span data-ttu-id="95f94-116">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="95f94-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="95f94-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95f94-117">-Name</span></span>
<span data-ttu-id="95f94-118">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="95f94-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f94-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95f94-119">-PassThru</span></span>
<span data-ttu-id="95f94-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="95f94-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="95f94-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="95f94-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="95f94-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f94-122">-ResourceGroupName</span></span>
<span data-ttu-id="95f94-123">Имя группы ресурсов для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="95f94-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="95f94-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95f94-124">-Confirm</span></span>
<span data-ttu-id="95f94-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95f94-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f94-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95f94-126">-WhatIf</span></span>
<span data-ttu-id="95f94-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95f94-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95f94-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95f94-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f94-129">CommonParameters</span></span>
<span data-ttu-id="95f94-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95f94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f94-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95f94-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f94-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95f94-132">INPUTS</span></span>

### <span data-ttu-id="95f94-133">System. String</span><span class="sxs-lookup"><span data-stu-id="95f94-133">System.String</span></span>

## <span data-ttu-id="95f94-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f94-134">OUTPUTS</span></span>

### <span data-ttu-id="95f94-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95f94-135">System.Boolean</span></span>

## <span data-ttu-id="95f94-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="95f94-136">NOTES</span></span>

## <span data-ttu-id="95f94-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95f94-137">RELATED LINKS</span></span>

[<span data-ttu-id="95f94-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95f94-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="95f94-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95f94-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)
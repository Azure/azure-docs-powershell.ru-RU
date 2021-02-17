---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227572"
---
# <span data-ttu-id="78b1a-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="78b1a-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="78b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="78b1a-103">Удаляет балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="78b1a-103">Removes a load balancer.</span></span>

## <span data-ttu-id="78b1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78b1a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78b1a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="78b1a-106">Для удаления балансиров нагрузки Azure удаляется **cmdlet Remove-AzLoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="78b1a-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="78b1a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="78b1a-108">Пример 1. Удаление балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="78b1a-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="78b1a-109">Эта команда удаляет балансировку нагрузки с именем MyLoadBalancer в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="78b1a-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="78b1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78b1a-110">PARAMETERS</span></span>

### <span data-ttu-id="78b1a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78b1a-111">-AsJob</span></span>
<span data-ttu-id="78b1a-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="78b1a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78b1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b1a-113">-DefaultProfile</span></span>
<span data-ttu-id="78b1a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78b1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78b1a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="78b1a-115">-Force</span></span>
<span data-ttu-id="78b1a-116">Указывает на то, что этот cmdlet удаляет баланс нагрузки независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="78b1a-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="78b1a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="78b1a-117">-Name</span></span>
<span data-ttu-id="78b1a-118">Указывает имя удаляемого балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="78b1a-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="78b1a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78b1a-119">-PassThru</span></span>
<span data-ttu-id="78b1a-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="78b1a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78b1a-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="78b1a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78b1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="78b1a-123">Имя группы ресурсов, которая содержит балансировую нагрузку, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="78b1a-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="78b1a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78b1a-124">-Confirm</span></span>
<span data-ttu-id="78b1a-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78b1a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b1a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b1a-126">-WhatIf</span></span>
<span data-ttu-id="78b1a-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78b1a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b1a-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78b1a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b1a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b1a-129">CommonParameters</span></span>
<span data-ttu-id="78b1a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b1a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b1a-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b1a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b1a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78b1a-132">INPUTS</span></span>

### <span data-ttu-id="78b1a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="78b1a-133">System.String</span></span>

## <span data-ttu-id="78b1a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78b1a-134">OUTPUTS</span></span>

### <span data-ttu-id="78b1a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78b1a-135">System.Boolean</span></span>

## <span data-ttu-id="78b1a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78b1a-136">NOTES</span></span>

## <span data-ttu-id="78b1a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78b1a-137">RELATED LINKS</span></span>

[<span data-ttu-id="78b1a-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="78b1a-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="78b1a-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="78b1a-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="78b1a-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="78b1a-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)



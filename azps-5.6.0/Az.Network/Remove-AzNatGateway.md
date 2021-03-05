---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 430ea183d618779045aaf5d13554edac2ce98626
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996257"
---
# <span data-ttu-id="7f2e9-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7f2e9-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="7f2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2e9-103">Удалить ресурс Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="7f2e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f2e9-104">SYNTAX</span></span>

### <span data-ttu-id="7f2e9-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f2e9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2e9-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f2e9-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2e9-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f2e9-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f2e9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f2e9-108">DESCRIPTION</span></span>
<span data-ttu-id="7f2e9-109">Удаление ресурса Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="7f2e9-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="7f2e9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f2e9-110">EXAMPLES</span></span>

### <span data-ttu-id="7f2e9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f2e9-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="7f2e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f2e9-112">PARAMETERS</span></span>

### <span data-ttu-id="7f2e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f2e9-113">-AsJob</span></span>
<span data-ttu-id="7f2e9-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7f2e9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f2e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2e9-115">-DefaultProfile</span></span>
<span data-ttu-id="7f2e9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f2e9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7f2e9-117">-Force</span></span>
<span data-ttu-id="7f2e9-118">Не спрашивайте подтверждения, если хотите удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="7f2e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f2e9-119">-InputObject</span></span>
<span data-ttu-id="7f2e9-120">Указывает ресурс Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7f2e9-121">-Name</span></span>
<span data-ttu-id="7f2e9-122">Имя ресурса Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f2e9-123">-PassThru</span></span>
<span data-ttu-id="7f2e9-124">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f2e9-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f2e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f2e9-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f2e9-128">-ResourceId</span></span>
<span data-ttu-id="7f2e9-129">ИД ресурса, связанный с шлюзом NAT.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f2e9-130">-Confirm</span></span>
<span data-ttu-id="7f2e9-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2e9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2e9-132">-WhatIf</span></span>
<span data-ttu-id="7f2e9-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f2e9-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2e9-135">CommonParameters</span></span>
<span data-ttu-id="7f2e9-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2e9-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f2e9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2e9-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f2e9-138">INPUTS</span></span>

### <span data-ttu-id="7f2e9-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="7f2e9-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="7f2e9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7f2e9-140">System.String</span></span>

## <span data-ttu-id="7f2e9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f2e9-141">OUTPUTS</span></span>

### <span data-ttu-id="7f2e9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f2e9-142">System.Boolean</span></span>

## <span data-ttu-id="7f2e9-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f2e9-143">NOTES</span></span>

## <span data-ttu-id="7f2e9-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f2e9-144">RELATED LINKS</span></span>

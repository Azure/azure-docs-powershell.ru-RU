---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245958"
---
# <span data-ttu-id="a1168-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a1168-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="a1168-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1168-102">SYNOPSIS</span></span>
<span data-ttu-id="a1168-103">Удалите ресурс шлюз NAT.</span><span class="sxs-lookup"><span data-stu-id="a1168-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="a1168-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1168-104">SYNTAX</span></span>

### <span data-ttu-id="a1168-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1168-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1168-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1168-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1168-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1168-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1168-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1168-108">DESCRIPTION</span></span>
<span data-ttu-id="a1168-109">Удаление ресурса шлюза NAT</span><span class="sxs-lookup"><span data-stu-id="a1168-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="a1168-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1168-110">EXAMPLES</span></span>

### <span data-ttu-id="a1168-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1168-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="a1168-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1168-112">PARAMETERS</span></span>

### <span data-ttu-id="a1168-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1168-113">-AsJob</span></span>
<span data-ttu-id="a1168-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a1168-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1168-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1168-115">-DefaultProfile</span></span>
<span data-ttu-id="a1168-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1168-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1168-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a1168-117">-Force</span></span>
<span data-ttu-id="a1168-118">Не запрашивать подтверждение, если вы хотите удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="a1168-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="a1168-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1168-119">-InputObject</span></span>
<span data-ttu-id="a1168-120">Указывает ресурс шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="a1168-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="a1168-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1168-121">-Name</span></span>
<span data-ttu-id="a1168-122">Имя ресурса шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="a1168-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="a1168-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1168-123">-PassThru</span></span>
<span data-ttu-id="a1168-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a1168-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a1168-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a1168-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1168-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1168-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1168-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1168-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="a1168-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1168-128">-ResourceId</span></span>
<span data-ttu-id="a1168-129">Идентификатор ресурса, связанный с шлюзом NAT.</span><span class="sxs-lookup"><span data-stu-id="a1168-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="a1168-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1168-130">-Confirm</span></span>
<span data-ttu-id="a1168-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1168-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1168-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1168-132">-WhatIf</span></span>
<span data-ttu-id="a1168-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1168-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1168-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1168-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1168-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1168-135">CommonParameters</span></span>
<span data-ttu-id="a1168-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1168-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1168-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1168-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1168-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1168-138">INPUTS</span></span>

### <span data-ttu-id="a1168-139">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a1168-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="a1168-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a1168-140">System.String</span></span>

## <span data-ttu-id="a1168-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1168-141">OUTPUTS</span></span>

### <span data-ttu-id="a1168-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1168-142">System.Boolean</span></span>

## <span data-ttu-id="a1168-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1168-143">NOTES</span></span>

## <span data-ttu-id="a1168-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1168-144">RELATED LINKS</span></span>
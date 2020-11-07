---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: 40a1d9c77d870971f8aa432735f556e89ad55e0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903297"
---
# <span data-ttu-id="ac02c-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ac02c-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="ac02c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac02c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac02c-103">Обновите ресурс шлюза NAT с помощью общедоступного IP-адреса, префикса публичного IP-протокола и IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="ac02c-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="ac02c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac02c-104">SYNTAX</span></span>

### <span data-ttu-id="ac02c-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac02c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac02c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac02c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac02c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac02c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac02c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac02c-108">DESCRIPTION</span></span>
<span data-ttu-id="ac02c-109">Обновите ресурс шлюза NAT с помощью общедоступного IP-адреса, префикса публичного IP-протокола и IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="ac02c-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="ac02c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac02c-110">EXAMPLES</span></span>

### <span data-ttu-id="ac02c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac02c-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="ac02c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac02c-112">PARAMETERS</span></span>

### <span data-ttu-id="ac02c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac02c-113">-AsJob</span></span>
<span data-ttu-id="ac02c-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ac02c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac02c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac02c-115">-DefaultProfile</span></span>
<span data-ttu-id="ac02c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac02c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac02c-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ac02c-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ac02c-118">Тайм-аут простоя шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="ac02c-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac02c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac02c-119">-InputObject</span></span>
<span data-ttu-id="ac02c-120">Указывает ресурс шлюз NAT.</span><span class="sxs-lookup"><span data-stu-id="ac02c-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac02c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac02c-121">-Name</span></span>
<span data-ttu-id="ac02c-122">Имя ресурса шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="ac02c-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac02c-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ac02c-123">-PublicIpAddress</span></span>
<span data-ttu-id="ac02c-124">Массив общедоступных IP-адресов, связанных с ресурсом шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="ac02c-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac02c-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ac02c-125">-PublicIpPrefix</span></span>
<span data-ttu-id="ac02c-126">Массив общедоступных IP-префиксов, связанных с ресурсом шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="ac02c-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac02c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac02c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac02c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac02c-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac02c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac02c-129">-ResourceId</span></span>
<span data-ttu-id="ac02c-130">Указывает идентификатор ресурса шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="ac02c-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac02c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac02c-131">-Confirm</span></span>
<span data-ttu-id="ac02c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac02c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac02c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac02c-133">-WhatIf</span></span>
<span data-ttu-id="ac02c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac02c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac02c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac02c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac02c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac02c-136">CommonParameters</span></span>
<span data-ttu-id="ac02c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac02c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac02c-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac02c-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac02c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac02c-139">INPUTS</span></span>

### <span data-ttu-id="ac02c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ac02c-140">System.String</span></span>

### <span data-ttu-id="ac02c-141">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="ac02c-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ac02c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac02c-142">OUTPUTS</span></span>

### <span data-ttu-id="ac02c-143">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="ac02c-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ac02c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac02c-144">NOTES</span></span>

## <span data-ttu-id="ac02c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac02c-145">RELATED LINKS</span></span>

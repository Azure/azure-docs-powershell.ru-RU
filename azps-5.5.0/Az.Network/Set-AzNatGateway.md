---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236497"
---
# <span data-ttu-id="3c0c6-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3c0c6-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="3c0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0c6-103">Обновление ресурса NAT шлюза с помощью общедоступных IP-адресов, префиксов общедоступных IP-адресов и IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="3c0c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c0c6-104">SYNTAX</span></span>

### <span data-ttu-id="3c0c6-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c0c6-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0c6-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0c6-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c0c6-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0c6-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c0c6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c0c6-108">DESCRIPTION</span></span>
<span data-ttu-id="3c0c6-109">Обновление ресурса NAT шлюза с помощью общедоступных IP-адресов, префиксов общедоступных IP-адресов и IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="3c0c6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c0c6-110">EXAMPLES</span></span>

### <span data-ttu-id="3c0c6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c0c6-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="3c0c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c0c6-112">PARAMETERS</span></span>

### <span data-ttu-id="3c0c6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c0c6-113">-AsJob</span></span>
<span data-ttu-id="3c0c6-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3c0c6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c0c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0c6-115">-DefaultProfile</span></span>
<span data-ttu-id="3c0c6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c0c6-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3c0c6-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3c0c6-118">Неавратное время ожидания шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="3c0c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c0c6-119">-InputObject</span></span>
<span data-ttu-id="3c0c6-120">Указывает ресурс Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="3c0c6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3c0c6-121">-Name</span></span>
<span data-ttu-id="3c0c6-122">Имя ресурса Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="3c0c6-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3c0c6-123">-PublicIpAddress</span></span>
<span data-ttu-id="3c0c6-124">Массив общедоступных IP-адресов, связанных с ресурсом nat шлюза.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="3c0c6-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c0c6-125">-PublicIpPrefix</span></span>
<span data-ttu-id="3c0c6-126">Массив общедоступных IP-префиксов, связанных с ресурсом nat шлюза.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="3c0c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c0c6-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="3c0c6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c0c6-129">-ResourceId</span></span>
<span data-ttu-id="3c0c6-130">Определяет ИД ресурса NAT шлюза.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="3c0c6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c0c6-131">-Confirm</span></span>
<span data-ttu-id="3c0c6-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c0c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c0c6-133">-WhatIf</span></span>
<span data-ttu-id="3c0c6-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c0c6-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c0c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0c6-136">CommonParameters</span></span>
<span data-ttu-id="3c0c6-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0c6-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c0c6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0c6-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c0c6-139">INPUTS</span></span>

### <span data-ttu-id="3c0c6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3c0c6-140">System.String</span></span>

### <span data-ttu-id="3c0c6-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="3c0c6-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="3c0c6-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c0c6-142">OUTPUTS</span></span>

### <span data-ttu-id="3c0c6-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="3c0c6-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="3c0c6-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c0c6-144">NOTES</span></span>

## <span data-ttu-id="3c0c6-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c0c6-145">RELATED LINKS</span></span>

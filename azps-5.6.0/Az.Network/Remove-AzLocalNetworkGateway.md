---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: c8e0e5a3d503b4fa587f2a0bdb284b059bff4eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993656"
---
# <span data-ttu-id="d55e1-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d55e1-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="d55e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d55e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d55e1-103">Удаление локального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="d55e1-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="d55e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d55e1-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d55e1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d55e1-105">DESCRIPTION</span></span>
<span data-ttu-id="d55e1-106">Локальный сетевой шлюз — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="d55e1-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="d55e1-107">Командлет **Remove-AzLocalNetworkGateway** удаляет объект, представляющий ваш собственный шлюз, на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d55e1-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d55e1-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d55e1-108">EXAMPLES</span></span>

### <span data-ttu-id="d55e1-109">Пример 1. Удаление локального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="d55e1-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="d55e1-110">Удаляет объект локального сетевого шлюза с именем MyLocalGW в группе ресурсов MyRG. Сначала необходимо удалить все подключения к локальному сетевому шлюзу с помощью командлета **Remove-AzVirtualNetworkGatewayConnection.**</span><span class="sxs-lookup"><span data-stu-id="d55e1-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="d55e1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d55e1-111">PARAMETERS</span></span>

### <span data-ttu-id="d55e1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d55e1-112">-AsJob</span></span>
<span data-ttu-id="d55e1-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d55e1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d55e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55e1-114">-DefaultProfile</span></span>
<span data-ttu-id="d55e1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d55e1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d55e1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d55e1-116">-Force</span></span>
<span data-ttu-id="d55e1-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d55e1-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d55e1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d55e1-118">-Name</span></span>
<span data-ttu-id="d55e1-119">Указывает имя локального сетевого шлюза, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55e1-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d55e1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d55e1-120">-PassThru</span></span>
<span data-ttu-id="d55e1-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d55e1-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d55e1-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d55e1-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d55e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d55e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="d55e1-124">Имя группы ресурсов, которая содержит локальный сетевой шлюз.</span><span class="sxs-lookup"><span data-stu-id="d55e1-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="d55e1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d55e1-125">-Confirm</span></span>
<span data-ttu-id="d55e1-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d55e1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d55e1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d55e1-127">-WhatIf</span></span>
<span data-ttu-id="d55e1-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55e1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d55e1-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d55e1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d55e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55e1-130">CommonParameters</span></span>
<span data-ttu-id="d55e1-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55e1-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d55e1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55e1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d55e1-133">INPUTS</span></span>

### <span data-ttu-id="d55e1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d55e1-134">System.String</span></span>

## <span data-ttu-id="d55e1-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d55e1-135">OUTPUTS</span></span>

### <span data-ttu-id="d55e1-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d55e1-136">System.Boolean</span></span>

## <span data-ttu-id="d55e1-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d55e1-137">NOTES</span></span>

## <span data-ttu-id="d55e1-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d55e1-138">RELATED LINKS</span></span>

[<span data-ttu-id="d55e1-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d55e1-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="d55e1-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d55e1-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="d55e1-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d55e1-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)

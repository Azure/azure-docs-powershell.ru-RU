---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f5ea9c291d23c6378170946ee6b605ec02742ed8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248302"
---
# <span data-ttu-id="ac879-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac879-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ac879-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac879-102">SYNOPSIS</span></span>
<span data-ttu-id="ac879-103">Удаление подключения к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ac879-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="ac879-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac879-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac879-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac879-105">DESCRIPTION</span></span>
<span data-ttu-id="ac879-106">Подключение к шлюзу виртуальной сети является объектом, представляющим туннель IPsec ("сайт-сайт" или "Виртуальная сеть-сеть"), подключенного к шлюзу виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="ac879-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="ac879-107">Командлет **Remove-AzVirtualNetworkGatewayConnection** удаляет объект подключения на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac879-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ac879-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac879-108">EXAMPLES</span></span>

### <span data-ttu-id="ac879-109">Пример 1: Удаление подключения к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ac879-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="ac879-110">Удаляет объект подключения к шлюзу виртуальной сети с именем "myTunnel" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="ac879-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="ac879-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac879-111">PARAMETERS</span></span>

### <span data-ttu-id="ac879-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac879-112">-DefaultProfile</span></span>
<span data-ttu-id="ac879-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac879-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac879-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ac879-114">-Force</span></span>
<span data-ttu-id="ac879-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ac879-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac879-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac879-116">-Name</span></span>
<span data-ttu-id="ac879-117">Указывает имя подключения к шлюзу виртуальной сети, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ac879-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac879-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac879-118">-PassThru</span></span>
<span data-ttu-id="ac879-119">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ac879-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac879-120">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ac879-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac879-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac879-121">-ResourceGroupName</span></span>
<span data-ttu-id="ac879-122">Указывает имя группы ресурсов, которая содержит подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ac879-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="ac879-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac879-123">-Confirm</span></span>
<span data-ttu-id="ac879-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac879-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac879-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac879-125">-WhatIf</span></span>
<span data-ttu-id="ac879-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac879-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac879-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac879-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac879-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac879-128">CommonParameters</span></span>
<span data-ttu-id="ac879-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac879-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac879-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac879-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac879-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac879-131">INPUTS</span></span>

### <span data-ttu-id="ac879-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ac879-132">System.String</span></span>

## <span data-ttu-id="ac879-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac879-133">OUTPUTS</span></span>

### <span data-ttu-id="ac879-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac879-134">System.Boolean</span></span>

## <span data-ttu-id="ac879-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac879-135">NOTES</span></span>

## <span data-ttu-id="ac879-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac879-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac879-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac879-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ac879-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac879-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ac879-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac879-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)

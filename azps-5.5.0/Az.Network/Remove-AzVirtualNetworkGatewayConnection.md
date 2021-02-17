---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f5ea9c291d23c6378170946ee6b605ec02742ed8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225769"
---
# <span data-ttu-id="ea564-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea564-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ea564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea564-102">SYNOPSIS</span></span>
<span data-ttu-id="ea564-103">Удаление подключения виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="ea564-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="ea564-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea564-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea564-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea564-105">DESCRIPTION</span></span>
<span data-ttu-id="ea564-106">Виртуальное подключение к сетевому шлюзу — это объект, представляющий туннель IPsec (Site-to-Site или Vnet-to-Vnet), подключенный к виртуальному сетевому шлюзу в Azure.</span><span class="sxs-lookup"><span data-stu-id="ea564-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="ea564-107">Командлет **Remove-AzVirtualNetworkGatewayConnection** удаляет объект подключения по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea564-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ea564-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea564-108">EXAMPLES</span></span>

### <span data-ttu-id="ea564-109">Пример 1. Удаление подключения виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="ea564-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="ea564-110">Удаляет объект подключения виртуального сетевого шлюза с именем myTunnel в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="ea564-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="ea564-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea564-111">PARAMETERS</span></span>

### <span data-ttu-id="ea564-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea564-112">-DefaultProfile</span></span>
<span data-ttu-id="ea564-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea564-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea564-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ea564-114">-Force</span></span>
<span data-ttu-id="ea564-115">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ea564-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea564-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ea564-116">-Name</span></span>
<span data-ttu-id="ea564-117">Указывает имя подключения виртуального сетевого шлюза, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea564-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea564-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea564-118">-PassThru</span></span>
<span data-ttu-id="ea564-119">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ea564-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea564-120">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ea564-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea564-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea564-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea564-122">Имя группы ресурсов, которая содержит подключение виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="ea564-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="ea564-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea564-123">-Confirm</span></span>
<span data-ttu-id="ea564-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea564-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea564-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea564-125">-WhatIf</span></span>
<span data-ttu-id="ea564-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea564-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea564-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ea564-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea564-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea564-128">CommonParameters</span></span>
<span data-ttu-id="ea564-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea564-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea564-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea564-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea564-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea564-131">INPUTS</span></span>

### <span data-ttu-id="ea564-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ea564-132">System.String</span></span>

## <span data-ttu-id="ea564-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea564-133">OUTPUTS</span></span>

### <span data-ttu-id="ea564-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea564-134">System.Boolean</span></span>

## <span data-ttu-id="ea564-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea564-135">NOTES</span></span>

## <span data-ttu-id="ea564-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea564-136">RELATED LINKS</span></span>

[<span data-ttu-id="ea564-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea564-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ea564-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea564-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ea564-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea564-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)

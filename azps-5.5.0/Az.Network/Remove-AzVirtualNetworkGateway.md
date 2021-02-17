---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225780"
---
# <span data-ttu-id="b005a-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b005a-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="b005a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b005a-102">SYNOPSIS</span></span>
<span data-ttu-id="b005a-103">Удаление виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="b005a-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="b005a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b005a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b005a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b005a-105">DESCRIPTION</span></span>
<span data-ttu-id="b005a-106">Виртуальный сетевой шлюз — это объект, представляющий шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="b005a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b005a-107">Командлет **Get-AzVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b005a-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b005a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b005a-108">EXAMPLES</span></span>

### <span data-ttu-id="b005a-109">Пример 1. Удаление виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="b005a-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b005a-110">Удаляет объект виртуального сетевого шлюза с именем MyGateway в группе ресурсов MyRG. Сначала необходимо удалить все подключения к виртуальному сетевому шлюзу с помощью командлета **Remove-AzVirtualNetworkGatewayConnection.**</span><span class="sxs-lookup"><span data-stu-id="b005a-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="b005a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b005a-111">PARAMETERS</span></span>

### <span data-ttu-id="b005a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b005a-112">-AsJob</span></span>
<span data-ttu-id="b005a-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b005a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b005a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b005a-114">-DefaultProfile</span></span>
<span data-ttu-id="b005a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b005a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b005a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b005a-116">-Force</span></span>
<span data-ttu-id="b005a-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b005a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b005a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b005a-118">-Name</span></span>
<span data-ttu-id="b005a-119">Указывает имя виртуального сетевого шлюза, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b005a-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b005a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b005a-120">-PassThru</span></span>
<span data-ttu-id="b005a-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b005a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b005a-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b005a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b005a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b005a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b005a-124">Имя группы ресурсов, которая содержит виртуальный сетевой шлюз.</span><span class="sxs-lookup"><span data-stu-id="b005a-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="b005a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b005a-125">-Confirm</span></span>
<span data-ttu-id="b005a-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b005a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b005a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b005a-127">-WhatIf</span></span>
<span data-ttu-id="b005a-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b005a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b005a-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b005a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b005a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b005a-130">CommonParameters</span></span>
<span data-ttu-id="b005a-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b005a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b005a-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b005a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b005a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b005a-133">INPUTS</span></span>

### <span data-ttu-id="b005a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b005a-134">System.String</span></span>

## <span data-ttu-id="b005a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b005a-135">OUTPUTS</span></span>

### <span data-ttu-id="b005a-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b005a-136">System.Boolean</span></span>

## <span data-ttu-id="b005a-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b005a-137">NOTES</span></span>

## <span data-ttu-id="b005a-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b005a-138">RELATED LINKS</span></span>

[<span data-ttu-id="b005a-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b005a-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b005a-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b005a-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b005a-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b005a-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b005a-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b005a-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b005a-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b005a-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7815755d9ec5fffe973e0ecb044409f945ee5faa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730108"
---
# <span data-ttu-id="c1039-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1039-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c1039-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1039-102">SYNOPSIS</span></span>
<span data-ttu-id="c1039-103">Удаление шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="c1039-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="c1039-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1039-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1039-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1039-105">DESCRIPTION</span></span>
<span data-ttu-id="c1039-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="c1039-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c1039-107">Командлет **Get-AzVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1039-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c1039-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1039-108">EXAMPLES</span></span>

### <span data-ttu-id="c1039-109">1: Удаление шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="c1039-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c1039-110">Удаляет объект шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG" Примечание. сначала необходимо удалить все подключения к шлюзу виртуальной сети с помощью командлета **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="c1039-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="c1039-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1039-111">PARAMETERS</span></span>

### <span data-ttu-id="c1039-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1039-112">-AsJob</span></span>
<span data-ttu-id="c1039-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c1039-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1039-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1039-114">-DefaultProfile</span></span>
<span data-ttu-id="c1039-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1039-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1039-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c1039-116">-Force</span></span>
<span data-ttu-id="c1039-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1039-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1039-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1039-118">-Name</span></span>
<span data-ttu-id="c1039-119">Указывает имя шлюза виртуальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c1039-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1039-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1039-120">-PassThru</span></span>
<span data-ttu-id="c1039-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c1039-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1039-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c1039-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1039-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1039-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1039-124">Указывает имя группы ресурсов, которая содержит шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c1039-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="c1039-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1039-125">-Confirm</span></span>
<span data-ttu-id="c1039-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1039-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1039-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1039-127">-WhatIf</span></span>
<span data-ttu-id="c1039-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1039-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1039-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1039-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1039-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1039-130">CommonParameters</span></span>
<span data-ttu-id="c1039-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1039-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1039-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1039-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1039-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1039-133">INPUTS</span></span>

### <span data-ttu-id="c1039-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c1039-134">System.String</span></span>

## <span data-ttu-id="c1039-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1039-135">OUTPUTS</span></span>

### <span data-ttu-id="c1039-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1039-136">System.Boolean</span></span>

## <span data-ttu-id="c1039-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1039-137">NOTES</span></span>

## <span data-ttu-id="c1039-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1039-138">RELATED LINKS</span></span>

[<span data-ttu-id="c1039-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1039-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1039-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1039-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1039-141">Сброс — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1039-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1039-142">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1039-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1039-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1039-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 945f1d8d12b4a493ca361c04ae14cd899f91956f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734697"
---
# <span data-ttu-id="7c31f-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c31f-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="7c31f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c31f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c31f-103">Удаляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="7c31f-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c31f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c31f-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c31f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c31f-105">DESCRIPTION</span></span>
<span data-ttu-id="7c31f-106">Командлет **Remove-AzureRmVirtualNetwork** удаляет виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="7c31f-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="7c31f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c31f-107">EXAMPLES</span></span>

### <span data-ttu-id="7c31f-108">1: создание и удаление виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7c31f-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="7c31f-109">Этот пример создает виртуальную сеть в группе ресурсов, а затем немедленно удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="7c31f-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="7c31f-110">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="7c31f-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="7c31f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c31f-111">PARAMETERS</span></span>

### <span data-ttu-id="7c31f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c31f-112">-AsJob</span></span>
<span data-ttu-id="7c31f-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7c31f-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c31f-114">-DefaultProfile</span></span>
<span data-ttu-id="7c31f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c31f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7c31f-116">-Force</span></span>
<span data-ttu-id="7c31f-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c31f-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c31f-118">-Name</span></span>
<span data-ttu-id="7c31f-119">Указывает имя виртуальной сети, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="7c31f-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c31f-120">-PassThru</span></span>
<span data-ttu-id="7c31f-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7c31f-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c31f-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7c31f-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c31f-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c31f-124">Указывает имя группы ресурсов, которая содержит виртуальную сеть, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7c31f-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c31f-125">-Confirm</span></span>
<span data-ttu-id="7c31f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c31f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c31f-127">-WhatIf</span></span>
<span data-ttu-id="7c31f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c31f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c31f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c31f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c31f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c31f-130">CommonParameters</span></span>
<span data-ttu-id="7c31f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c31f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c31f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c31f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c31f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c31f-133">INPUTS</span></span>

### <span data-ttu-id="7c31f-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="7c31f-134">None</span></span>
<span data-ttu-id="7c31f-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7c31f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c31f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c31f-136">OUTPUTS</span></span>

## <span data-ttu-id="7c31f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c31f-137">NOTES</span></span>

## <span data-ttu-id="7c31f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c31f-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c31f-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c31f-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7c31f-140">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c31f-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7c31f-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c31f-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)



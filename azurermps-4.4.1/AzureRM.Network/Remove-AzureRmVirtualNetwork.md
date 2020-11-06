---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1ab783b4b5a49793b4f4c91f2f7bc9f5410e5ddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559627"
---
# <span data-ttu-id="8ce7e-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ce7e-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="8ce7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ce7e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce7e-103">Удаляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ce7e-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce7e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ce7e-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce7e-106">Командлет **Remove-AzureRmVirtualNetwork** удаляет виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="8ce7e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ce7e-107">EXAMPLES</span></span>

### <span data-ttu-id="8ce7e-108">1: создание и удаление виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8ce7e-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="8ce7e-109">Этот пример создает виртуальную сеть в группе ресурсов, а затем немедленно удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8ce7e-110">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="8ce7e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ce7e-111">PARAMETERS</span></span>

### <span data-ttu-id="8ce7e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="8ce7e-112">-Force</span></span>
<span data-ttu-id="8ce7e-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ce7e-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ce7e-114">-Name</span></span>
<span data-ttu-id="8ce7e-115">Указывает имя виртуальной сети, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-115">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ce7e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ce7e-116">-PassThru</span></span>
<span data-ttu-id="8ce7e-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8ce7e-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8ce7e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce7e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8ce7e-120">Указывает имя группы ресурсов, которая содержит виртуальную сеть, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-120">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ce7e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ce7e-121">-Confirm</span></span>
<span data-ttu-id="8ce7e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce7e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce7e-123">-WhatIf</span></span>
<span data-ttu-id="8ce7e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ce7e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce7e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce7e-126">-DefaultProfile</span></span>
<span data-ttu-id="8ce7e-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce7e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce7e-128">CommonParameters</span></span>
<span data-ttu-id="8ce7e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce7e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce7e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce7e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ce7e-131">INPUTS</span></span>

## <span data-ttu-id="8ce7e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ce7e-132">OUTPUTS</span></span>

## <span data-ttu-id="8ce7e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ce7e-133">NOTES</span></span>

## <span data-ttu-id="8ce7e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ce7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8ce7e-135">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ce7e-135">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="8ce7e-136">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ce7e-136">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="8ce7e-137">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ce7e-137">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 744b5941335666078f33d04bd053faac51adb4bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065581"
---
# <span data-ttu-id="c6946-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="c6946-101">Add-AzDelegation</span></span>

## <span data-ttu-id="c6946-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6946-102">SYNOPSIS</span></span>
<span data-ttu-id="c6946-103">Добавляет делегирование в подсеть.</span><span class="sxs-lookup"><span data-stu-id="c6946-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="c6946-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6946-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6946-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6946-105">DESCRIPTION</span></span>
<span data-ttu-id="c6946-106">Командлет **Add-AzDelegation** добавляет делегирование служб в подсеть Azure.</span><span class="sxs-lookup"><span data-stu-id="c6946-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="c6946-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6946-107">EXAMPLES</span></span>

### <span data-ttu-id="c6946-108">1: Добавление делегирования</span><span class="sxs-lookup"><span data-stu-id="c6946-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="c6946-109">Первая команда извлекает виртуальную сеть, в которой находится подсеть.</span><span class="sxs-lookup"><span data-stu-id="c6946-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="c6946-110">Вторая команда изолирует подсеть, которой вы хотите делегировать.</span><span class="sxs-lookup"><span data-stu-id="c6946-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="c6946-111">Третья команда добавляет делегирование в подсеть.</span><span class="sxs-lookup"><span data-stu-id="c6946-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="c6946-112">Этот конкретный пример полезен, если вы хотите включить SQL для создания конечных точек интерфейса в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="c6946-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="c6946-113">Последняя команда отправляет обновленную подсеть на сервер для фактического обновления вашей подсети.</span><span class="sxs-lookup"><span data-stu-id="c6946-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="c6946-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6946-114">PARAMETERS</span></span>

### <span data-ttu-id="c6946-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6946-115">-DefaultProfile</span></span>
<span data-ttu-id="c6946-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6946-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6946-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6946-117">-Name</span></span>
<span data-ttu-id="c6946-118">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="c6946-118">The name of the delegation</span></span>

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

### <span data-ttu-id="c6946-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c6946-119">-ServiceName</span></span>
<span data-ttu-id="c6946-120">Имя службы, которой подсеть нужно делегировать.</span><span class="sxs-lookup"><span data-stu-id="c6946-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="c6946-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="c6946-121">-Subnet</span></span>
<span data-ttu-id="c6946-122">Подсеть</span><span class="sxs-lookup"><span data-stu-id="c6946-122">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6946-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6946-123">CommonParameters</span></span>
<span data-ttu-id="c6946-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6946-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6946-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6946-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6946-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6946-126">INPUTS</span></span>

### <span data-ttu-id="c6946-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c6946-127">System.String</span></span>

### <span data-ttu-id="c6946-128">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c6946-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c6946-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6946-129">OUTPUTS</span></span>

### <span data-ttu-id="c6946-130">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c6946-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c6946-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6946-131">NOTES</span></span>

## <span data-ttu-id="c6946-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6946-132">RELATED LINKS</span></span>

<span data-ttu-id="c6946-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="c6946-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>
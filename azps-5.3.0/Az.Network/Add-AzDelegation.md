---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: c915f2e95c8912a071fd949a6c231a1eff79b97b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518162"
---
# <span data-ttu-id="95d28-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="95d28-101">Add-AzDelegation</span></span>

## <span data-ttu-id="95d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d28-102">SYNOPSIS</span></span>
<span data-ttu-id="95d28-103">Добавляет делегирования в подсеть.</span><span class="sxs-lookup"><span data-stu-id="95d28-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="95d28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95d28-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95d28-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95d28-105">DESCRIPTION</span></span>
<span data-ttu-id="95d28-106">В подсети Azure добавляется делегирование службы **Add-AzDelegation.**</span><span class="sxs-lookup"><span data-stu-id="95d28-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="95d28-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95d28-107">EXAMPLES</span></span>

### <span data-ttu-id="95d28-108">Пример 1. Добавление делегирования</span><span class="sxs-lookup"><span data-stu-id="95d28-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="95d28-109">Первая команда извлекает виртуальную сеть, на которой расположена подсеть.</span><span class="sxs-lookup"><span data-stu-id="95d28-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="95d28-110">Вторая команда изолирует подсеть интересов — подсеть, которую вы хотите делегировать.</span><span class="sxs-lookup"><span data-stu-id="95d28-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="95d28-111">Третья команда добавляет делегирования в подсеть.</span><span class="sxs-lookup"><span data-stu-id="95d28-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="95d28-112">Этот конкретный пример будет полезен, если вы хотите включить SQL интерфейса для создания конечных точек интерфейса в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="95d28-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="95d28-113">Конечная команда отправляет обновленную подсеть на сервер для ее обновления.</span><span class="sxs-lookup"><span data-stu-id="95d28-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="95d28-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95d28-114">PARAMETERS</span></span>

### <span data-ttu-id="95d28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d28-115">-DefaultProfile</span></span>
<span data-ttu-id="95d28-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95d28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d28-117">-Name</span><span class="sxs-lookup"><span data-stu-id="95d28-117">-Name</span></span>
<span data-ttu-id="95d28-118">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="95d28-118">The name of the delegation</span></span>

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

### <span data-ttu-id="95d28-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="95d28-119">-ServiceName</span></span>
<span data-ttu-id="95d28-120">Имя службы, которой должна быть делегирована подсеть.</span><span class="sxs-lookup"><span data-stu-id="95d28-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="95d28-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="95d28-121">-Subnet</span></span>
<span data-ttu-id="95d28-122">Подсеть</span><span class="sxs-lookup"><span data-stu-id="95d28-122">The subnet</span></span>

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

### <span data-ttu-id="95d28-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d28-123">CommonParameters</span></span>
<span data-ttu-id="95d28-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d28-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d28-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d28-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d28-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95d28-126">INPUTS</span></span>

### <span data-ttu-id="95d28-127">System.String</span><span class="sxs-lookup"><span data-stu-id="95d28-127">System.String</span></span>

### <span data-ttu-id="95d28-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="95d28-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="95d28-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95d28-129">OUTPUTS</span></span>

### <span data-ttu-id="95d28-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="95d28-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="95d28-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95d28-131">NOTES</span></span>

## <span data-ttu-id="95d28-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95d28-132">RELATED LINKS</span></span>

<span data-ttu-id="95d28-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="95d28-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>
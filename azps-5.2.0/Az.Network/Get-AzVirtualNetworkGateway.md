---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408511"
---
# <span data-ttu-id="bd039-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd039-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="bd039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd039-102">SYNOPSIS</span></span>
<span data-ttu-id="bd039-103">Получает виртуальный сетевой шлюз</span><span class="sxs-lookup"><span data-stu-id="bd039-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="bd039-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd039-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd039-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd039-105">DESCRIPTION</span></span>
<span data-ttu-id="bd039-106">Виртуальный сетевой шлюз — это объект, представляющий шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="bd039-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="bd039-107">Командлет **Get-AzVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd039-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="bd039-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd039-108">EXAMPLES</span></span>

### <span data-ttu-id="bd039-109">Пример 1. Получить виртуальный сетевой шлюз</span><span class="sxs-lookup"><span data-stu-id="bd039-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="bd039-110">Возвращает объект виртуального сетевого шлюза с именем MyGateway1 в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="bd039-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="bd039-111">Пример 2. Получить виртуальный сетевой шлюз</span><span class="sxs-lookup"><span data-stu-id="bd039-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="bd039-112">Возвращает все виртуальные сетевые шлюзы, которые начинаются с myGateway в группе ресурсов MyRG.</span><span class="sxs-lookup"><span data-stu-id="bd039-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="bd039-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd039-113">PARAMETERS</span></span>

### <span data-ttu-id="bd039-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd039-114">-DefaultProfile</span></span>
<span data-ttu-id="bd039-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd039-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd039-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bd039-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bd039-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd039-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bd039-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd039-118">CommonParameters</span></span>
<span data-ttu-id="bd039-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd039-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd039-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd039-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd039-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd039-121">INPUTS</span></span>

### <span data-ttu-id="bd039-122">System.String</span><span class="sxs-lookup"><span data-stu-id="bd039-122">System.String</span></span>

## <span data-ttu-id="bd039-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd039-123">OUTPUTS</span></span>

### <span data-ttu-id="bd039-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd039-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bd039-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd039-125">NOTES</span></span>

## <span data-ttu-id="bd039-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd039-126">RELATED LINKS</span></span>

[<span data-ttu-id="bd039-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd039-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="bd039-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd039-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="bd039-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd039-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="bd039-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd039-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="bd039-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd039-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

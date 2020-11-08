---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248340"
---
# <span data-ttu-id="19cd8-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19cd8-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="19cd8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="19cd8-103">Получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="19cd8-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="19cd8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19cd8-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19cd8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="19cd8-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="19cd8-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="19cd8-107">Командлет **Get-AzVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19cd8-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="19cd8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19cd8-108">EXAMPLES</span></span>

### <span data-ttu-id="19cd8-109">Пример 1: получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="19cd8-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="19cd8-110">Возвращает объект шлюза виртуальной сети с именем "myGateway1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="19cd8-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="19cd8-111">Пример 2: получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="19cd8-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="19cd8-112">Возвращает все виртуальные сетевые шлюзы, которые начинаются с "myGateway" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="19cd8-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="19cd8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19cd8-113">PARAMETERS</span></span>

### <span data-ttu-id="19cd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cd8-114">-DefaultProfile</span></span>
<span data-ttu-id="19cd8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19cd8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19cd8-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19cd8-116">-Name</span></span>
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

### <span data-ttu-id="19cd8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19cd8-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="19cd8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cd8-118">CommonParameters</span></span>
<span data-ttu-id="19cd8-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19cd8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cd8-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19cd8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cd8-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19cd8-121">INPUTS</span></span>

### <span data-ttu-id="19cd8-122">System. String</span><span class="sxs-lookup"><span data-stu-id="19cd8-122">System.String</span></span>

## <span data-ttu-id="19cd8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19cd8-123">OUTPUTS</span></span>

### <span data-ttu-id="19cd8-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19cd8-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="19cd8-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="19cd8-125">NOTES</span></span>

## <span data-ttu-id="19cd8-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19cd8-126">RELATED LINKS</span></span>

[<span data-ttu-id="19cd8-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19cd8-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="19cd8-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19cd8-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="19cd8-129">Сброс — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19cd8-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="19cd8-130">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19cd8-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="19cd8-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19cd8-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

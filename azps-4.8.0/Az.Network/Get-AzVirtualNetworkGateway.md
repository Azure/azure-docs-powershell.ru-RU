---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235503"
---
# <span data-ttu-id="cf8cc-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf8cc-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="cf8cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8cc-103">Получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cf8cc-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="cf8cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf8cc-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf8cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf8cc-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8cc-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="cf8cc-107">Командлет **Get-AzVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="cf8cc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf8cc-108">EXAMPLES</span></span>

### <span data-ttu-id="cf8cc-109">Пример 1: получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cf8cc-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="cf8cc-110">Возвращает объект шлюза виртуальной сети с именем "myGateway1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="cf8cc-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="cf8cc-111">Пример 2: получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cf8cc-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="cf8cc-112">Возвращает все виртуальные сетевые шлюзы, которые начинаются с "myGateway" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="cf8cc-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="cf8cc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf8cc-113">PARAMETERS</span></span>

### <span data-ttu-id="cf8cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8cc-114">-DefaultProfile</span></span>
<span data-ttu-id="cf8cc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf8cc-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf8cc-116">-Name</span></span>
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

### <span data-ttu-id="cf8cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf8cc-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="cf8cc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8cc-118">CommonParameters</span></span>
<span data-ttu-id="cf8cc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8cc-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf8cc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8cc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf8cc-121">INPUTS</span></span>

### <span data-ttu-id="cf8cc-122">System. String</span><span class="sxs-lookup"><span data-stu-id="cf8cc-122">System.String</span></span>

## <span data-ttu-id="cf8cc-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf8cc-123">OUTPUTS</span></span>

### <span data-ttu-id="cf8cc-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf8cc-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="cf8cc-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf8cc-125">NOTES</span></span>

## <span data-ttu-id="cf8cc-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf8cc-126">RELATED LINKS</span></span>

[<span data-ttu-id="cf8cc-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf8cc-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cf8cc-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf8cc-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cf8cc-129">Сброс — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf8cc-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cf8cc-130">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf8cc-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cf8cc-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf8cc-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

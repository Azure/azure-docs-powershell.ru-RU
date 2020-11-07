---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: d837355891f3b8095da0380fd91a9ac58a74acff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902278"
---
# <span data-ttu-id="f6c86-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f6c86-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="f6c86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6c86-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c86-103">Получает параметры IPsec VPN, заданные для шлюза виртуальной сети, для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="f6c86-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="f6c86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6c86-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c86-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c86-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c86-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f6c86-107">Командлет **Get-AzVpnClientIpsecParameter** возвращает объект параметров IPsec VPN, заданных на шлюзе в Azure на основе имени шлюза и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6c86-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="f6c86-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6c86-108">EXAMPLES</span></span>

### <span data-ttu-id="f6c86-109">1: получает параметры IPsec VPN, заданные для шлюза виртуальной сети, для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="f6c86-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="f6c86-110">Возвращает объект параметров IPsec VPN, заданных для шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="f6c86-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="f6c86-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6c86-111">PARAMETERS</span></span>

### <span data-ttu-id="f6c86-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c86-112">-DefaultProfile</span></span>
<span data-ttu-id="f6c86-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c86-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6c86-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6c86-114">-Name</span></span>
<span data-ttu-id="f6c86-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6c86-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c86-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6c86-116">-ResourceGroupName</span></span>
<span data-ttu-id="f6c86-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6c86-117">The resource group name.</span></span>

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

### <span data-ttu-id="f6c86-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c86-118">CommonParameters</span></span>
<span data-ttu-id="f6c86-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6c86-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c86-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6c86-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c86-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6c86-121">INPUTS</span></span>

### <span data-ttu-id="f6c86-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f6c86-122">System.String</span></span>

## <span data-ttu-id="f6c86-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c86-123">OUTPUTS</span></span>

### <span data-ttu-id="f6c86-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="f6c86-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="f6c86-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6c86-125">NOTES</span></span>

## <span data-ttu-id="f6c86-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6c86-126">RELATED LINKS</span></span>

[<span data-ttu-id="f6c86-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f6c86-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="f6c86-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f6c86-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="f6c86-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f6c86-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)

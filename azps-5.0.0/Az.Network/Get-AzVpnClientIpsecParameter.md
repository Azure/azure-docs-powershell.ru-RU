---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246206"
---
# <span data-ttu-id="cf19a-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cf19a-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="cf19a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf19a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf19a-103">Получает параметры IPsec VPN, заданные для шлюза виртуальной сети, для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="cf19a-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="cf19a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf19a-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf19a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf19a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf19a-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="cf19a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="cf19a-107">Командлет **Get-AzVpnClientIpsecParameter** возвращает объект параметров IPsec VPN, заданных на шлюзе в Azure на основе имени шлюза и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf19a-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="cf19a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf19a-108">EXAMPLES</span></span>

### <span data-ttu-id="cf19a-109">Пример 1: Возвращает параметры IPsec VPN, заданные для шлюза виртуальной сети, для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="cf19a-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="cf19a-110">Возвращает объект параметров IPsec VPN, заданных для шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="cf19a-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="cf19a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf19a-111">PARAMETERS</span></span>

### <span data-ttu-id="cf19a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf19a-112">-DefaultProfile</span></span>
<span data-ttu-id="cf19a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf19a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf19a-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf19a-114">-Name</span></span>
<span data-ttu-id="cf19a-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf19a-115">The resource name.</span></span>

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

### <span data-ttu-id="cf19a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf19a-116">-ResourceGroupName</span></span>
<span data-ttu-id="cf19a-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf19a-117">The resource group name.</span></span>

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

### <span data-ttu-id="cf19a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf19a-118">CommonParameters</span></span>
<span data-ttu-id="cf19a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf19a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf19a-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf19a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf19a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf19a-121">INPUTS</span></span>

### <span data-ttu-id="cf19a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="cf19a-122">System.String</span></span>

## <span data-ttu-id="cf19a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf19a-123">OUTPUTS</span></span>

### <span data-ttu-id="cf19a-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="cf19a-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="cf19a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf19a-125">NOTES</span></span>

## <span data-ttu-id="cf19a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf19a-126">RELATED LINKS</span></span>

[<span data-ttu-id="cf19a-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cf19a-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cf19a-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cf19a-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cf19a-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cf19a-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)

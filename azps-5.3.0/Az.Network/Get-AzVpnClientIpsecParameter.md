---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422023"
---
# <span data-ttu-id="dd37a-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd37a-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="dd37a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd37a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd37a-103">Получает параметры VPN Ipsec, заданные на виртуальном сетевом шлюзе для подключения point к сайту.</span><span class="sxs-lookup"><span data-stu-id="dd37a-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="dd37a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd37a-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd37a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd37a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd37a-106">Виртуальный сетевой шлюз — это объект, представляющий шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="dd37a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="dd37a-107">Cmdlet **Get-AzVpnClientIpsecParameter** возвращает объект параметров vpn ipsec, заданный для шлюза в Azure на основе имени шлюза и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd37a-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="dd37a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd37a-108">EXAMPLES</span></span>

### <span data-ttu-id="dd37a-109">Пример 1. Получает параметры VPN Ipsec, заданные на виртуальном сетевом шлюзе для подключения point к сайту.</span><span class="sxs-lookup"><span data-stu-id="dd37a-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="dd37a-110">Возвращает объект параметров ipsec VPN, заданный на виртуальном сетевом шлюзе с именем MyGateway в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="dd37a-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="dd37a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd37a-111">PARAMETERS</span></span>

### <span data-ttu-id="dd37a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd37a-112">-DefaultProfile</span></span>
<span data-ttu-id="dd37a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd37a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd37a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="dd37a-114">-Name</span></span>
<span data-ttu-id="dd37a-115">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd37a-115">The resource name.</span></span>

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

### <span data-ttu-id="dd37a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd37a-116">-ResourceGroupName</span></span>
<span data-ttu-id="dd37a-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd37a-117">The resource group name.</span></span>

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

### <span data-ttu-id="dd37a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd37a-118">CommonParameters</span></span>
<span data-ttu-id="dd37a-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd37a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd37a-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd37a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd37a-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd37a-121">INPUTS</span></span>

### <span data-ttu-id="dd37a-122">System.String</span><span class="sxs-lookup"><span data-stu-id="dd37a-122">System.String</span></span>

## <span data-ttu-id="dd37a-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd37a-123">OUTPUTS</span></span>

### <span data-ttu-id="dd37a-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="dd37a-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="dd37a-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd37a-125">NOTES</span></span>

## <span data-ttu-id="dd37a-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd37a-126">RELATED LINKS</span></span>

[<span data-ttu-id="dd37a-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd37a-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="dd37a-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd37a-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="dd37a-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd37a-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)

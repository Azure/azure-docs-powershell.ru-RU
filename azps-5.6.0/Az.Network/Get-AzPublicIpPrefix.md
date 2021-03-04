---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 6083c87ddf0bd7b2306fdacc6d109ccebc144faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954104"
---
# <span data-ttu-id="d3cbd-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d3cbd-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="d3cbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="d3cbd-103">Возвращает префикс общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="d3cbd-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="d3cbd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3cbd-104">SYNTAX</span></span>

### <span data-ttu-id="d3cbd-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3cbd-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3cbd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3cbd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3cbd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3cbd-107">DESCRIPTION</span></span>
<span data-ttu-id="d3cbd-108">Для получения одного или более общедоступных IP-префиксов в группе ресурсов возвращается один или несколько общедоступных **IP-префиксов Get-AzPublicIpPrefix.**</span><span class="sxs-lookup"><span data-stu-id="d3cbd-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="d3cbd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3cbd-109">EXAMPLES</span></span>

### <span data-ttu-id="d3cbd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3cbd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="d3cbd-111">Эта команда получает общедоступный IP-префикс ресурса с myPublicIpPrefix1 в группе ресурсов myRg</span><span class="sxs-lookup"><span data-stu-id="d3cbd-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="d3cbd-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d3cbd-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="d3cbd-113">Эта команда возвращает все общедоступные ресурсы по IP-префиксу, которые начинаются с myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d3cbd-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="d3cbd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3cbd-114">PARAMETERS</span></span>

### <span data-ttu-id="d3cbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3cbd-115">-DefaultProfile</span></span>
<span data-ttu-id="d3cbd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3cbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3cbd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d3cbd-117">-Name</span></span>
<span data-ttu-id="d3cbd-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d3cbd-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d3cbd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3cbd-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3cbd-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3cbd-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d3cbd-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3cbd-121">-ResourceId</span></span>
<span data-ttu-id="d3cbd-122">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="d3cbd-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3cbd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3cbd-123">CommonParameters</span></span>
<span data-ttu-id="d3cbd-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3cbd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3cbd-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3cbd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3cbd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3cbd-126">INPUTS</span></span>

### <span data-ttu-id="d3cbd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d3cbd-127">System.String</span></span>

## <span data-ttu-id="d3cbd-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3cbd-128">OUTPUTS</span></span>

### <span data-ttu-id="d3cbd-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d3cbd-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="d3cbd-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3cbd-130">NOTES</span></span>

## <span data-ttu-id="d3cbd-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3cbd-131">RELATED LINKS</span></span>

[<span data-ttu-id="d3cbd-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d3cbd-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="d3cbd-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d3cbd-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="d3cbd-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d3cbd-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)

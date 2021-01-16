---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 567fdda7c4f95a1bcdecab172223608ec78ef1f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413919"
---
# <span data-ttu-id="cecef-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cecef-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="cecef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cecef-102">SYNOPSIS</span></span>
<span data-ttu-id="cecef-103">Возвращает префикс общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="cecef-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="cecef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cecef-104">SYNTAX</span></span>

### <span data-ttu-id="cecef-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cecef-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cecef-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecef-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cecef-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cecef-107">DESCRIPTION</span></span>
<span data-ttu-id="cecef-108">Для получения одного или более общедоступных IP-префиксов в группе ресурсов возвращается один или несколько общедоступных **IP-префиксов Get-AzPublicIpPrefix.**</span><span class="sxs-lookup"><span data-stu-id="cecef-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="cecef-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cecef-109">EXAMPLES</span></span>

### <span data-ttu-id="cecef-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cecef-110">Example 1</span></span>
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

<span data-ttu-id="cecef-111">Эта команда получает общедоступный IP-префикс ресурса с myPublicIpPrefix1 в группе ресурсов myRg</span><span class="sxs-lookup"><span data-stu-id="cecef-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="cecef-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cecef-112">Example 2</span></span>
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

<span data-ttu-id="cecef-113">Эта команда возвращает все общедоступные ресурсы по IP-префиксу, которые начинаются с myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="cecef-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="cecef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cecef-114">PARAMETERS</span></span>

### <span data-ttu-id="cecef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cecef-115">-DefaultProfile</span></span>
<span data-ttu-id="cecef-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cecef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cecef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cecef-117">-Name</span></span>
<span data-ttu-id="cecef-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cecef-118">The resource name.</span></span>

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

### <span data-ttu-id="cecef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cecef-119">-ResourceGroupName</span></span>
<span data-ttu-id="cecef-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cecef-120">The resource group name.</span></span>

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

### <span data-ttu-id="cecef-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cecef-121">-ResourceId</span></span>
<span data-ttu-id="cecef-122">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="cecef-122">The resource Id.</span></span>

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

### <span data-ttu-id="cecef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cecef-123">CommonParameters</span></span>
<span data-ttu-id="cecef-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cecef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cecef-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cecef-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cecef-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cecef-126">INPUTS</span></span>

### <span data-ttu-id="cecef-127">System.String</span><span class="sxs-lookup"><span data-stu-id="cecef-127">System.String</span></span>

## <span data-ttu-id="cecef-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cecef-128">OUTPUTS</span></span>

### <span data-ttu-id="cecef-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cecef-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="cecef-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cecef-130">NOTES</span></span>

## <span data-ttu-id="cecef-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cecef-131">RELATED LINKS</span></span>

[<span data-ttu-id="cecef-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cecef-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="cecef-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cecef-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="cecef-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cecef-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)

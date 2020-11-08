---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 35e6496cf8dbbcc9bb183bef2e8c83f7fba4a9b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073298"
---
# <span data-ttu-id="a83fd-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a83fd-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="a83fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a83fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a83fd-103">Получает префикс общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a83fd-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="a83fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a83fd-104">SYNTAX</span></span>

### <span data-ttu-id="a83fd-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a83fd-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a83fd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a83fd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a83fd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a83fd-107">DESCRIPTION</span></span>
<span data-ttu-id="a83fd-108">Командлет **Get-AzPublicIpPrefix** получает один или несколько общедоступных префиксов IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a83fd-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="a83fd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a83fd-109">EXAMPLES</span></span>

### <span data-ttu-id="a83fd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a83fd-110">Example 1</span></span>
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
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="a83fd-111">Эта команда получает ресурс префикса общедоступного IP-адреса с myPublicIpPrefix1 в группе ресурсов myRg</span><span class="sxs-lookup"><span data-stu-id="a83fd-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="a83fd-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a83fd-112">Example 2</span></span>
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
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="a83fd-113">Эта команда получает все ресурсы префиксов общедоступного IP-адреса, которые начинаются с myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="a83fd-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="a83fd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a83fd-114">PARAMETERS</span></span>

### <span data-ttu-id="a83fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83fd-115">-DefaultProfile</span></span>
<span data-ttu-id="a83fd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a83fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a83fd-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a83fd-117">-Name</span></span>
<span data-ttu-id="a83fd-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a83fd-118">The resource name.</span></span>

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

### <span data-ttu-id="a83fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a83fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="a83fd-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a83fd-120">The resource group name.</span></span>

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

### <span data-ttu-id="a83fd-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a83fd-121">-ResourceId</span></span>
<span data-ttu-id="a83fd-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a83fd-122">The resource Id.</span></span>

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

### <span data-ttu-id="a83fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83fd-123">CommonParameters</span></span>
<span data-ttu-id="a83fd-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a83fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83fd-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a83fd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83fd-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a83fd-126">INPUTS</span></span>

### <span data-ttu-id="a83fd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a83fd-127">System.String</span></span>

## <span data-ttu-id="a83fd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a83fd-128">OUTPUTS</span></span>

### <span data-ttu-id="a83fd-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a83fd-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="a83fd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a83fd-130">NOTES</span></span>

## <span data-ttu-id="a83fd-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a83fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="a83fd-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a83fd-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="a83fd-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a83fd-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="a83fd-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a83fd-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)

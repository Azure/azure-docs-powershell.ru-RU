---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074854"
---
# <span data-ttu-id="e0e5d-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0e5d-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="e0e5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e5d-103">Возвращает существующий VpnServerConfiguration для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="e0e5d-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="e0e5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0e5d-104">SYNTAX</span></span>

### <span data-ttu-id="e0e5d-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0e5d-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0e5d-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e5d-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0e5d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0e5d-107">DESCRIPTION</span></span>
<span data-ttu-id="e0e5d-108">Командлет **Get-AzVpnServerConfiguration** возвращает существующий VpnServerConfiguration для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="e0e5d-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="e0e5d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0e5d-109">EXAMPLES</span></span>

### <span data-ttu-id="e0e5d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0e5d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="e0e5d-111">В приведенной выше команде будет получено существующее VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0e5d-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="e0e5d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0e5d-112">PARAMETERS</span></span>

### <span data-ttu-id="e0e5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e5d-113">-DefaultProfile</span></span>
<span data-ttu-id="e0e5d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e5d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0e5d-115">-Name</span></span>
<span data-ttu-id="e0e5d-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e0e5d-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0e5d-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0e5d-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e5d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e5d-119">CommonParameters</span></span>
<span data-ttu-id="e0e5d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0e5d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e5d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e5d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e5d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0e5d-122">INPUTS</span></span>

### <span data-ttu-id="e0e5d-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="e0e5d-123">None</span></span>

## <span data-ttu-id="e0e5d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0e5d-124">OUTPUTS</span></span>

### <span data-ttu-id="e0e5d-125">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0e5d-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="e0e5d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0e5d-126">NOTES</span></span>

## <span data-ttu-id="e0e5d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0e5d-127">RELATED LINKS</span></span>

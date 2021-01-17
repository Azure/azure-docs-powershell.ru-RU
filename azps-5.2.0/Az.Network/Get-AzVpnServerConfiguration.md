---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417655"
---
# <span data-ttu-id="b60b4-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b60b4-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="b60b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b60b4-103">Получает существующую структуру VpnServerConfiguration для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="b60b4-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="b60b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b60b4-104">SYNTAX</span></span>

### <span data-ttu-id="b60b4-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b60b4-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b60b4-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60b4-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b60b4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b60b4-107">DESCRIPTION</span></span>
<span data-ttu-id="b60b4-108">Cmdlet **Get-AzVpnServerConfiguration** возвращает существующую структуру VpnServerConfiguration для подключения point к сайту.</span><span class="sxs-lookup"><span data-stu-id="b60b4-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="b60b4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b60b4-109">EXAMPLES</span></span>

### <span data-ttu-id="b60b4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b60b4-110">Example 1</span></span>
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

<span data-ttu-id="b60b4-111">С помощью этой команды вы получите существующую команду VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b60b4-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="b60b4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b60b4-112">PARAMETERS</span></span>

### <span data-ttu-id="b60b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60b4-113">-DefaultProfile</span></span>
<span data-ttu-id="b60b4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b60b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b60b4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b60b4-115">-Name</span></span>
<span data-ttu-id="b60b4-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b60b4-116">The resource name.</span></span>

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

### <span data-ttu-id="b60b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b60b4-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b60b4-118">The resource group name.</span></span>

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

### <span data-ttu-id="b60b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60b4-119">CommonParameters</span></span>
<span data-ttu-id="b60b4-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60b4-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60b4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60b4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b60b4-122">INPUTS</span></span>

### <span data-ttu-id="b60b4-123">Нет</span><span class="sxs-lookup"><span data-stu-id="b60b4-123">None</span></span>

## <span data-ttu-id="b60b4-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b60b4-124">OUTPUTS</span></span>

### <span data-ttu-id="b60b4-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b60b4-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b60b4-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b60b4-126">NOTES</span></span>

## <span data-ttu-id="b60b4-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b60b4-127">RELATED LINKS</span></span>

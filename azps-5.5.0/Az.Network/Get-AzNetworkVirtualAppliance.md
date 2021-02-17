---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226020"
---
# <span data-ttu-id="fbb52-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="fbb52-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="fbb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb52-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb52-103">"Получить" или "Список сетевых виртуальных устройств".</span><span class="sxs-lookup"><span data-stu-id="fbb52-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="fbb52-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fbb52-104">SYNTAX</span></span>

### <span data-ttu-id="fbb52-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbb52-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb52-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb52-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbb52-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb52-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb52-108">Команды Get-AzNetworkVirtualAppliance получают или перечисляют ресурсы сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="fbb52-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="fbb52-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fbb52-109">EXAMPLES</span></span>

### <span data-ttu-id="fbb52-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbb52-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="fbb52-111">Получите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="fbb52-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="fbb52-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb52-112">PARAMETERS</span></span>

### <span data-ttu-id="fbb52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb52-113">-DefaultProfile</span></span>
<span data-ttu-id="fbb52-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb52-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb52-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fbb52-115">-Name</span></span>
<span data-ttu-id="fbb52-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fbb52-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb52-117">-ResourceGroupName</span></span>
<span data-ttu-id="fbb52-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbb52-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb52-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb52-119">-ResourceId</span></span>
<span data-ttu-id="fbb52-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="fbb52-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb52-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb52-121">CommonParameters</span></span>
<span data-ttu-id="fbb52-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb52-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb52-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbb52-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb52-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbb52-124">INPUTS</span></span>

### <span data-ttu-id="fbb52-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fbb52-125">System.String</span></span>

## <span data-ttu-id="fbb52-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fbb52-126">OUTPUTS</span></span>

### <span data-ttu-id="fbb52-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="fbb52-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="fbb52-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fbb52-128">NOTES</span></span>

## <span data-ttu-id="fbb52-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbb52-129">RELATED LINKS</span></span>

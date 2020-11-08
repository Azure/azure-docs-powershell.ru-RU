---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245984"
---
# <span data-ttu-id="33ced-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="33ced-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="33ced-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33ced-102">SYNOPSIS</span></span>
<span data-ttu-id="33ced-103">Получить или Просмотреть виртуальные сетевые устройства.</span><span class="sxs-lookup"><span data-stu-id="33ced-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="33ced-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33ced-104">SYNTAX</span></span>

### <span data-ttu-id="33ced-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33ced-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33ced-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33ced-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33ced-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33ced-107">DESCRIPTION</span></span>
<span data-ttu-id="33ced-108">Команды Get-AzNetworkVirtualAppliance выводят на экран сетевые устройства виртуальных устройств.</span><span class="sxs-lookup"><span data-stu-id="33ced-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="33ced-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33ced-109">EXAMPLES</span></span>

### <span data-ttu-id="33ced-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33ced-110">Example 1</span></span>
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

<span data-ttu-id="33ced-111">Получите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="33ced-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="33ced-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33ced-112">PARAMETERS</span></span>

### <span data-ttu-id="33ced-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ced-113">-DefaultProfile</span></span>
<span data-ttu-id="33ced-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33ced-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33ced-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33ced-115">-Name</span></span>
<span data-ttu-id="33ced-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="33ced-116">The resource name.</span></span>

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

### <span data-ttu-id="33ced-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ced-117">-ResourceGroupName</span></span>
<span data-ttu-id="33ced-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33ced-118">The resource group name.</span></span>

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

### <span data-ttu-id="33ced-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33ced-119">-ResourceId</span></span>
<span data-ttu-id="33ced-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="33ced-120">The resource Id.</span></span>

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

### <span data-ttu-id="33ced-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ced-121">CommonParameters</span></span>
<span data-ttu-id="33ced-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33ced-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ced-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33ced-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ced-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33ced-124">INPUTS</span></span>

### <span data-ttu-id="33ced-125">System. String</span><span class="sxs-lookup"><span data-stu-id="33ced-125">System.String</span></span>

## <span data-ttu-id="33ced-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33ced-126">OUTPUTS</span></span>

### <span data-ttu-id="33ced-127">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="33ced-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="33ced-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="33ced-128">NOTES</span></span>

## <span data-ttu-id="33ced-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33ced-129">RELATED LINKS</span></span>

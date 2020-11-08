---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235558"
---
# <span data-ttu-id="96657-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="96657-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="96657-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96657-102">SYNOPSIS</span></span>
<span data-ttu-id="96657-103">Получить или Просмотреть виртуальные сетевые устройства.</span><span class="sxs-lookup"><span data-stu-id="96657-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="96657-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96657-104">SYNTAX</span></span>

### <span data-ttu-id="96657-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96657-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96657-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96657-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96657-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96657-107">DESCRIPTION</span></span>
<span data-ttu-id="96657-108">Команды Get-AzNetworkVirtualAppliance выводят на экран сетевые устройства виртуальных устройств.</span><span class="sxs-lookup"><span data-stu-id="96657-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="96657-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96657-109">EXAMPLES</span></span>

### <span data-ttu-id="96657-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96657-110">Example 1</span></span>
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

<span data-ttu-id="96657-111">Получите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="96657-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="96657-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96657-112">PARAMETERS</span></span>

### <span data-ttu-id="96657-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96657-113">-DefaultProfile</span></span>
<span data-ttu-id="96657-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96657-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96657-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96657-115">-Name</span></span>
<span data-ttu-id="96657-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="96657-116">The resource name.</span></span>

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

### <span data-ttu-id="96657-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96657-117">-ResourceGroupName</span></span>
<span data-ttu-id="96657-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96657-118">The resource group name.</span></span>

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

### <span data-ttu-id="96657-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96657-119">-ResourceId</span></span>
<span data-ttu-id="96657-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="96657-120">The resource Id.</span></span>

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

### <span data-ttu-id="96657-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96657-121">CommonParameters</span></span>
<span data-ttu-id="96657-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96657-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96657-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96657-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96657-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96657-124">INPUTS</span></span>

### <span data-ttu-id="96657-125">System. String</span><span class="sxs-lookup"><span data-stu-id="96657-125">System.String</span></span>

## <span data-ttu-id="96657-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96657-126">OUTPUTS</span></span>

### <span data-ttu-id="96657-127">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="96657-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="96657-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="96657-128">NOTES</span></span>

## <span data-ttu-id="96657-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96657-129">RELATED LINKS</span></span>

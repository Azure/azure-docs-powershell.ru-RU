---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e165b481b1321f5ddd81766452120f55f6f0e153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954531"
---
# <span data-ttu-id="10f8e-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="10f8e-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="10f8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="10f8e-103">Получите или перечислите доступные на складе сетевые виртуальные устройства.</span><span class="sxs-lookup"><span data-stu-id="10f8e-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="10f8e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10f8e-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10f8e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10f8e-105">DESCRIPTION</span></span>
<span data-ttu-id="10f8e-106">В Get-AzNetworkVirtualApplianceSku список доступных skus сетевых виртуальных устройств в инвентаризации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="10f8e-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="10f8e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10f8e-107">EXAMPLES</span></span>

### <span data-ttu-id="10f8e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10f8e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="10f8e-109">Получите SKU по имени.</span><span class="sxs-lookup"><span data-stu-id="10f8e-109">Get a sku by name.</span></span>

### <span data-ttu-id="10f8e-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="10f8e-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="10f8e-111">Список всех доступных skus сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="10f8e-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="10f8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10f8e-112">PARAMETERS</span></span>

### <span data-ttu-id="10f8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f8e-113">-DefaultProfile</span></span>
<span data-ttu-id="10f8e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10f8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10f8e-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="10f8e-115">-SkuName</span></span>
<span data-ttu-id="10f8e-116">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="10f8e-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f8e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f8e-117">CommonParameters</span></span>
<span data-ttu-id="10f8e-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f8e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f8e-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10f8e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f8e-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10f8e-120">INPUTS</span></span>

### <span data-ttu-id="10f8e-121">Нет</span><span class="sxs-lookup"><span data-stu-id="10f8e-121">None</span></span>

## <span data-ttu-id="10f8e-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10f8e-122">OUTPUTS</span></span>

### <span data-ttu-id="10f8e-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="10f8e-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="10f8e-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10f8e-124">NOTES</span></span>

## <span data-ttu-id="10f8e-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10f8e-125">RELATED LINKS</span></span>

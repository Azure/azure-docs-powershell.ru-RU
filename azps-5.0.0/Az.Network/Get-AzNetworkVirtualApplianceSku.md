---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245980"
---
# <span data-ttu-id="8af03-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="8af03-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="8af03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8af03-102">SYNOPSIS</span></span>
<span data-ttu-id="8af03-103">Получение или перечисление доступных конфигураций сетевого устройства виртуальных устройств на складе.</span><span class="sxs-lookup"><span data-stu-id="8af03-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="8af03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8af03-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8af03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8af03-105">DESCRIPTION</span></span>
<span data-ttu-id="8af03-106">Get-AzNetworkVirtualApplianceSku получает или перечисляет доступные SKU сетевых виртуальных устройств в инвентаризации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8af03-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="8af03-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8af03-107">EXAMPLES</span></span>

### <span data-ttu-id="8af03-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8af03-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="8af03-109">Получение номера SKU по имени.</span><span class="sxs-lookup"><span data-stu-id="8af03-109">Get a sku by name.</span></span>

### <span data-ttu-id="8af03-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8af03-110">Example 2</span></span>
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

<span data-ttu-id="8af03-111">Перечислите все доступные SKU сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="8af03-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="8af03-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8af03-112">PARAMETERS</span></span>

### <span data-ttu-id="8af03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af03-113">-DefaultProfile</span></span>
<span data-ttu-id="8af03-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8af03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af03-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8af03-115">-SkuName</span></span>
<span data-ttu-id="8af03-116">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="8af03-116">The Sku name.</span></span>

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

### <span data-ttu-id="8af03-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af03-117">CommonParameters</span></span>
<span data-ttu-id="8af03-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8af03-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af03-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8af03-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af03-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8af03-120">INPUTS</span></span>

### <span data-ttu-id="8af03-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="8af03-121">None</span></span>

## <span data-ttu-id="8af03-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8af03-122">OUTPUTS</span></span>

### <span data-ttu-id="8af03-123">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="8af03-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="8af03-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="8af03-124">NOTES</span></span>

## <span data-ttu-id="8af03-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8af03-125">RELATED LINKS</span></span>
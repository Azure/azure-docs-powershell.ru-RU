---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: a5febccec0ed09cde866925ce03d7025408b27f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568355"
---
# <span data-ttu-id="309dc-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="309dc-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="309dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="309dc-102">SYNOPSIS</span></span>
<span data-ttu-id="309dc-103">Создает экземпляр PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="309dc-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="309dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="309dc-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="309dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="309dc-105">DESCRIPTION</span></span>
<span data-ttu-id="309dc-106">Вспомогательная команда для создания экземпляра PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="309dc-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="309dc-107">Эта команда используется с New-AzureRmApiManagement командой.</span><span class="sxs-lookup"><span data-stu-id="309dc-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="309dc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="309dc-108">EXAMPLES</span></span>

### <span data-ttu-id="309dc-109">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="309dc-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="309dc-110">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="309dc-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="309dc-111">Создает службу ApiManagement внешних VpnType в регионе "Западная часть США" с дополнительным регионом в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="309dc-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="309dc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="309dc-112">PARAMETERS</span></span>

### <span data-ttu-id="309dc-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="309dc-113">-Capacity</span></span>
<span data-ttu-id="309dc-114">SKU емкость дополнительного региона службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="309dc-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="309dc-115">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="309dc-115">Default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309dc-116">-Location</span><span class="sxs-lookup"><span data-stu-id="309dc-116">-Location</span></span>
<span data-ttu-id="309dc-117">Расположение дополнительной области развертывания.</span><span class="sxs-lookup"><span data-stu-id="309dc-117">Location of the additional deployment region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309dc-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="309dc-118">-VirtualNetwork</span></span>
<span data-ttu-id="309dc-119">Настройка виртуальной сети для области развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="309dc-119">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="309dc-120">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="309dc-120">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="309dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="309dc-121">-DefaultProfile</span></span>
<span data-ttu-id="309dc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="309dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309dc-123">CommonParameters</span></span>
<span data-ttu-id="309dc-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="309dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309dc-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="309dc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309dc-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="309dc-126">INPUTS</span></span>

## <span data-ttu-id="309dc-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="309dc-127">OUTPUTS</span></span>

### <span data-ttu-id="309dc-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="309dc-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="309dc-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="309dc-129">NOTES</span></span>

## <span data-ttu-id="309dc-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="309dc-130">RELATED LINKS</span></span>


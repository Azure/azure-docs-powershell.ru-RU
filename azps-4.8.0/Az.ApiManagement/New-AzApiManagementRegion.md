---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077992"
---
# <span data-ttu-id="388c7-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="388c7-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="388c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="388c7-102">SYNOPSIS</span></span>
<span data-ttu-id="388c7-103">Создает экземпляр PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="388c7-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="388c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="388c7-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="388c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="388c7-105">DESCRIPTION</span></span>
<span data-ttu-id="388c7-106">Вспомогательная команда для создания экземпляра PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="388c7-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="388c7-107">Эта команда используется с New-AzApiManagement командой.</span><span class="sxs-lookup"><span data-stu-id="388c7-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="388c7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="388c7-108">EXAMPLES</span></span>

### <span data-ttu-id="388c7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="388c7-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="388c7-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="388c7-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="388c7-111">Создает службу ApiManagement внешних VpnType в регионе "Западная часть США" с дополнительным регионом в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="388c7-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="388c7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="388c7-112">PARAMETERS</span></span>

### <span data-ttu-id="388c7-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="388c7-113">-Capacity</span></span>
<span data-ttu-id="388c7-114">SKU емкость дополнительного региона службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="388c7-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="388c7-115">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="388c7-115">Default value is 1.</span></span>

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

### <span data-ttu-id="388c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388c7-116">-DefaultProfile</span></span>
<span data-ttu-id="388c7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="388c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="388c7-118">-Location</span><span class="sxs-lookup"><span data-stu-id="388c7-118">-Location</span></span>
<span data-ttu-id="388c7-119">Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="388c7-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="388c7-120">Для получения допустимых местоположений используйте командлет Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="388c7-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="388c7-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="388c7-121">-VirtualNetwork</span></span>
<span data-ttu-id="388c7-122">Настройка виртуальной сети для области развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="388c7-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="388c7-123">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="388c7-123">Default value is $null.</span></span>

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

### <span data-ttu-id="388c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388c7-124">CommonParameters</span></span>
<span data-ttu-id="388c7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="388c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388c7-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="388c7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388c7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="388c7-127">INPUTS</span></span>

### <span data-ttu-id="388c7-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="388c7-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="388c7-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="388c7-129">OUTPUTS</span></span>

### <span data-ttu-id="388c7-130">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="388c7-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="388c7-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="388c7-131">NOTES</span></span>

## <span data-ttu-id="388c7-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="388c7-132">RELATED LINKS</span></span>

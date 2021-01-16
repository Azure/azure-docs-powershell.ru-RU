---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409559"
---
# <span data-ttu-id="c2ebc-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c2ebc-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="c2ebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ebc-103">Создает экземпляр PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="c2ebc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2ebc-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ebc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ebc-106">Команда-помощник для создания экземпляра PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="c2ebc-107">Эта команда будет использоваться с командой New-AzApiManagement команды.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="c2ebc-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2ebc-108">EXAMPLES</span></span>

### <span data-ttu-id="c2ebc-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2ebc-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="c2ebc-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c2ebc-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="c2ebc-111">Создает службу ApiManagement external VpnType в западной части США с дополнительным регионом в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="c2ebc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2ebc-112">PARAMETERS</span></span>

### <span data-ttu-id="c2ebc-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="c2ebc-113">-Capacity</span></span>
<span data-ttu-id="c2ebc-114">SKU дополнительного региона для службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="c2ebc-115">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-115">Default value is 1.</span></span>

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

### <span data-ttu-id="c2ebc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ebc-116">-DefaultProfile</span></span>
<span data-ttu-id="c2ebc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2ebc-118">-Location</span><span class="sxs-lookup"><span data-stu-id="c2ebc-118">-Location</span></span>
<span data-ttu-id="c2ebc-119">Указывает расположение нового региона развертывания из поддерживаемого региона для службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="c2ebc-120">Чтобы получить допустимые расположения, используйте Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | где {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Расположения</span><span class="sxs-lookup"><span data-stu-id="c2ebc-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="c2ebc-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c2ebc-121">-VirtualNetwork</span></span>
<span data-ttu-id="c2ebc-122">Конфигурация виртуальной сети для региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="c2ebc-123">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-123">Default value is $null.</span></span>

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

### <span data-ttu-id="c2ebc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ebc-124">CommonParameters</span></span>
<span data-ttu-id="c2ebc-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ebc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ebc-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2ebc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ebc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2ebc-127">INPUTS</span></span>

### <span data-ttu-id="c2ebc-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c2ebc-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="c2ebc-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2ebc-129">OUTPUTS</span></span>

### <span data-ttu-id="c2ebc-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c2ebc-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="c2ebc-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2ebc-131">NOTES</span></span>

## <span data-ttu-id="c2ebc-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2ebc-132">RELATED LINKS</span></span>
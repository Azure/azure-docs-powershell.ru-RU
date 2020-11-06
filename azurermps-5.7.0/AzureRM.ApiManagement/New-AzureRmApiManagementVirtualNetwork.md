---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570324"
---
# <span data-ttu-id="3ae73-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ae73-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="3ae73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ae73-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae73-103">Создает экземпляр PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="3ae73-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ae73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ae73-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ae73-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae73-106">Командлет **New-AzureRmApiManagementVirtualNetwork** является вспомогательной командой для создания экземпляра **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="3ae73-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="3ae73-107">Эта команда используется с командлетом **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="3ae73-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="3ae73-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ae73-108">EXAMPLES</span></span>

### <span data-ttu-id="3ae73-109">Пример 1: создание виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3ae73-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="3ae73-110">В этом примере создается виртуальная сеть, после чего вызывается командлет **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="3ae73-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="3ae73-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ae73-111">PARAMETERS</span></span>

### <span data-ttu-id="3ae73-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae73-112">-DefaultProfile</span></span>
<span data-ttu-id="3ae73-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae73-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae73-114">-Location</span><span class="sxs-lookup"><span data-stu-id="3ae73-114">-Location</span></span>
<span data-ttu-id="3ae73-115">Задает расположение, в котором находится поддерживаемый регион для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="3ae73-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="3ae73-116">Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="3ae73-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae73-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="3ae73-117">-SubnetResourceId</span></span>
<span data-ttu-id="3ae73-118">Указывает идентификатор ресурса подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3ae73-118">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae73-119">CommonParameters</span></span>
<span data-ttu-id="3ae73-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ae73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae73-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae73-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae73-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ae73-122">INPUTS</span></span>

### <span data-ttu-id="3ae73-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ae73-123">None</span></span>
<span data-ttu-id="3ae73-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3ae73-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ae73-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ae73-125">OUTPUTS</span></span>

### <span data-ttu-id="3ae73-126">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ae73-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="3ae73-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ae73-127">NOTES</span></span>

## <span data-ttu-id="3ae73-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ae73-128">RELATED LINKS</span></span>

[<span data-ttu-id="3ae73-129">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3ae73-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


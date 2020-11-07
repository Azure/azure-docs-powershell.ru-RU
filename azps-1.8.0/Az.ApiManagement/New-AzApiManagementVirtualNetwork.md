---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901702"
---
# <span data-ttu-id="5dadf-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5dadf-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5dadf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dadf-102">SYNOPSIS</span></span>
<span data-ttu-id="5dadf-103">Создает экземпляр PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="5dadf-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="5dadf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dadf-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dadf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dadf-105">DESCRIPTION</span></span>
<span data-ttu-id="5dadf-106">Командлет **New-AzApiManagementVirtualNetwork** является вспомогательной командой для создания экземпляра **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="5dadf-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="5dadf-107">Эта команда используется с командлетом **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="5dadf-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="5dadf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dadf-108">EXAMPLES</span></span>

### <span data-ttu-id="5dadf-109">Пример 1: создание виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="5dadf-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="5dadf-110">В этом примере создается виртуальная сеть, после чего вызывается командлет **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="5dadf-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="5dadf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dadf-111">PARAMETERS</span></span>

### <span data-ttu-id="5dadf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dadf-112">-DefaultProfile</span></span>
<span data-ttu-id="5dadf-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dadf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dadf-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="5dadf-114">-SubnetResourceId</span></span>
<span data-ttu-id="5dadf-115">Указывает идентификатор ресурса подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5dadf-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="5dadf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dadf-116">CommonParameters</span></span>
<span data-ttu-id="5dadf-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dadf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dadf-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dadf-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dadf-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dadf-119">INPUTS</span></span>

### <span data-ttu-id="5dadf-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="5dadf-120">None</span></span>

## <span data-ttu-id="5dadf-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dadf-121">OUTPUTS</span></span>

### <span data-ttu-id="5dadf-122">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5dadf-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5dadf-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dadf-123">NOTES</span></span>

## <span data-ttu-id="5dadf-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dadf-124">RELATED LINKS</span></span>

[<span data-ttu-id="5dadf-125">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5dadf-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)


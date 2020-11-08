---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249734"
---
# <span data-ttu-id="a52c8-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a52c8-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a52c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a52c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a52c8-103">Создает экземпляр PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a52c8-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="a52c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a52c8-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a52c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a52c8-105">DESCRIPTION</span></span>
<span data-ttu-id="a52c8-106">Командлет **New-AzApiManagementVirtualNetwork** является вспомогательной командой для создания экземпляра **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="a52c8-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="a52c8-107">Эта команда используется с командлетом **Set-AzApiManagement** и **New-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="a52c8-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="a52c8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a52c8-108">EXAMPLES</span></span>

### <span data-ttu-id="a52c8-109">Пример 1: создание виртуальной сети и обновление существующей службы APIM в VNET</span><span class="sxs-lookup"><span data-stu-id="a52c8-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="a52c8-110">В этом примере создается виртуальная сеть и затем вызывается командлет **Set-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="a52c8-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="a52c8-111">Пример 2: создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a52c8-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="a52c8-112">В этом примере создается новая служба APIM в виртуальной сети в `External` режиме</span><span class="sxs-lookup"><span data-stu-id="a52c8-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="a52c8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a52c8-113">PARAMETERS</span></span>

### <span data-ttu-id="a52c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52c8-114">-DefaultProfile</span></span>
<span data-ttu-id="a52c8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a52c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a52c8-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="a52c8-116">-SubnetResourceId</span></span>
<span data-ttu-id="a52c8-117">Указывает идентификатор ресурса подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a52c8-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="a52c8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52c8-118">CommonParameters</span></span>
<span data-ttu-id="a52c8-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a52c8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52c8-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a52c8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52c8-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a52c8-121">INPUTS</span></span>

### <span data-ttu-id="a52c8-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="a52c8-122">None</span></span>

## <span data-ttu-id="a52c8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a52c8-123">OUTPUTS</span></span>

### <span data-ttu-id="a52c8-124">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a52c8-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a52c8-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a52c8-125">NOTES</span></span>

## <span data-ttu-id="a52c8-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a52c8-126">RELATED LINKS</span></span>

<span data-ttu-id="a52c8-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="a52c8-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>


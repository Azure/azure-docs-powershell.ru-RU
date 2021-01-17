---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423516"
---
# <span data-ttu-id="0d433-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d433-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="0d433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d433-102">SYNOPSIS</span></span>
<span data-ttu-id="0d433-103">Создает экземпляр PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="0d433-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="0d433-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d433-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d433-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d433-105">DESCRIPTION</span></span>
<span data-ttu-id="0d433-106">Командлет **New-AzApiManagementVirtualNetwork** является командлетом-помощником для создания экземпляра **PsApiManagementVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="0d433-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="0d433-107">Эта команда используется с **командлетами Set-AzApiManagement** и **New-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="0d433-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="0d433-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d433-108">EXAMPLES</span></span>

### <span data-ttu-id="0d433-109">Пример 1. Создание виртуальной сети и обновление существующей службы APIM в VNET</span><span class="sxs-lookup"><span data-stu-id="0d433-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="0d433-110">В этом примере создается виртуальная сеть, а затем вызывается **cmdlet Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="0d433-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="0d433-111">Пример 2. Создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="0d433-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="0d433-112">В этом примере новая служба APIM создается в режиме виртуальной `External` сети.</span><span class="sxs-lookup"><span data-stu-id="0d433-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="0d433-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d433-113">PARAMETERS</span></span>

### <span data-ttu-id="0d433-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d433-114">-DefaultProfile</span></span>
<span data-ttu-id="0d433-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d433-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d433-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="0d433-116">-SubnetResourceId</span></span>
<span data-ttu-id="0d433-117">Определяет ИД ресурса подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d433-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="0d433-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d433-118">CommonParameters</span></span>
<span data-ttu-id="0d433-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d433-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d433-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d433-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d433-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d433-121">INPUTS</span></span>

### <span data-ttu-id="0d433-122">Нет</span><span class="sxs-lookup"><span data-stu-id="0d433-122">None</span></span>

## <span data-ttu-id="0d433-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d433-123">OUTPUTS</span></span>

### <span data-ttu-id="0d433-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d433-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="0d433-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d433-125">NOTES</span></span>

## <span data-ttu-id="0d433-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d433-126">RELATED LINKS</span></span>

<span data-ttu-id="0d433-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="0d433-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>


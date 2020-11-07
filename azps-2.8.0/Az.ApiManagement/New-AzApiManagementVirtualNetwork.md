---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 8833d6380c14c3b2e9b9c53657602f9f3cbfd1af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728014"
---
# <span data-ttu-id="dc0a2-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dc0a2-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="dc0a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0a2-103">Создает экземпляр PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="dc0a2-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="dc0a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc0a2-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc0a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc0a2-105">DESCRIPTION</span></span>
<span data-ttu-id="dc0a2-106">Командлет **New-AzApiManagementVirtualNetwork** является вспомогательной командой для создания экземпляра **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="dc0a2-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="dc0a2-107">Эта команда используется с командлетом **Set-AzApiManagement** и **New-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="dc0a2-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="dc0a2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc0a2-108">EXAMPLES</span></span>

### <span data-ttu-id="dc0a2-109">Пример 1: создание виртуальной сети и обновление существующей службы APIM в VNET</span><span class="sxs-lookup"><span data-stu-id="dc0a2-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="dc0a2-110">В этом примере создается виртуальная сеть и затем вызывается командлет **Set-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="dc0a2-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="dc0a2-111">Пример 2: создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="dc0a2-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="dc0a2-112">В этом примере создается новая служба APIM в виртуальной сети в `External` режиме</span><span class="sxs-lookup"><span data-stu-id="dc0a2-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="dc0a2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc0a2-113">PARAMETERS</span></span>

### <span data-ttu-id="dc0a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0a2-114">-DefaultProfile</span></span>
<span data-ttu-id="dc0a2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0a2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc0a2-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="dc0a2-116">-SubnetResourceId</span></span>
<span data-ttu-id="dc0a2-117">Указывает идентификатор ресурса подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dc0a2-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="dc0a2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0a2-118">CommonParameters</span></span>
<span data-ttu-id="dc0a2-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc0a2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0a2-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc0a2-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0a2-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc0a2-121">INPUTS</span></span>

### <span data-ttu-id="dc0a2-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="dc0a2-122">None</span></span>

## <span data-ttu-id="dc0a2-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc0a2-123">OUTPUTS</span></span>

### <span data-ttu-id="dc0a2-124">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dc0a2-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="dc0a2-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc0a2-125">NOTES</span></span>

## <span data-ttu-id="dc0a2-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc0a2-126">RELATED LINKS</span></span>

<span data-ttu-id="dc0a2-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="dc0a2-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>


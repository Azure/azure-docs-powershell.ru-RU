---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734939"
---
# <span data-ttu-id="a5ee5-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a5ee5-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="a5ee5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ee5-103">Получает Azure VirtualHub по имени и ResourceGroupName или отображает список всех виртуальных концентраторов по ResourceGroupName и подписке.</span><span class="sxs-lookup"><span data-stu-id="a5ee5-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5ee5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5ee5-104">SYNTAX</span></span>

### <span data-ttu-id="a5ee5-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5ee5-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5ee5-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ee5-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5ee5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5ee5-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ee5-108">Получает Azure VirtualHub по имени и ResourceGroupName или отображает список всех виртуальных концентраторов по ResourceGroupName и подписке.</span><span class="sxs-lookup"><span data-stu-id="a5ee5-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="a5ee5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5ee5-109">EXAMPLES</span></span>

### <span data-ttu-id="a5ee5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5ee5-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a5ee5-111">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="a5ee5-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a5ee5-112">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a5ee5-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="a5ee5-113">Затем он получает виртуальный концентратор, используя его ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a5ee5-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="a5ee5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5ee5-114">PARAMETERS</span></span>

### <span data-ttu-id="a5ee5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ee5-115">-DefaultProfile</span></span>
<span data-ttu-id="a5ee5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ee5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ee5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5ee5-117">-Name</span></span>
<span data-ttu-id="a5ee5-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a5ee5-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ee5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ee5-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5ee5-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5ee5-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ee5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ee5-121">CommonParameters</span></span>
<span data-ttu-id="a5ee5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5ee5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ee5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ee5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ee5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5ee5-124">INPUTS</span></span>

### <span data-ttu-id="a5ee5-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="a5ee5-125">None</span></span>

## <span data-ttu-id="a5ee5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5ee5-126">OUTPUTS</span></span>

### <span data-ttu-id="a5ee5-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a5ee5-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a5ee5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5ee5-128">NOTES</span></span>

## <span data-ttu-id="a5ee5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5ee5-129">RELATED LINKS</span></span>

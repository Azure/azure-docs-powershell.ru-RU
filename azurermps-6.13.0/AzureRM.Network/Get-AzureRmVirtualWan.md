---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562939"
---
# <span data-ttu-id="5d965-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="5d965-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="5d965-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d965-102">SYNOPSIS</span></span>
<span data-ttu-id="5d965-103">Возвращает виртуальную глобальную сеть или все виртуальные глобальные ресурсы в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="5d965-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d965-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d965-104">SYNTAX</span></span>

### <span data-ttu-id="5d965-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d965-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d965-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d965-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d965-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d965-107">DESCRIPTION</span></span>
<span data-ttu-id="5d965-108">Возвращает виртуальную глобальную сеть или все виртуальные глобальные ресурсы в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="5d965-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="5d965-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d965-109">EXAMPLES</span></span>

### <span data-ttu-id="5d965-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d965-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="5d965-111">Эта команда получает виртуальную глобальную сеть с именем myVirtualWAN в группе ресурсов testRG.</span><span class="sxs-lookup"><span data-stu-id="5d965-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="5d965-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d965-112">PARAMETERS</span></span>

### <span data-ttu-id="5d965-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d965-113">-DefaultProfile</span></span>
<span data-ttu-id="5d965-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d965-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d965-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d965-115">-Name</span></span>
<span data-ttu-id="5d965-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d965-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d965-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d965-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d965-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d965-118">The resource group name.</span></span>

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

### <span data-ttu-id="5d965-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d965-119">CommonParameters</span></span>
<span data-ttu-id="5d965-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d965-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d965-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d965-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d965-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d965-122">INPUTS</span></span>

### <span data-ttu-id="5d965-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="5d965-123">None</span></span>

## <span data-ttu-id="5d965-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d965-124">OUTPUTS</span></span>

### <span data-ttu-id="5d965-125">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="5d965-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="5d965-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d965-126">NOTES</span></span>

## <span data-ttu-id="5d965-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d965-127">RELATED LINKS</span></span>

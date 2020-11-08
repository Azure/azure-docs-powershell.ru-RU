---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246900"
---
# <span data-ttu-id="1fef4-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1fef4-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="1fef4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fef4-102">SYNOPSIS</span></span>
<span data-ttu-id="1fef4-103">Возвращает виртуальную глобальную сеть или все виртуальные глобальные ресурсы в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="1fef4-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="1fef4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fef4-104">SYNTAX</span></span>

### <span data-ttu-id="1fef4-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fef4-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fef4-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fef4-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fef4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fef4-107">DESCRIPTION</span></span>
<span data-ttu-id="1fef4-108">Возвращает виртуальную глобальную сеть или все виртуальные глобальные ресурсы в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="1fef4-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="1fef4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fef4-109">EXAMPLES</span></span>

### <span data-ttu-id="1fef4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fef4-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="1fef4-111">Эта команда получает виртуальную глобальную сеть с именем myVirtualWAN в группе ресурсов testRG.</span><span class="sxs-lookup"><span data-stu-id="1fef4-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="1fef4-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1fef4-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="1fef4-113">Эта команда получает все виртуальные глобальные сети, начинающиеся с "тест".</span><span class="sxs-lookup"><span data-stu-id="1fef4-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="1fef4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fef4-114">PARAMETERS</span></span>

### <span data-ttu-id="1fef4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fef4-115">-DefaultProfile</span></span>
<span data-ttu-id="1fef4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fef4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fef4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fef4-117">-Name</span></span>
<span data-ttu-id="1fef4-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1fef4-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1fef4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fef4-119">-ResourceGroupName</span></span>
<span data-ttu-id="1fef4-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fef4-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1fef4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fef4-121">CommonParameters</span></span>
<span data-ttu-id="1fef4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fef4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fef4-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fef4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fef4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fef4-124">INPUTS</span></span>

### <span data-ttu-id="1fef4-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="1fef4-125">None</span></span>

## <span data-ttu-id="1fef4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fef4-126">OUTPUTS</span></span>

### <span data-ttu-id="1fef4-127">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1fef4-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="1fef4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fef4-128">NOTES</span></span>

## <span data-ttu-id="1fef4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fef4-129">RELATED LINKS</span></span>

[<span data-ttu-id="1fef4-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1fef4-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="1fef4-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1fef4-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="1fef4-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1fef4-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)

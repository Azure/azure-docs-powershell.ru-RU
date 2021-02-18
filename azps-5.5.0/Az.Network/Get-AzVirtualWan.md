---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218649"
---
# <span data-ttu-id="88bc4-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="88bc4-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="88bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="88bc4-103">Возвращает виртуальнуюwan или все виртуальные waNs в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="88bc4-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="88bc4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88bc4-104">SYNTAX</span></span>

### <span data-ttu-id="88bc4-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88bc4-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88bc4-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88bc4-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88bc4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="88bc4-108">Возвращает виртуальнуюwan или все виртуальные waNs в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="88bc4-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="88bc4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="88bc4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88bc4-110">Example 1</span></span>

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

<span data-ttu-id="88bc4-111">Эта команда получает виртуальную WAN с именем myVirtualWAN в testRG группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88bc4-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="88bc4-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88bc4-112">Example 2</span></span>

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

<span data-ttu-id="88bc4-113">Эта команда получает все виртуальные WANs, начиная с "test".</span><span class="sxs-lookup"><span data-stu-id="88bc4-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="88bc4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88bc4-114">PARAMETERS</span></span>

### <span data-ttu-id="88bc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bc4-115">-DefaultProfile</span></span>
<span data-ttu-id="88bc4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88bc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88bc4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="88bc4-117">-Name</span></span>
<span data-ttu-id="88bc4-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="88bc4-118">The resource name.</span></span>

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

### <span data-ttu-id="88bc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88bc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="88bc4-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88bc4-120">The resource group name.</span></span>

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

### <span data-ttu-id="88bc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bc4-121">CommonParameters</span></span>
<span data-ttu-id="88bc4-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88bc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bc4-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88bc4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bc4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88bc4-124">INPUTS</span></span>

### <span data-ttu-id="88bc4-125">Нет</span><span class="sxs-lookup"><span data-stu-id="88bc4-125">None</span></span>

## <span data-ttu-id="88bc4-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88bc4-126">OUTPUTS</span></span>

### <span data-ttu-id="88bc4-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="88bc4-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="88bc4-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88bc4-128">NOTES</span></span>

## <span data-ttu-id="88bc4-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88bc4-129">RELATED LINKS</span></span>

[<span data-ttu-id="88bc4-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="88bc4-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="88bc4-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="88bc4-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="88bc4-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="88bc4-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)

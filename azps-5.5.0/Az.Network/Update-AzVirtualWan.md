---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240509"
---
# <span data-ttu-id="a7fc4-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a7fc4-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="a7fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="a7fc4-103">Обновляет виртуальную WAN Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="a7fc4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7fc4-104">SYNTAX</span></span>

### <span data-ttu-id="a7fc4-105">ByVirtualWanName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7fc4-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7fc4-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a7fc4-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7fc4-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="a7fc4-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7fc4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7fc4-108">DESCRIPTION</span></span>
<span data-ttu-id="a7fc4-109">Обновляет виртуальную WAN Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="a7fc4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7fc4-110">EXAMPLES</span></span>

### <span data-ttu-id="a7fc4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7fc4-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="a7fc4-112">Выше будет создаваться группа ресурсов testRG в регионе "Западная США" и виртуальная WAN Azure в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="a7fc4-113">VirtualWan обновляется с помощью новых свойств.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="a7fc4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7fc4-114">PARAMETERS</span></span>

### <span data-ttu-id="a7fc4-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="a7fc4-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="a7fc4-116">Разрешить ветвь-трафик для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="a7fc4-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="a7fc4-118">Разрешить VNET-трафик vnet для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7fc4-119">-AsJob</span></span>
<span data-ttu-id="a7fc4-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a7fc4-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7fc4-121">-DefaultProfile</span></span>
<span data-ttu-id="a7fc4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a7fc4-123">-Force</span></span>
<span data-ttu-id="a7fc4-124">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="a7fc4-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7fc4-125">-InputObject</span></span>
<span data-ttu-id="a7fc4-126">Объект виртуальной wan, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="a7fc4-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a7fc4-127">-Name</span></span>
<span data-ttu-id="a7fc4-128">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7fc4-129">-ResourceGroupName</span></span>
<span data-ttu-id="a7fc4-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7fc4-131">-ResourceId</span></span>
<span data-ttu-id="a7fc4-132">ИД ресурсов Azure для виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7fc4-133">-Tag</span></span>
<span data-ttu-id="a7fc4-134">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a7fc4-135">-VirtualWANType</span></span>
<span data-ttu-id="a7fc4-136">Тип виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7fc4-137">-Confirm</span></span>
<span data-ttu-id="a7fc4-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7fc4-139">-WhatIf</span></span>
<span data-ttu-id="a7fc4-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7fc4-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7fc4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7fc4-142">CommonParameters</span></span>
<span data-ttu-id="a7fc4-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7fc4-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7fc4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7fc4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7fc4-145">INPUTS</span></span>

### <span data-ttu-id="a7fc4-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a7fc4-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="a7fc4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a7fc4-147">System.String</span></span>

## <span data-ttu-id="a7fc4-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7fc4-148">OUTPUTS</span></span>

### <span data-ttu-id="a7fc4-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a7fc4-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="a7fc4-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7fc4-150">NOTES</span></span>

## <span data-ttu-id="a7fc4-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7fc4-151">RELATED LINKS</span></span>

[<span data-ttu-id="a7fc4-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a7fc4-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="a7fc4-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a7fc4-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="a7fc4-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a7fc4-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

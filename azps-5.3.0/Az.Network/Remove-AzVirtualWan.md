---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425180"
---
# <span data-ttu-id="e5639-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5639-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="e5639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5639-102">SYNOPSIS</span></span>
<span data-ttu-id="e5639-103">Удаляет виртуальнуюwan-wan Azure.</span><span class="sxs-lookup"><span data-stu-id="e5639-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e5639-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5639-104">SYNTAX</span></span>

### <span data-ttu-id="e5639-105">ByVirtualWanName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5639-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5639-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="e5639-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5639-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="e5639-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5639-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5639-108">DESCRIPTION</span></span>
<span data-ttu-id="e5639-109">Удаляет виртуальнуюwan-wan Azure.</span><span class="sxs-lookup"><span data-stu-id="e5639-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e5639-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5639-110">EXAMPLES</span></span>

### <span data-ttu-id="e5639-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5639-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="e5639-112">В этом примере создается виртуальнаяwan в группе ресурсов, а затем сразу удаляется.</span><span class="sxs-lookup"><span data-stu-id="e5639-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e5639-113">Чтобы скрыть запрос при удалении виртуальной WAN, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="e5639-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="e5639-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5639-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="e5639-115">В этом примере создается виртуальнаяwan в группе ресурсов, а затем сразу удаляется.</span><span class="sxs-lookup"><span data-stu-id="e5639-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e5639-116">Это удаление происходит с использованием объекта виртуальной wan, возвращаемого New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e5639-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="e5639-117">Чтобы скрыть запрос при удалении виртуальной WAN, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="e5639-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="e5639-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e5639-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="e5639-119">В этом примере создается виртуальнаяwan в группе ресурсов, а затем сразу удаляется.</span><span class="sxs-lookup"><span data-stu-id="e5639-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e5639-120">Это удаление происходит с помощью ид ресурса виртуальной wan, возвращаемого New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e5639-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="e5639-121">Чтобы скрыть запрос при удалении виртуальной WAN, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="e5639-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="e5639-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5639-122">PARAMETERS</span></span>

### <span data-ttu-id="e5639-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5639-123">-DefaultProfile</span></span>
<span data-ttu-id="e5639-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5639-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5639-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e5639-125">-Force</span></span>
<span data-ttu-id="e5639-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e5639-126">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5639-127">-InputObject</span></span>
<span data-ttu-id="e5639-128">Удаляемый объект виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="e5639-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e5639-129">-Name</span></span>
<span data-ttu-id="e5639-130">Виртуальное имя wan.</span><span class="sxs-lookup"><span data-stu-id="e5639-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5639-131">-PassThru</span></span>
<span data-ttu-id="e5639-132">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e5639-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5639-133">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e5639-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5639-134">-ResourceGroupName</span></span>
<span data-ttu-id="e5639-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5639-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5639-136">-ResourceId</span></span>
<span data-ttu-id="e5639-137">Удаляемый ИД ресурсов Azure для виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="e5639-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5639-138">-Confirm</span></span>
<span data-ttu-id="e5639-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5639-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5639-140">-WhatIf</span></span>
<span data-ttu-id="e5639-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5639-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5639-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e5639-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5639-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5639-143">CommonParameters</span></span>
<span data-ttu-id="e5639-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5639-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5639-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5639-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5639-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5639-146">INPUTS</span></span>

### <span data-ttu-id="e5639-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5639-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="e5639-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e5639-148">System.String</span></span>

## <span data-ttu-id="e5639-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5639-149">OUTPUTS</span></span>

### <span data-ttu-id="e5639-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5639-150">System.Boolean</span></span>

## <span data-ttu-id="e5639-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5639-151">NOTES</span></span>

## <span data-ttu-id="e5639-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5639-152">RELATED LINKS</span></span>

[<span data-ttu-id="e5639-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5639-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="e5639-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5639-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="e5639-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5639-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)

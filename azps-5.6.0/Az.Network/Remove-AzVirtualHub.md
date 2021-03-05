---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 7a5724346f1b94af0dbc07df16f9cdab5f798523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006115"
---
# <span data-ttu-id="06e98-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="06e98-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="06e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e98-102">SYNOPSIS</span></span>
<span data-ttu-id="06e98-103">Удаляет ресурс Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="06e98-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="06e98-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06e98-104">SYNTAX</span></span>

### <span data-ttu-id="06e98-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06e98-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e98-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="06e98-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e98-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="06e98-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e98-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06e98-108">DESCRIPTION</span></span>
<span data-ttu-id="06e98-109">Удаляет ресурс Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="06e98-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="06e98-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06e98-110">EXAMPLES</span></span>

### <span data-ttu-id="06e98-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06e98-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="06e98-112">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="06e98-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="06e98-113">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="06e98-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="06e98-114">Затем он удаляет виртуальный концентратор с помощью его resourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="06e98-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="06e98-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="06e98-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="06e98-116">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="06e98-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="06e98-117">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="06e98-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="06e98-118">Затем он удаляет виртуальный концентратор с помощью входного объекта.</span><span class="sxs-lookup"><span data-stu-id="06e98-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="06e98-119">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="06e98-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="06e98-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="06e98-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="06e98-121">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="06e98-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="06e98-122">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="06e98-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="06e98-123">Затем он удаляет виртуальный концентратор с помощью piping powershell, используя выходные данные из Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="06e98-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="06e98-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06e98-124">PARAMETERS</span></span>

### <span data-ttu-id="06e98-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06e98-125">-AsJob</span></span>
<span data-ttu-id="06e98-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="06e98-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06e98-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e98-127">-DefaultProfile</span></span>
<span data-ttu-id="06e98-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06e98-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e98-129">-Force</span><span class="sxs-lookup"><span data-stu-id="06e98-129">-Force</span></span>
<span data-ttu-id="06e98-130">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="06e98-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="06e98-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06e98-131">-InputObject</span></span>
<span data-ttu-id="06e98-132">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="06e98-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06e98-133">-Name</span><span class="sxs-lookup"><span data-stu-id="06e98-133">-Name</span></span>
<span data-ttu-id="06e98-134">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="06e98-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e98-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06e98-135">-PassThru</span></span>
<span data-ttu-id="06e98-136">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="06e98-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06e98-137">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="06e98-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06e98-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e98-138">-ResourceGroupName</span></span>
<span data-ttu-id="06e98-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06e98-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e98-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e98-140">-ResourceId</span></span>
<span data-ttu-id="06e98-141">ИД ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="06e98-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e98-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06e98-142">-Confirm</span></span>
<span data-ttu-id="06e98-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e98-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e98-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e98-144">-WhatIf</span></span>
<span data-ttu-id="06e98-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e98-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e98-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="06e98-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e98-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e98-147">CommonParameters</span></span>
<span data-ttu-id="06e98-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e98-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e98-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e98-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e98-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06e98-150">INPUTS</span></span>

### <span data-ttu-id="06e98-151">System.String</span><span class="sxs-lookup"><span data-stu-id="06e98-151">System.String</span></span>

### <span data-ttu-id="06e98-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="06e98-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="06e98-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06e98-153">OUTPUTS</span></span>

### <span data-ttu-id="06e98-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06e98-154">System.Boolean</span></span>

## <span data-ttu-id="06e98-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06e98-155">NOTES</span></span>

## <span data-ttu-id="06e98-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06e98-156">RELATED LINKS</span></span>

[<span data-ttu-id="06e98-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="06e98-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="06e98-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="06e98-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="06e98-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="06e98-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

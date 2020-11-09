---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248100"
---
# <span data-ttu-id="07f8e-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="07f8e-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="07f8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="07f8e-103">Удаление ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="07f8e-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="07f8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07f8e-104">SYNTAX</span></span>

### <span data-ttu-id="07f8e-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07f8e-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f8e-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="07f8e-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f8e-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="07f8e-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f8e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07f8e-108">DESCRIPTION</span></span>
<span data-ttu-id="07f8e-109">Удаление ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="07f8e-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="07f8e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07f8e-110">EXAMPLES</span></span>

### <span data-ttu-id="07f8e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07f8e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="07f8e-112">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="07f8e-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="07f8e-113">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="07f8e-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="07f8e-114">Затем виртуальный концентратор будет удален с использованием его ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="07f8e-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="07f8e-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="07f8e-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="07f8e-116">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="07f8e-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="07f8e-117">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="07f8e-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="07f8e-118">Затем виртуальный концентратор удаляется с помощью объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="07f8e-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="07f8e-119">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="07f8e-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="07f8e-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="07f8e-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="07f8e-121">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="07f8e-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="07f8e-122">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="07f8e-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="07f8e-123">Затем виртуальный концентратор удаляется с помощью конвейера PowerShell с помощью выходных данных Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="07f8e-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="07f8e-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07f8e-124">PARAMETERS</span></span>

### <span data-ttu-id="07f8e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07f8e-125">-AsJob</span></span>
<span data-ttu-id="07f8e-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="07f8e-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07f8e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f8e-127">-DefaultProfile</span></span>
<span data-ttu-id="07f8e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07f8e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f8e-129">-Force</span><span class="sxs-lookup"><span data-stu-id="07f8e-129">-Force</span></span>
<span data-ttu-id="07f8e-130">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="07f8e-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="07f8e-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07f8e-131">-InputObject</span></span>
<span data-ttu-id="07f8e-132">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="07f8e-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="07f8e-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07f8e-133">-Name</span></span>
<span data-ttu-id="07f8e-134">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="07f8e-134">The resource name.</span></span>

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

### <span data-ttu-id="07f8e-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07f8e-135">-PassThru</span></span>
<span data-ttu-id="07f8e-136">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="07f8e-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="07f8e-137">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="07f8e-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="07f8e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f8e-138">-ResourceGroupName</span></span>
<span data-ttu-id="07f8e-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07f8e-139">The resource group name.</span></span>

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

### <span data-ttu-id="07f8e-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f8e-140">-ResourceId</span></span>
<span data-ttu-id="07f8e-141">Идентификатор ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="07f8e-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="07f8e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07f8e-142">-Confirm</span></span>
<span data-ttu-id="07f8e-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="07f8e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f8e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f8e-144">-WhatIf</span></span>
<span data-ttu-id="07f8e-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="07f8e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f8e-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="07f8e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f8e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f8e-147">CommonParameters</span></span>
<span data-ttu-id="07f8e-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07f8e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f8e-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f8e-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f8e-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07f8e-150">INPUTS</span></span>

### <span data-ttu-id="07f8e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="07f8e-151">System.String</span></span>

### <span data-ttu-id="07f8e-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="07f8e-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="07f8e-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07f8e-153">OUTPUTS</span></span>

### <span data-ttu-id="07f8e-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07f8e-154">System.Boolean</span></span>

## <span data-ttu-id="07f8e-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="07f8e-155">NOTES</span></span>

## <span data-ttu-id="07f8e-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07f8e-156">RELATED LINKS</span></span>

[<span data-ttu-id="07f8e-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="07f8e-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="07f8e-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="07f8e-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="07f8e-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="07f8e-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
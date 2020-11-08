---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078876"
---
# <span data-ttu-id="14a2f-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="14a2f-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="14a2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="14a2f-103">Удаление ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="14a2f-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="14a2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14a2f-104">SYNTAX</span></span>

### <span data-ttu-id="14a2f-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14a2f-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a2f-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="14a2f-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a2f-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="14a2f-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a2f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14a2f-108">DESCRIPTION</span></span>
<span data-ttu-id="14a2f-109">Удаление ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="14a2f-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="14a2f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14a2f-110">EXAMPLES</span></span>

### <span data-ttu-id="14a2f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14a2f-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="14a2f-112">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="14a2f-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="14a2f-113">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="14a2f-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="14a2f-114">Затем виртуальный концентратор будет удален с использованием его ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="14a2f-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="14a2f-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="14a2f-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="14a2f-116">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="14a2f-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="14a2f-117">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="14a2f-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="14a2f-118">Затем виртуальный концентратор удаляется с помощью объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="14a2f-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="14a2f-119">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="14a2f-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="14a2f-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="14a2f-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="14a2f-121">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="14a2f-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="14a2f-122">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="14a2f-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="14a2f-123">Затем виртуальный концентратор удаляется с помощью конвейера PowerShell с помощью выходных данных Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="14a2f-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="14a2f-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14a2f-124">PARAMETERS</span></span>

### <span data-ttu-id="14a2f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14a2f-125">-AsJob</span></span>
<span data-ttu-id="14a2f-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14a2f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14a2f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a2f-127">-DefaultProfile</span></span>
<span data-ttu-id="14a2f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14a2f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a2f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="14a2f-129">-Force</span></span>
<span data-ttu-id="14a2f-130">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="14a2f-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="14a2f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a2f-131">-InputObject</span></span>
<span data-ttu-id="14a2f-132">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="14a2f-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="14a2f-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14a2f-133">-Name</span></span>
<span data-ttu-id="14a2f-134">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="14a2f-134">The resource name.</span></span>

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

### <span data-ttu-id="14a2f-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14a2f-135">-PassThru</span></span>
<span data-ttu-id="14a2f-136">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="14a2f-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="14a2f-137">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="14a2f-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14a2f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a2f-138">-ResourceGroupName</span></span>
<span data-ttu-id="14a2f-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14a2f-139">The resource group name.</span></span>

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

### <span data-ttu-id="14a2f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a2f-140">-ResourceId</span></span>
<span data-ttu-id="14a2f-141">Идентификатор ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="14a2f-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="14a2f-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14a2f-142">-Confirm</span></span>
<span data-ttu-id="14a2f-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14a2f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a2f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a2f-144">-WhatIf</span></span>
<span data-ttu-id="14a2f-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14a2f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a2f-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14a2f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a2f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a2f-147">CommonParameters</span></span>
<span data-ttu-id="14a2f-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14a2f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a2f-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a2f-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a2f-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14a2f-150">INPUTS</span></span>

### <span data-ttu-id="14a2f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="14a2f-151">System.String</span></span>

### <span data-ttu-id="14a2f-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="14a2f-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="14a2f-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14a2f-153">OUTPUTS</span></span>

### <span data-ttu-id="14a2f-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14a2f-154">System.Boolean</span></span>

## <span data-ttu-id="14a2f-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="14a2f-155">NOTES</span></span>

## <span data-ttu-id="14a2f-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14a2f-156">RELATED LINKS</span></span>

[<span data-ttu-id="14a2f-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="14a2f-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="14a2f-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="14a2f-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="14a2f-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="14a2f-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

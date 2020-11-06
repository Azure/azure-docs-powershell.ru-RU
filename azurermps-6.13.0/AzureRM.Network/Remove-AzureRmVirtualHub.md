---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
ms.openlocfilehash: 65d319749424697c882012d23bf12f87f92adbc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568454"
---
# <span data-ttu-id="c7df9-101">Remove-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c7df9-101">Remove-AzureRmVirtualHub</span></span>

## <span data-ttu-id="c7df9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7df9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7df9-103">Удаление ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c7df9-103">Removes an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7df9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7df9-104">SYNTAX</span></span>

### <span data-ttu-id="c7df9-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7df9-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7df9-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c7df9-106">ByVirtualHubResourceId</span></span>
```
Remove-AzureRmVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7df9-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c7df9-107">ByVirtualHubObject</span></span>
```
Remove-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7df9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7df9-108">DESCRIPTION</span></span>
<span data-ttu-id="c7df9-109">Удаление ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c7df9-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="c7df9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7df9-110">EXAMPLES</span></span>

### <span data-ttu-id="c7df9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7df9-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="c7df9-112">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="c7df9-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c7df9-113">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c7df9-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c7df9-114">Затем виртуальный концентратор будет удален с использованием его ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="c7df9-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="c7df9-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c7df9-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="c7df9-116">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="c7df9-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c7df9-117">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c7df9-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c7df9-118">Затем виртуальный концентратор удаляется с помощью объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="c7df9-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="c7df9-119">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c7df9-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="c7df9-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c7df9-120">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzureRmVirtualHub
```

<span data-ttu-id="c7df9-121">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="c7df9-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c7df9-122">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c7df9-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c7df9-123">Затем виртуальный концентратор удаляется с помощью конвейера PowerShell с помощью выходных данных Get-AzureRmVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c7df9-123">It then deletes the virtual hub using powershell piping using output from Get-AzureRmVirtualHub.</span></span>

## <span data-ttu-id="c7df9-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7df9-124">PARAMETERS</span></span>

### <span data-ttu-id="c7df9-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7df9-125">-AsJob</span></span>
<span data-ttu-id="c7df9-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c7df9-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7df9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7df9-127">-DefaultProfile</span></span>
<span data-ttu-id="c7df9-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7df9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7df9-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c7df9-129">-Force</span></span>
<span data-ttu-id="c7df9-130">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="c7df9-130">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c7df9-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7df9-131">-InputObject</span></span>
<span data-ttu-id="c7df9-132">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c7df9-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="c7df9-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7df9-133">-Name</span></span>
<span data-ttu-id="c7df9-134">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c7df9-134">The resource name.</span></span>

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

### <span data-ttu-id="c7df9-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7df9-135">-PassThru</span></span>
<span data-ttu-id="c7df9-136">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c7df9-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c7df9-137">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c7df9-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c7df9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7df9-138">-ResourceGroupName</span></span>
<span data-ttu-id="c7df9-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7df9-139">The resource group name.</span></span>

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

### <span data-ttu-id="c7df9-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7df9-140">-ResourceId</span></span>
<span data-ttu-id="c7df9-141">Идентификатор ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c7df9-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="c7df9-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7df9-142">-Confirm</span></span>
<span data-ttu-id="c7df9-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7df9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7df9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7df9-144">-WhatIf</span></span>
<span data-ttu-id="c7df9-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7df9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7df9-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7df9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7df9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7df9-147">CommonParameters</span></span>
<span data-ttu-id="c7df9-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7df9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7df9-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7df9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7df9-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7df9-150">INPUTS</span></span>

### <span data-ttu-id="c7df9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c7df9-151">System.String</span></span>

### <span data-ttu-id="c7df9-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c7df9-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c7df9-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7df9-153">OUTPUTS</span></span>

### <span data-ttu-id="c7df9-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7df9-154">System.Boolean</span></span>

## <span data-ttu-id="c7df9-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7df9-155">NOTES</span></span>

## <span data-ttu-id="c7df9-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7df9-156">RELATED LINKS</span></span>

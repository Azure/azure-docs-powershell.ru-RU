---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561059"
---
# <span data-ttu-id="ab57b-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab57b-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="ab57b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab57b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab57b-103">Получает свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab57b-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab57b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab57b-104">SYNTAX</span></span>

### <span data-ttu-id="ab57b-105">ListAllVirtualMachinesParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab57b-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab57b-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ab57b-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab57b-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ab57b-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab57b-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="ab57b-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab57b-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="ab57b-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab57b-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab57b-110">DESCRIPTION</span></span>
<span data-ttu-id="ab57b-111">Командлет **Get-AzureRmVM** получает представление модели и экземпляр для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="ab57b-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="ab57b-112">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab57b-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="ab57b-113">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab57b-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="ab57b-114">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab57b-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="ab57b-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab57b-115">EXAMPLES</span></span>

### <span data-ttu-id="ab57b-116">Пример 1: получение свойств модели и представления экземпляров</span><span class="sxs-lookup"><span data-stu-id="ab57b-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ab57b-117">Эта команда получает свойства представления модели и экземпляра виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ab57b-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="ab57b-118">Пример 2: получение свойств представления экземпляра</span><span class="sxs-lookup"><span data-stu-id="ab57b-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="ab57b-119">Эта команда получает свойства виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ab57b-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ab57b-120">Эта команда задает параметр *Status* .</span><span class="sxs-lookup"><span data-stu-id="ab57b-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="ab57b-121">Таким образом, команда возвращает только свойства представления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ab57b-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="ab57b-122">Пример 3: получение свойств для всех виртуальных машин в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ab57b-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ab57b-123">Эта команда получает свойства всех виртуальных машин в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ab57b-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ab57b-124">Пример 4: получение всех виртуальных машин в подписке</span><span class="sxs-lookup"><span data-stu-id="ab57b-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="ab57b-125">Эта команда возвращает все виртуальные машины в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="ab57b-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="ab57b-126">Пример 5: получение всех виртуальных машин в расположении.</span><span class="sxs-lookup"><span data-stu-id="ab57b-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="ab57b-127">Эта команда возвращает все виртуальные машины в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="ab57b-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="ab57b-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab57b-128">PARAMETERS</span></span>

### <span data-ttu-id="ab57b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab57b-129">-DefaultProfile</span></span>
<span data-ttu-id="ab57b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab57b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab57b-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="ab57b-131">-DisplayHint</span></span>
<span data-ttu-id="ab57b-132">Определяет способ отображения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab57b-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="ab57b-133">Допустимые значения:--Compact: отображает только свойства верхнего уровня--Expand: отображает все свойства на всех уровнях.</span><span class="sxs-lookup"><span data-stu-id="ab57b-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab57b-134">-Location</span><span class="sxs-lookup"><span data-stu-id="ab57b-134">-Location</span></span>
<span data-ttu-id="ab57b-135">Задает расположение для списка виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ab57b-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab57b-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab57b-136">-Name</span></span>
<span data-ttu-id="ab57b-137">Указывает имя виртуальной машины, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ab57b-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab57b-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ab57b-138">-NextLink</span></span>
<span data-ttu-id="ab57b-139">Указывает следующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="ab57b-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab57b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab57b-140">-ResourceGroupName</span></span>
<span data-ttu-id="ab57b-141">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab57b-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab57b-142">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="ab57b-142">-Status</span></span>
<span data-ttu-id="ab57b-143">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab57b-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab57b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab57b-144">CommonParameters</span></span>
<span data-ttu-id="ab57b-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab57b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab57b-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab57b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab57b-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab57b-147">INPUTS</span></span>

### <span data-ttu-id="ab57b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ab57b-148">System.String</span></span>

### <span data-ttu-id="ab57b-149">System. URI</span><span class="sxs-lookup"><span data-stu-id="ab57b-149">System.Uri</span></span>

### <span data-ttu-id="ab57b-150">Microsoft. Azure. Commands. COMPUTE. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="ab57b-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="ab57b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab57b-151">OUTPUTS</span></span>

### <span data-ttu-id="ab57b-152">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ab57b-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ab57b-153">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="ab57b-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="ab57b-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab57b-154">NOTES</span></span>

## <span data-ttu-id="ab57b-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab57b-155">RELATED LINKS</span></span>

[<span data-ttu-id="ab57b-156">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab57b-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ab57b-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab57b-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ab57b-158">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab57b-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="ab57b-159">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab57b-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ab57b-160">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab57b-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ab57b-161">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab57b-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)



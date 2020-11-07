---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911544"
---
# <span data-ttu-id="71404-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="71404-101">Get-AzVM</span></span>

## <span data-ttu-id="71404-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71404-102">SYNOPSIS</span></span>
<span data-ttu-id="71404-103">Получает свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71404-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="71404-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71404-104">SYNTAX</span></span>

### <span data-ttu-id="71404-105">ListAllVirtualMachinesParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71404-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71404-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="71404-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71404-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="71404-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71404-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="71404-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71404-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71404-109">DESCRIPTION</span></span>
<span data-ttu-id="71404-110">Командлет **Get-AzVM** получает представление модели и экземпляр для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="71404-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="71404-111">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71404-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="71404-112">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71404-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="71404-113">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71404-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="71404-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71404-114">EXAMPLES</span></span>

### <span data-ttu-id="71404-115">Пример 1: получение свойств модели и представления экземпляров</span><span class="sxs-lookup"><span data-stu-id="71404-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="71404-116">Эта команда получает свойства представления модели и экземпляра виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="71404-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="71404-117">Пример 2: получение свойств представления экземпляра</span><span class="sxs-lookup"><span data-stu-id="71404-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="71404-118">Эта команда получает свойства виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="71404-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="71404-119">Эта команда задает параметр *Status* .</span><span class="sxs-lookup"><span data-stu-id="71404-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="71404-120">Таким образом, команда возвращает только свойства представления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71404-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="71404-121">Пример 3: получение свойств для всех виртуальных машин в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="71404-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="71404-122">Эта команда получает свойства всех виртуальных машин в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="71404-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="71404-123">Пример 4: получение всех виртуальных машин в подписке</span><span class="sxs-lookup"><span data-stu-id="71404-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="71404-124">Эта команда возвращает все виртуальные машины в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="71404-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="71404-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71404-125">PARAMETERS</span></span>

### <span data-ttu-id="71404-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71404-126">-DefaultProfile</span></span>
<span data-ttu-id="71404-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71404-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71404-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="71404-128">-DisplayHint</span></span>
<span data-ttu-id="71404-129">Определяет способ отображения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71404-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="71404-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="71404-130">Valid values are:</span></span>

<span data-ttu-id="71404-131">--Компактный: отображаются только свойства верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="71404-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="71404-132">--Expand: отображает все свойства на всех уровнях.</span><span class="sxs-lookup"><span data-stu-id="71404-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71404-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71404-133">-Name</span></span>
<span data-ttu-id="71404-134">Указывает имя виртуальной машины, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="71404-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71404-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="71404-135">-NextLink</span></span>
<span data-ttu-id="71404-136">Указывает следующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="71404-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71404-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71404-137">-ResourceGroupName</span></span>
<span data-ttu-id="71404-138">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71404-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71404-139">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="71404-139">-Status</span></span>
<span data-ttu-id="71404-140">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71404-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71404-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71404-141">CommonParameters</span></span>
<span data-ttu-id="71404-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71404-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71404-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71404-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71404-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71404-144">INPUTS</span></span>

### <span data-ttu-id="71404-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="71404-145">None</span></span>
<span data-ttu-id="71404-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="71404-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71404-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71404-147">OUTPUTS</span></span>

### <span data-ttu-id="71404-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="71404-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="71404-149">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="71404-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="71404-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="71404-150">NOTES</span></span>

## <span data-ttu-id="71404-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71404-151">RELATED LINKS</span></span>

[<span data-ttu-id="71404-152">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="71404-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="71404-153">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="71404-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="71404-154">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="71404-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="71404-155">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="71404-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="71404-156">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="71404-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="71404-157">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="71404-157">Update-AzVM</span></span>](./Update-AzVM.md)



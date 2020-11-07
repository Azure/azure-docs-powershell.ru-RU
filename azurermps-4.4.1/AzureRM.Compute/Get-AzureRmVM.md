---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: afe5c168c9a5f3633ce4766df5938a81ccc60510
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732279"
---
# <span data-ttu-id="19127-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19127-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="19127-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19127-102">SYNOPSIS</span></span>
<span data-ttu-id="19127-103">Получает свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19127-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19127-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19127-104">SYNTAX</span></span>

### <span data-ttu-id="19127-105">ListAllVirtualMachinesParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19127-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19127-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="19127-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19127-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="19127-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19127-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="19127-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19127-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19127-109">DESCRIPTION</span></span>
<span data-ttu-id="19127-110">Командлет **Get-AzureRmVM** получает представление модели и экземпляр для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="19127-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="19127-111">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19127-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="19127-112">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19127-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="19127-113">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19127-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="19127-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19127-114">EXAMPLES</span></span>

### <span data-ttu-id="19127-115">Пример 1: получение свойств модели и представления экземпляров</span><span class="sxs-lookup"><span data-stu-id="19127-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="19127-116">Эта команда получает свойства представления модели и экземпляра виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="19127-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="19127-117">Пример 2: получение свойств представления экземпляра</span><span class="sxs-lookup"><span data-stu-id="19127-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="19127-118">Эта команда получает свойства виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="19127-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="19127-119">Эта команда задает параметр *Status* .</span><span class="sxs-lookup"><span data-stu-id="19127-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="19127-120">Таким образом, команда возвращает только свойства представления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="19127-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="19127-121">Пример 3: получение свойств для всех виртуальных машин в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="19127-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="19127-122">Эта команда получает свойства всех виртуальных машин в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="19127-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="19127-123">Пример 4: получение всех виртуальных машин в подписке</span><span class="sxs-lookup"><span data-stu-id="19127-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="19127-124">Эта команда возвращает все виртуальные машины в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="19127-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="19127-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19127-125">PARAMETERS</span></span>

### <span data-ttu-id="19127-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19127-126">-DefaultProfile</span></span>
<span data-ttu-id="19127-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19127-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19127-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="19127-128">-DisplayHint</span></span>
<span data-ttu-id="19127-129">Определяет способ отображения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19127-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="19127-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="19127-130">Valid values are:</span></span>

<span data-ttu-id="19127-131">--Компактный: отображаются только свойства верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="19127-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="19127-132">--Expand: отображает все свойства на всех уровнях.</span><span class="sxs-lookup"><span data-stu-id="19127-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="19127-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19127-133">-Name</span></span>
<span data-ttu-id="19127-134">Указывает имя виртуальной машины, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="19127-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="19127-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="19127-135">-NextLink</span></span>
<span data-ttu-id="19127-136">Указывает следующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="19127-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="19127-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19127-137">-ResourceGroupName</span></span>
<span data-ttu-id="19127-138">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19127-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="19127-139">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="19127-139">-Status</span></span>
<span data-ttu-id="19127-140">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19127-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="19127-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19127-141">CommonParameters</span></span>
<span data-ttu-id="19127-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19127-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19127-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19127-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19127-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19127-144">INPUTS</span></span>

## <span data-ttu-id="19127-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19127-145">OUTPUTS</span></span>

## <span data-ttu-id="19127-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="19127-146">NOTES</span></span>

## <span data-ttu-id="19127-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19127-147">RELATED LINKS</span></span>

[<span data-ttu-id="19127-148">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19127-148">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="19127-149">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19127-149">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="19127-150">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19127-150">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="19127-151">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19127-151">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="19127-152">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19127-152">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="19127-153">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19127-153">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)



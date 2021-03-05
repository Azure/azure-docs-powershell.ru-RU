---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001784"
---
# <span data-ttu-id="c28f0-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="c28f0-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="c28f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c28f0-103">Свойства виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="c28f0-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="c28f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c28f0-104">SYNTAX</span></span>

### <span data-ttu-id="c28f0-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c28f0-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c28f0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c28f0-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c28f0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c28f0-107">DESCRIPTION</span></span>
<span data-ttu-id="c28f0-108">Для **этого можно** получить представление модели и экземпляра виртуальной машины-набора масштаба (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c28f0-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="c28f0-109">Представление модели — это свойства виртуальной машины, заданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="c28f0-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="c28f0-110">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c28f0-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="c28f0-111">Укажите *параметр состояния,* чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c28f0-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="c28f0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c28f0-112">EXAMPLES</span></span>

### <span data-ttu-id="c28f0-113">Пример 1. Свойства виртуальной машины VMSS</span><span class="sxs-lookup"><span data-stu-id="c28f0-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c28f0-114">Эта команда получает свойства виртуальной машины VMSS с именем VMSS001, которая принадлежит к группе ресурсов Group001.</span><span class="sxs-lookup"><span data-stu-id="c28f0-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="c28f0-115">Так как команда не указывает параметр переключения *InstanceView,* командлет получает представление модели виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c28f0-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="c28f0-116">Пример 2. Просмотр свойств представления модели виртуальной машины VMSS</span><span class="sxs-lookup"><span data-stu-id="c28f0-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="c28f0-117">Эта команда получает свойства виртуальной машины VMSS с именем VMSS004, которая принадлежит к группе ресурсов Group002.</span><span class="sxs-lookup"><span data-stu-id="c28f0-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="c28f0-118">Команда получает ИД экземпляра из переменной$ID для которой требуется получить представление модели.</span><span class="sxs-lookup"><span data-stu-id="c28f0-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="c28f0-119">Пример 3. Просмотр свойств представления экземпляра виртуальной машины VMSS</span><span class="sxs-lookup"><span data-stu-id="c28f0-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="c28f0-120">Эта команда получает свойства виртуальной машины VMSS с именем VMSS004, которая принадлежит к группе ресурсов Group002.</span><span class="sxs-lookup"><span data-stu-id="c28f0-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="c28f0-121">Так как команда указывает параметр *переключения InstanceView,* командлет получает представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c28f0-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="c28f0-122">Команда получает ИД экземпляра из переменной$ID для которой требуется получить представление экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c28f0-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="c28f0-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c28f0-123">PARAMETERS</span></span>

### <span data-ttu-id="c28f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28f0-124">-DefaultProfile</span></span>
<span data-ttu-id="c28f0-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c28f0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c28f0-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c28f0-126">-InstanceId</span></span>
<span data-ttu-id="c28f0-127">Определяет ИД экземпляра, для которого требуется получить представление модели.</span><span class="sxs-lookup"><span data-stu-id="c28f0-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28f0-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="c28f0-128">-InstanceView</span></span>
<span data-ttu-id="c28f0-129">Указывает на то, что этот cmdlet получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c28f0-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28f0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28f0-130">-ResourceGroupName</span></span>
<span data-ttu-id="c28f0-131">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="c28f0-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28f0-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c28f0-132">-VMScaleSetName</span></span>
<span data-ttu-id="c28f0-133">Вид имени VMSS.</span><span class="sxs-lookup"><span data-stu-id="c28f0-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28f0-134">CommonParameters</span></span>
<span data-ttu-id="c28f0-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28f0-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c28f0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28f0-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c28f0-137">INPUTS</span></span>

### <span data-ttu-id="c28f0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c28f0-138">System.String</span></span>

## <span data-ttu-id="c28f0-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c28f0-139">OUTPUTS</span></span>

### <span data-ttu-id="c28f0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c28f0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="c28f0-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c28f0-141">NOTES</span></span>

## <span data-ttu-id="c28f0-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c28f0-142">RELATED LINKS</span></span>

[<span data-ttu-id="c28f0-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="c28f0-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="c28f0-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c28f0-144">Get-AzVmss</span></span>](./Get-AzVmss.md)



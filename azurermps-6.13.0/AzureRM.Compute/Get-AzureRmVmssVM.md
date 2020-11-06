---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 00325dc33daa6ec58693dbe6cd6d526ac41b8fd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567808"
---
# <span data-ttu-id="dec95-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="dec95-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="dec95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dec95-102">SYNOPSIS</span></span>
<span data-ttu-id="dec95-103">Получает свойства виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="dec95-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dec95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dec95-104">SYNTAX</span></span>

### <span data-ttu-id="dec95-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dec95-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec95-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="dec95-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dec95-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dec95-107">DESCRIPTION</span></span>
<span data-ttu-id="dec95-108">Командлет **Get-AzureRmVmssVM** получает представление модели и экземпляр для виртуальной машины с набором масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="dec95-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="dec95-109">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dec95-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="dec95-110">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dec95-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="dec95-111">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dec95-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="dec95-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dec95-112">EXAMPLES</span></span>

### <span data-ttu-id="dec95-113">Пример 1: получение свойств виртуальной машины VMSS</span><span class="sxs-lookup"><span data-stu-id="dec95-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="dec95-114">Эта команда получает свойства виртуальной машины VMSS с именем VMSS001, которая относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="dec95-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="dec95-115">Так как в команде не указан параметр переключателя *InstanceView* , командлет получает представление модели виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dec95-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="dec95-116">Пример 2: получение свойств представления модели виртуальной машины VMSS</span><span class="sxs-lookup"><span data-stu-id="dec95-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="dec95-117">Эта команда получает свойства виртуальной машины VMSS с именем VMSS004, которая относится к группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="dec95-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="dec95-118">Команда получает идентификатор экземпляра, хранящийся в $ID переменной, для которого требуется получить представление модели.</span><span class="sxs-lookup"><span data-stu-id="dec95-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="dec95-119">Пример 3: получение свойств представления экземпляра виртуальной машины VMSS</span><span class="sxs-lookup"><span data-stu-id="dec95-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="dec95-120">Эта команда получает свойства виртуальной машины VMSS с именем VMSS004, которая относится к группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="dec95-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="dec95-121">Поскольку в команде указан параметр переключателя *InstanceView* , командлет получает представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dec95-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="dec95-122">Команда получает идентификатор экземпляра, хранящийся в $ID переменной, для которого требуется получить представление экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dec95-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="dec95-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dec95-123">PARAMETERS</span></span>

### <span data-ttu-id="dec95-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec95-124">-DefaultProfile</span></span>
<span data-ttu-id="dec95-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dec95-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec95-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="dec95-126">-InstanceId</span></span>
<span data-ttu-id="dec95-127">Указывает идентификатор экземпляра, для которого требуется получить представление модели.</span><span class="sxs-lookup"><span data-stu-id="dec95-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="dec95-128">-InstanceView</span></span>
<span data-ttu-id="dec95-129">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dec95-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="dec95-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec95-130">-ResourceGroupName</span></span>
<span data-ttu-id="dec95-131">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="dec95-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dec95-132">-VMScaleSetName</span></span>
<span data-ttu-id="dec95-133">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="dec95-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec95-134">CommonParameters</span></span>
<span data-ttu-id="dec95-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dec95-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec95-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec95-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec95-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dec95-137">INPUTS</span></span>

### <span data-ttu-id="dec95-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dec95-138">System.String</span></span>

## <span data-ttu-id="dec95-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dec95-139">OUTPUTS</span></span>

### <span data-ttu-id="dec95-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="dec95-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="dec95-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="dec95-141">NOTES</span></span>

## <span data-ttu-id="dec95-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dec95-142">RELATED LINKS</span></span>

[<span data-ttu-id="dec95-143">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="dec95-143">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="dec95-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dec95-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)



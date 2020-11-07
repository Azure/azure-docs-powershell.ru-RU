---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733907"
---
# <span data-ttu-id="b1631-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="b1631-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1631-102">SYNOPSIS</span></span>
<span data-ttu-id="b1631-103">Возвращает свойства VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1631-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1631-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1631-104">SYNTAX</span></span>

### <span data-ttu-id="b1631-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1631-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1631-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b1631-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1631-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="b1631-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1631-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1631-108">DESCRIPTION</span></span>
<span data-ttu-id="b1631-109">Командлет **Get-AzureRmVmss** Возвращает модель и представление экземпляра набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b1631-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b1631-110">Представление "модель" — свойства, заданные пользователем в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b1631-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="b1631-111">Представление экземпляра — это состояние уровня экземпляра для набора масштабов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b1631-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="b1631-112">Укажите параметр *InstanceView* , чтобы получить только представление экземпляра для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b1631-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="b1631-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1631-113">EXAMPLES</span></span>

### <span data-ttu-id="b1631-114">Пример 1: получение свойств VMSS</span><span class="sxs-lookup"><span data-stu-id="b1631-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b1631-115">Эта команда получает свойства VMSS с именем VMSS001, которые относятся к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="b1631-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="b1631-116">Так как в команде не указан параметр переключателя *InstanceView* , командлет возвращает представление модели для набора масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b1631-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="b1631-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1631-117">PARAMETERS</span></span>

### <span data-ttu-id="b1631-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1631-118">-DefaultProfile</span></span>
<span data-ttu-id="b1631-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1631-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1631-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="b1631-120">-InstanceView</span></span>
<span data-ttu-id="b1631-121">Указывает на то, что этот командлет получает только представление экземпляра для набора масштабов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b1631-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b1631-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="b1631-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="b1631-123">Указывает на то, что этот командлет перечисляет историю обновления операционной системы для набора масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b1631-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1631-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1631-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1631-125">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1631-125">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="b1631-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b1631-126">-VMScaleSetName</span></span>
<span data-ttu-id="b1631-127">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1631-127">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="b1631-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1631-128">CommonParameters</span></span>
<span data-ttu-id="b1631-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1631-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1631-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1631-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1631-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1631-131">INPUTS</span></span>

### <span data-ttu-id="b1631-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b1631-132">System.String</span></span>

## <span data-ttu-id="b1631-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1631-133">OUTPUTS</span></span>

### <span data-ttu-id="b1631-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b1631-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b1631-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1631-135">NOTES</span></span>

## <span data-ttu-id="b1631-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1631-136">RELATED LINKS</span></span>

[<span data-ttu-id="b1631-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b1631-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b1631-139">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="b1631-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b1631-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b1631-142">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="b1631-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1631-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



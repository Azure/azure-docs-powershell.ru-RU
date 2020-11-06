---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568630"
---
# <span data-ttu-id="9424d-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="9424d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9424d-102">SYNOPSIS</span></span>
<span data-ttu-id="9424d-103">Возвращает свойства VMSS.</span><span class="sxs-lookup"><span data-stu-id="9424d-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9424d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9424d-104">SYNTAX</span></span>

### <span data-ttu-id="9424d-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9424d-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="9424d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9424d-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## <span data-ttu-id="9424d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9424d-107">DESCRIPTION</span></span>
<span data-ttu-id="9424d-108">Командлет **Get-AzureRmVmss** Возвращает модель и представление экземпляра набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9424d-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9424d-109">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9424d-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="9424d-110">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9424d-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="9424d-111">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9424d-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="9424d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9424d-112">EXAMPLES</span></span>

### <span data-ttu-id="9424d-113">Пример 1: получение свойств VMSS</span><span class="sxs-lookup"><span data-stu-id="9424d-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="9424d-114">Эта команда получает свойства VMSS с именем VMSS001, которые относятся к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="9424d-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="9424d-115">Так как в команде не указан параметр переключателя *InstanceView* , командлет получает представление модели виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9424d-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="9424d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9424d-116">PARAMETERS</span></span>

### <span data-ttu-id="9424d-117">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="9424d-117">-InstanceView</span></span>
<span data-ttu-id="9424d-118">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9424d-118">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9424d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9424d-119">-ResourceGroupName</span></span>
<span data-ttu-id="9424d-120">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="9424d-120">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9424d-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9424d-121">-VMScaleSetName</span></span>
<span data-ttu-id="9424d-122">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="9424d-122">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9424d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9424d-123">CommonParameters</span></span>
<span data-ttu-id="9424d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9424d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9424d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9424d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9424d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9424d-126">INPUTS</span></span>

### <span data-ttu-id="9424d-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="9424d-127">None</span></span>
<span data-ttu-id="9424d-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9424d-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9424d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9424d-129">OUTPUTS</span></span>

### <span data-ttu-id="9424d-130">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9424d-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9424d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9424d-131">NOTES</span></span>

## <span data-ttu-id="9424d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9424d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9424d-133">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="9424d-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="9424d-135">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="9424d-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="9424d-137">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="9424d-138">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="9424d-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9424d-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



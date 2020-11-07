---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911503"
---
# <span data-ttu-id="19871-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-101">Get-AzVmss</span></span>

## <span data-ttu-id="19871-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19871-102">SYNOPSIS</span></span>
<span data-ttu-id="19871-103">Возвращает свойства VMSS.</span><span class="sxs-lookup"><span data-stu-id="19871-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="19871-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19871-104">SYNTAX</span></span>

### <span data-ttu-id="19871-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19871-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19871-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="19871-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19871-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19871-107">DESCRIPTION</span></span>
<span data-ttu-id="19871-108">Командлет **Get-AzVmss** Возвращает модель и представление экземпляра набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="19871-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="19871-109">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19871-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="19871-110">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19871-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="19871-111">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19871-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="19871-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19871-112">EXAMPLES</span></span>

### <span data-ttu-id="19871-113">Пример 1: получение свойств VMSS</span><span class="sxs-lookup"><span data-stu-id="19871-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="19871-114">Эта команда получает свойства VMSS с именем VMSS001, которые относятся к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="19871-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="19871-115">Так как в команде не указан параметр переключателя *InstanceView* , командлет получает представление модели виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19871-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="19871-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19871-116">PARAMETERS</span></span>

### <span data-ttu-id="19871-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19871-117">-DefaultProfile</span></span>
<span data-ttu-id="19871-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19871-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19871-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="19871-119">-InstanceView</span></span>
<span data-ttu-id="19871-120">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19871-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19871-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19871-121">-ResourceGroupName</span></span>
<span data-ttu-id="19871-122">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="19871-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="19871-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="19871-123">-VMScaleSetName</span></span>
<span data-ttu-id="19871-124">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="19871-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="19871-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19871-125">CommonParameters</span></span>
<span data-ttu-id="19871-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19871-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19871-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19871-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19871-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19871-128">INPUTS</span></span>

### <span data-ttu-id="19871-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="19871-129">None</span></span>
<span data-ttu-id="19871-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="19871-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19871-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19871-131">OUTPUTS</span></span>

### <span data-ttu-id="19871-132">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="19871-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="19871-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="19871-133">NOTES</span></span>

## <span data-ttu-id="19871-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19871-134">RELATED LINKS</span></span>

[<span data-ttu-id="19871-135">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="19871-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="19871-137">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="19871-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="19871-139">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="19871-140">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="19871-141">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19871-141">Update-AzVmss</span></span>](./Update-AzVmss.md)



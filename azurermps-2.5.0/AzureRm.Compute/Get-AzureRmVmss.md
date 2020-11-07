---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914241"
---
# <span data-ttu-id="ace96-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="ace96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ace96-102">SYNOPSIS</span></span>
<span data-ttu-id="ace96-103">Возвращает свойства VMSS.</span><span class="sxs-lookup"><span data-stu-id="ace96-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ace96-104">SYNTAX</span></span>

### <span data-ttu-id="ace96-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ace96-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace96-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ace96-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace96-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace96-107">DESCRIPTION</span></span>
<span data-ttu-id="ace96-108">Командлет **Get-AzureRmVmss** Возвращает модель и представление экземпляра набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ace96-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ace96-109">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace96-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="ace96-110">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace96-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="ace96-111">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace96-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="ace96-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ace96-112">EXAMPLES</span></span>

### <span data-ttu-id="ace96-113">Пример 1: получение свойств VMSS</span><span class="sxs-lookup"><span data-stu-id="ace96-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ace96-114">Эта команда получает свойства VMSS с именем VMSS001, которые относятся к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="ace96-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="ace96-115">Так как в команде не указан параметр переключателя *InstanceView* , командлет получает представление модели виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace96-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="ace96-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ace96-116">PARAMETERS</span></span>

### <span data-ttu-id="ace96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace96-117">-DefaultProfile</span></span>
<span data-ttu-id="ace96-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ace96-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ace96-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="ace96-119">-InstanceView</span></span>
<span data-ttu-id="ace96-120">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace96-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="ace96-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace96-121">-ResourceGroupName</span></span>
<span data-ttu-id="ace96-122">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="ace96-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="ace96-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ace96-123">-VMScaleSetName</span></span>
<span data-ttu-id="ace96-124">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="ace96-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="ace96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace96-125">CommonParameters</span></span>
<span data-ttu-id="ace96-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ace96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace96-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace96-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace96-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ace96-128">INPUTS</span></span>

### <span data-ttu-id="ace96-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="ace96-129">None</span></span>
<span data-ttu-id="ace96-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ace96-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ace96-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace96-131">OUTPUTS</span></span>

### <span data-ttu-id="ace96-132">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ace96-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ace96-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ace96-133">NOTES</span></span>

## <span data-ttu-id="ace96-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ace96-134">RELATED LINKS</span></span>

[<span data-ttu-id="ace96-135">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ace96-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ace96-137">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ace96-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="ace96-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ace96-140">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="ace96-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ace96-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



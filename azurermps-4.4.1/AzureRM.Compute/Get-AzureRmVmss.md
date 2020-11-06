---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: fa8681a8dab5aaba6d82b03a8b3885fd453e1faa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567144"
---
# <span data-ttu-id="9c560-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="9c560-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c560-102">SYNOPSIS</span></span>
<span data-ttu-id="9c560-103">Возвращает свойства VMSS.</span><span class="sxs-lookup"><span data-stu-id="9c560-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c560-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c560-104">SYNTAX</span></span>

### <span data-ttu-id="9c560-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c560-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c560-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9c560-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c560-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c560-107">DESCRIPTION</span></span>
<span data-ttu-id="9c560-108">Командлет **Get-AzureRmVmss** Возвращает модель и представление экземпляра набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9c560-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9c560-109">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c560-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="9c560-110">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c560-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="9c560-111">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c560-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="9c560-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c560-112">EXAMPLES</span></span>

### <span data-ttu-id="9c560-113">Пример 1: получение свойств VMSS</span><span class="sxs-lookup"><span data-stu-id="9c560-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="9c560-114">Эта команда получает свойства VMSS с именем VMSS001, которые относятся к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="9c560-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="9c560-115">Так как в команде не указан параметр переключателя *InstanceView* , командлет получает представление модели виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c560-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="9c560-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c560-116">PARAMETERS</span></span>

### <span data-ttu-id="9c560-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c560-117">-DefaultProfile</span></span>
<span data-ttu-id="9c560-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c560-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c560-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="9c560-119">-InstanceView</span></span>
<span data-ttu-id="9c560-120">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c560-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="9c560-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c560-121">-ResourceGroupName</span></span>
<span data-ttu-id="9c560-122">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="9c560-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="9c560-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9c560-123">-VMScaleSetName</span></span>
<span data-ttu-id="9c560-124">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="9c560-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="9c560-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c560-125">CommonParameters</span></span>
<span data-ttu-id="9c560-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c560-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c560-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c560-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c560-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c560-128">INPUTS</span></span>

## <span data-ttu-id="9c560-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c560-129">OUTPUTS</span></span>

### <span data-ttu-id="9c560-130">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9c560-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9c560-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c560-131">NOTES</span></span>

## <span data-ttu-id="9c560-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c560-132">RELATED LINKS</span></span>

[<span data-ttu-id="9c560-133">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="9c560-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="9c560-135">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="9c560-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="9c560-137">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="9c560-138">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="9c560-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c560-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



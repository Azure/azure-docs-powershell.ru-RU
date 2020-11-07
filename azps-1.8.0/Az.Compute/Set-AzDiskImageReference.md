---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 44339fd00589af880d6cf2d5b3cb45f8c134e590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731255"
---
# <span data-ttu-id="58bc2-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="58bc2-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="58bc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="58bc2-103">Задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="58bc2-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="58bc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58bc2-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58bc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="58bc2-106">Командлет **Set-AzDiskImageReference** задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="58bc2-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="58bc2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="58bc2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58bc2-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="58bc2-109">Первая команда создает локальный дисковый объект с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="58bc2-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="58bc2-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="58bc2-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="58bc2-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для дискового объекта.</span><span class="sxs-lookup"><span data-stu-id="58bc2-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="58bc2-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="58bc2-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="58bc2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58bc2-113">PARAMETERS</span></span>

### <span data-ttu-id="58bc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bc2-114">-DefaultProfile</span></span>
<span data-ttu-id="58bc2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58bc2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58bc2-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="58bc2-116">-Disk</span></span>
<span data-ttu-id="58bc2-117">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="58bc2-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58bc2-118">-ID</span><span class="sxs-lookup"><span data-stu-id="58bc2-118">-Id</span></span>
<span data-ttu-id="58bc2-119">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="58bc2-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="58bc2-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="58bc2-120">-Lun</span></span>
<span data-ttu-id="58bc2-121">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="58bc2-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58bc2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58bc2-122">-Confirm</span></span>
<span data-ttu-id="58bc2-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58bc2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58bc2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58bc2-124">-WhatIf</span></span>
<span data-ttu-id="58bc2-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58bc2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58bc2-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58bc2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58bc2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bc2-127">CommonParameters</span></span>
<span data-ttu-id="58bc2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58bc2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bc2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58bc2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bc2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58bc2-130">INPUTS</span></span>

### <span data-ttu-id="58bc2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="58bc2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="58bc2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="58bc2-132">System.String</span></span>

### <span data-ttu-id="58bc2-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="58bc2-133">System.Int32</span></span>

## <span data-ttu-id="58bc2-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58bc2-134">OUTPUTS</span></span>

### <span data-ttu-id="58bc2-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="58bc2-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="58bc2-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="58bc2-136">NOTES</span></span>

## <span data-ttu-id="58bc2-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58bc2-137">RELATED LINKS</span></span>

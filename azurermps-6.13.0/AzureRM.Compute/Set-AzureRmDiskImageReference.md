---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: e544007d8e23e20ed311f07eb33f98a5e2d6a409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732994"
---
# <span data-ttu-id="3fc70-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="3fc70-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="3fc70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fc70-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc70-103">Задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="3fc70-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fc70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fc70-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fc70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fc70-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc70-106">Командлет **Set-AzureRmDiskImageReference** задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="3fc70-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="3fc70-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fc70-107">EXAMPLES</span></span>

### <span data-ttu-id="3fc70-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3fc70-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="3fc70-109">Первая команда создает локальный дисковый объект с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3fc70-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3fc70-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="3fc70-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="3fc70-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для дискового объекта.</span><span class="sxs-lookup"><span data-stu-id="3fc70-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="3fc70-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3fc70-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3fc70-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fc70-113">PARAMETERS</span></span>

### <span data-ttu-id="3fc70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc70-114">-DefaultProfile</span></span>
<span data-ttu-id="3fc70-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc70-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fc70-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="3fc70-116">-Disk</span></span>
<span data-ttu-id="3fc70-117">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="3fc70-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="3fc70-118">-ID</span><span class="sxs-lookup"><span data-stu-id="3fc70-118">-Id</span></span>
<span data-ttu-id="3fc70-119">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3fc70-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="3fc70-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="3fc70-120">-Lun</span></span>
<span data-ttu-id="3fc70-121">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="3fc70-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="3fc70-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fc70-122">-Confirm</span></span>
<span data-ttu-id="3fc70-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3fc70-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fc70-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fc70-124">-WhatIf</span></span>
<span data-ttu-id="3fc70-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3fc70-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fc70-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fc70-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fc70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc70-127">CommonParameters</span></span>
<span data-ttu-id="3fc70-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fc70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc70-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc70-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc70-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fc70-130">INPUTS</span></span>

### <span data-ttu-id="3fc70-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="3fc70-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="3fc70-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3fc70-132">System.String</span></span>

### <span data-ttu-id="3fc70-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3fc70-133">System.Int32</span></span>

## <span data-ttu-id="3fc70-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fc70-134">OUTPUTS</span></span>

### <span data-ttu-id="3fc70-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="3fc70-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="3fc70-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fc70-136">NOTES</span></span>

## <span data-ttu-id="3fc70-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fc70-137">RELATED LINKS</span></span>

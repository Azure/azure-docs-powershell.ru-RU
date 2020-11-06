---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: 963e6f4621276eda4fdf598d571f2c2171dbc4f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566213"
---
# <span data-ttu-id="c461b-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="c461b-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="c461b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c461b-102">SYNOPSIS</span></span>
<span data-ttu-id="c461b-103">Задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="c461b-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c461b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c461b-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <Disk> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c461b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c461b-105">DESCRIPTION</span></span>
<span data-ttu-id="c461b-106">Командлет **Set-AzureRmDiskImageReference** задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="c461b-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="c461b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c461b-107">EXAMPLES</span></span>

### <span data-ttu-id="c461b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c461b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="c461b-109">Первая команда создает локальный дисковый объект с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c461b-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="c461b-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="c461b-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="c461b-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для дискового объекта.</span><span class="sxs-lookup"><span data-stu-id="c461b-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="c461b-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c461b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c461b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c461b-113">PARAMETERS</span></span>

### <span data-ttu-id="c461b-114">-Диск</span><span class="sxs-lookup"><span data-stu-id="c461b-114">-Disk</span></span>
<span data-ttu-id="c461b-115">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="c461b-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c461b-116">-ID</span><span class="sxs-lookup"><span data-stu-id="c461b-116">-Id</span></span>
<span data-ttu-id="c461b-117">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c461b-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="c461b-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="c461b-118">-Lun</span></span>
<span data-ttu-id="c461b-119">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="c461b-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c461b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c461b-120">-Confirm</span></span>
<span data-ttu-id="c461b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c461b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c461b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c461b-122">-WhatIf</span></span>
<span data-ttu-id="c461b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c461b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c461b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c461b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c461b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c461b-125">CommonParameters</span></span>
<span data-ttu-id="c461b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c461b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c461b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c461b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c461b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c461b-128">INPUTS</span></span>

### <span data-ttu-id="c461b-129">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="c461b-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="c461b-130">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c461b-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c461b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c461b-131">OUTPUTS</span></span>

### <span data-ttu-id="c461b-132">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="c461b-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="c461b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c461b-133">NOTES</span></span>

## <span data-ttu-id="c461b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c461b-134">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 55a3a45cf22dd6558a9728a254531a0e01627e20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566200"
---
# <span data-ttu-id="cdb29-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="cdb29-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="cdb29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cdb29-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb29-103">Задает свойства ссылки на изображение для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="cdb29-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdb29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cdb29-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <DiskUpdate> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb29-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdb29-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb29-106">Командлет **Set-AzureRmDiskUpdateImageReference** задает свойства ссылок на изображения в объекте обновления диска.</span><span class="sxs-lookup"><span data-stu-id="cdb29-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="cdb29-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cdb29-107">EXAMPLES</span></span>

### <span data-ttu-id="cdb29-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cdb29-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="cdb29-109">В первой команде создается объект обновления локального диска с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cdb29-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="cdb29-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="cdb29-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="cdb29-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="cdb29-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="cdb29-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cdb29-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cdb29-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cdb29-113">PARAMETERS</span></span>

### <span data-ttu-id="cdb29-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb29-114">-DiskUpdate</span></span>
<span data-ttu-id="cdb29-115">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="cdb29-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb29-116">-ID</span><span class="sxs-lookup"><span data-stu-id="cdb29-116">-Id</span></span>
<span data-ttu-id="cdb29-117">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="cdb29-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="cdb29-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="cdb29-118">-Lun</span></span>
<span data-ttu-id="cdb29-119">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="cdb29-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="cdb29-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdb29-120">-Confirm</span></span>
<span data-ttu-id="cdb29-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cdb29-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb29-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb29-122">-WhatIf</span></span>
<span data-ttu-id="cdb29-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cdb29-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdb29-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cdb29-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb29-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb29-125">CommonParameters</span></span>
<span data-ttu-id="cdb29-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cdb29-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb29-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb29-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb29-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cdb29-128">INPUTS</span></span>

### <span data-ttu-id="cdb29-129">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb29-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="cdb29-130">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cdb29-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cdb29-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdb29-131">OUTPUTS</span></span>

### <span data-ttu-id="cdb29-132">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb29-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="cdb29-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cdb29-133">NOTES</span></span>

## <span data-ttu-id="cdb29-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdb29-134">RELATED LINKS</span></span>


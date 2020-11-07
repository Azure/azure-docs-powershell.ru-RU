---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914178"
---
# <span data-ttu-id="4ce50-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="4ce50-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="4ce50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ce50-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce50-103">Задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="4ce50-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ce50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ce50-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce50-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ce50-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce50-106">Командлет **Set-AzureRmDiskImageReference** задает свойства ссылки на изображение для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="4ce50-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="4ce50-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ce50-107">EXAMPLES</span></span>

### <span data-ttu-id="4ce50-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ce50-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="4ce50-109">Первая команда создает локальный дисковый объект с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4ce50-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4ce50-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="4ce50-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="4ce50-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для дискового объекта.</span><span class="sxs-lookup"><span data-stu-id="4ce50-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="4ce50-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4ce50-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4ce50-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ce50-113">PARAMETERS</span></span>

### <span data-ttu-id="4ce50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce50-114">-DefaultProfile</span></span>
<span data-ttu-id="4ce50-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce50-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ce50-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="4ce50-116">-Disk</span></span>
<span data-ttu-id="4ce50-117">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="4ce50-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce50-118">-ID</span><span class="sxs-lookup"><span data-stu-id="4ce50-118">-Id</span></span>
<span data-ttu-id="4ce50-119">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="4ce50-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="4ce50-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="4ce50-120">-Lun</span></span>
<span data-ttu-id="4ce50-121">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="4ce50-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="4ce50-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ce50-122">-Confirm</span></span>
<span data-ttu-id="4ce50-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ce50-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce50-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce50-124">-WhatIf</span></span>
<span data-ttu-id="4ce50-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ce50-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ce50-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ce50-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce50-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce50-127">CommonParameters</span></span>
<span data-ttu-id="4ce50-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ce50-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce50-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce50-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce50-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ce50-130">INPUTS</span></span>

### <span data-ttu-id="4ce50-131">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="4ce50-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="4ce50-132">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4ce50-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4ce50-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ce50-133">OUTPUTS</span></span>

### <span data-ttu-id="4ce50-134">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="4ce50-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="4ce50-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ce50-135">NOTES</span></span>

## <span data-ttu-id="4ce50-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ce50-136">RELATED LINKS</span></span>


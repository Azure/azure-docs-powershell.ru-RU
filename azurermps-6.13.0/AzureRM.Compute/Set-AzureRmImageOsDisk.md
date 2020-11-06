---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 74dbe48c40dfa08df9fd224f43774095d10a539c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568940"
---
# <span data-ttu-id="0637a-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="0637a-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="0637a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0637a-102">SYNOPSIS</span></span>
<span data-ttu-id="0637a-103">Задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="0637a-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0637a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0637a-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0637a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0637a-105">DESCRIPTION</span></span>
<span data-ttu-id="0637a-106">Командлет **Set-AzureRmImageOsDisk** задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="0637a-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="0637a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0637a-107">EXAMPLES</span></span>

### <span data-ttu-id="0637a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0637a-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="0637a-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0637a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="0637a-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="0637a-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="0637a-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="0637a-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="0637a-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0637a-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0637a-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="0637a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="0637a-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0637a-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0637a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0637a-115">PARAMETERS</span></span>

### <span data-ttu-id="0637a-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="0637a-116">-BlobUri</span></span>
<span data-ttu-id="0637a-117">Задает универсальный код ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0637a-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="0637a-118">-Caching</span></span>
<span data-ttu-id="0637a-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="0637a-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0637a-120">-DefaultProfile</span></span>
<span data-ttu-id="0637a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0637a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0637a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0637a-122">-DiskSizeGB</span></span>
<span data-ttu-id="0637a-123">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="0637a-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-124">-Image</span><span class="sxs-lookup"><span data-stu-id="0637a-124">-Image</span></span>
<span data-ttu-id="0637a-125">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="0637a-125">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="0637a-126">-ManagedDiskId</span></span>
<span data-ttu-id="0637a-127">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="0637a-127">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="0637a-128">-OsState</span></span>
<span data-ttu-id="0637a-129">Указывает состояние операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0637a-129">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="0637a-130">-OsType</span></span>
<span data-ttu-id="0637a-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0637a-131">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="0637a-132">-SnapshotId</span></span>
<span data-ttu-id="0637a-133">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="0637a-133">Specifies the ID of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0637a-134">-StorageAccountType</span></span>
<span data-ttu-id="0637a-135">Тип учетной записи хранения на диске образа операционной системы</span><span class="sxs-lookup"><span data-stu-id="0637a-135">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0637a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0637a-136">-Confirm</span></span>
<span data-ttu-id="0637a-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0637a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0637a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0637a-138">-WhatIf</span></span>
<span data-ttu-id="0637a-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0637a-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0637a-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0637a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0637a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0637a-141">CommonParameters</span></span>
<span data-ttu-id="0637a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0637a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0637a-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0637a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0637a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0637a-144">INPUTS</span></span>

### <span data-ttu-id="0637a-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="0637a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="0637a-146">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0637a-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0637a-147">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0637a-147">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0637a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0637a-148">System.String</span></span>

### <span data-ttu-id="0637a-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0637a-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0637a-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0637a-150">System.Int32</span></span>

## <span data-ttu-id="0637a-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0637a-151">OUTPUTS</span></span>

### <span data-ttu-id="0637a-152">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="0637a-152">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0637a-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="0637a-153">NOTES</span></span>

## <span data-ttu-id="0637a-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0637a-154">RELATED LINKS</span></span>

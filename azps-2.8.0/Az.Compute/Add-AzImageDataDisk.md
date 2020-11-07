---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 5b3ea899b7cd1b5868fd3f230358a75e92ec1d3e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727531"
---
# <span data-ttu-id="d0522-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="d0522-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="d0522-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0522-102">SYNOPSIS</span></span>
<span data-ttu-id="d0522-103">Добавляет диск с данными в объект Image.</span><span class="sxs-lookup"><span data-stu-id="d0522-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="d0522-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0522-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0522-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0522-105">DESCRIPTION</span></span>
<span data-ttu-id="d0522-106">Командлет **Add-AzImageDataDisk** добавляет диск с данными в объект Image.</span><span class="sxs-lookup"><span data-stu-id="d0522-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="d0522-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0522-107">EXAMPLES</span></span>

### <span data-ttu-id="d0522-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0522-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="d0522-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d0522-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="d0522-110">Следующие три команды назначают пути к дискам операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="d0522-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d0522-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="d0522-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="d0522-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d0522-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d0522-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="d0522-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="d0522-114">Последняя команда создает изображение с именем ImageName01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d0522-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d0522-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0522-115">PARAMETERS</span></span>

### <span data-ttu-id="d0522-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="d0522-116">-BlobUri</span></span>
<span data-ttu-id="d0522-117">Указывает ссылку в качестве универсального кода ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="d0522-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0522-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="d0522-118">-Caching</span></span>
<span data-ttu-id="d0522-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="d0522-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0522-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0522-120">-DefaultProfile</span></span>
<span data-ttu-id="d0522-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0522-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0522-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d0522-122">-DiskSizeGB</span></span>
<span data-ttu-id="d0522-123">Задает размер диска в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="d0522-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="d0522-124">-Image</span><span class="sxs-lookup"><span data-stu-id="d0522-124">-Image</span></span>
<span data-ttu-id="d0522-125">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="d0522-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="d0522-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="d0522-126">-Lun</span></span>
<span data-ttu-id="d0522-127">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="d0522-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0522-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d0522-128">-ManagedDiskId</span></span>
<span data-ttu-id="d0522-129">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="d0522-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="d0522-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="d0522-130">-SnapshotId</span></span>
<span data-ttu-id="d0522-131">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="d0522-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="d0522-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d0522-132">-StorageAccountType</span></span>
<span data-ttu-id="d0522-133">Тип учетной записи хранения на диске образа данных</span><span class="sxs-lookup"><span data-stu-id="d0522-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="d0522-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0522-134">-Confirm</span></span>
<span data-ttu-id="d0522-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0522-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0522-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0522-136">-WhatIf</span></span>
<span data-ttu-id="d0522-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0522-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0522-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0522-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0522-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0522-139">CommonParameters</span></span>
<span data-ttu-id="d0522-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0522-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0522-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0522-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0522-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0522-142">INPUTS</span></span>

### <span data-ttu-id="d0522-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="d0522-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="d0522-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d0522-144">System.Int32</span></span>

### <span data-ttu-id="d0522-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d0522-145">System.String</span></span>

### <span data-ttu-id="d0522-146">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d0522-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d0522-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0522-147">OUTPUTS</span></span>

### <span data-ttu-id="d0522-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="d0522-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="d0522-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0522-149">NOTES</span></span>

## <span data-ttu-id="d0522-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0522-150">RELATED LINKS</span></span>

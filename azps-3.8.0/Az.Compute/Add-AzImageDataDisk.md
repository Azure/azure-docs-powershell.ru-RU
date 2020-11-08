---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064767"
---
# <span data-ttu-id="af422-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="af422-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="af422-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af422-102">SYNOPSIS</span></span>
<span data-ttu-id="af422-103">Добавляет диск с данными в объект Image.</span><span class="sxs-lookup"><span data-stu-id="af422-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="af422-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af422-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af422-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af422-105">DESCRIPTION</span></span>
<span data-ttu-id="af422-106">Командлет **Add-AzImageDataDisk** добавляет диск с данными в объект Image.</span><span class="sxs-lookup"><span data-stu-id="af422-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="af422-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af422-107">EXAMPLES</span></span>

### <span data-ttu-id="af422-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af422-108">Example 1</span></span>
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

<span data-ttu-id="af422-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="af422-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="af422-110">Следующие три команды назначают пути к дискам операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="af422-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="af422-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="af422-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="af422-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="af422-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="af422-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="af422-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="af422-114">Последняя команда создает изображение с именем ImageName01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="af422-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="af422-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af422-115">PARAMETERS</span></span>

### <span data-ttu-id="af422-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="af422-116">-BlobUri</span></span>
<span data-ttu-id="af422-117">Указывает ссылку в качестве универсального кода ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="af422-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="af422-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="af422-118">-Caching</span></span>
<span data-ttu-id="af422-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="af422-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="af422-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af422-120">-DefaultProfile</span></span>
<span data-ttu-id="af422-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af422-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af422-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="af422-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="af422-123">Указывает идентификатор ресурса набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="af422-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="af422-124">Это может быть указано только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="af422-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="af422-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="af422-125">-DiskSizeGB</span></span>
<span data-ttu-id="af422-126">Задает размер диска в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="af422-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="af422-127">-Image</span><span class="sxs-lookup"><span data-stu-id="af422-127">-Image</span></span>
<span data-ttu-id="af422-128">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="af422-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="af422-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="af422-129">-Lun</span></span>
<span data-ttu-id="af422-130">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="af422-130">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="af422-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="af422-131">-ManagedDiskId</span></span>
<span data-ttu-id="af422-132">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="af422-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="af422-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="af422-133">-SnapshotId</span></span>
<span data-ttu-id="af422-134">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="af422-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="af422-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="af422-135">-StorageAccountType</span></span>
<span data-ttu-id="af422-136">Тип учетной записи хранения на диске образа данных</span><span class="sxs-lookup"><span data-stu-id="af422-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="af422-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af422-137">-Confirm</span></span>
<span data-ttu-id="af422-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af422-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af422-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af422-139">-WhatIf</span></span>
<span data-ttu-id="af422-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af422-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af422-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af422-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af422-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af422-142">CommonParameters</span></span>
<span data-ttu-id="af422-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af422-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af422-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af422-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af422-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af422-145">INPUTS</span></span>

### <span data-ttu-id="af422-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="af422-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="af422-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="af422-147">System.Int32</span></span>

### <span data-ttu-id="af422-148">System. String</span><span class="sxs-lookup"><span data-stu-id="af422-148">System.String</span></span>

### <span data-ttu-id="af422-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="af422-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="af422-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af422-150">OUTPUTS</span></span>

### <span data-ttu-id="af422-151">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="af422-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="af422-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="af422-152">NOTES</span></span>

## <span data-ttu-id="af422-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af422-153">RELATED LINKS</span></span>

---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: e38402359a3bccebc33d92211ed10d8032a0dd4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977096"
---
# <span data-ttu-id="ab1f0-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="ab1f0-101">New-AzImportExport</span></span>

## <span data-ttu-id="ab1f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1f0-103">Создание нового задания или обновление существующего задания в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="ab1f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab1f0-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ab1f0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="ab1f0-106">Создание нового задания или обновление существующего задания в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="ab1f0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="ab1f0-108">Пример 1. Создание задания ImportExport</span><span class="sxs-lookup"><span data-stu-id="ab1f0-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ab1f0-109">Эти cmdlets создают задание ImportExport.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="ab1f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab1f0-110">PARAMETERS</span></span>

### <span data-ttu-id="ab1f0-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ab1f0-111">-AcceptLanguage</span></span>
<span data-ttu-id="ab1f0-112">Указывает предпочтительный язык для ответа.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="ab1f0-113">-BackupDriveManifest</span></span>
<span data-ttu-id="ab1f0-114">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-114">Default value is false.</span></span>
<span data-ttu-id="ab1f0-115">Указывает на то, следует ли копировать файлы манифеста на дисках, чтобы блокировать BLOB-файлы.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="ab1f0-116">-BlobListBlobPath</span></span>
<span data-ttu-id="ab1f0-117">Набор строк BLOB-пути.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="ab1f0-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="ab1f0-119">Набор строк С BLOB-префиксами.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="ab1f0-120">-CancelRequested</span></span>
<span data-ttu-id="ab1f0-121">Указывает, был ли отправлен запрос на отмену задания.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-121">Indicates whether a request has been submitted to cancel the job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="ab1f0-122">-ClientTenantId</span></span>
<span data-ttu-id="ab1f0-123">ИД клиента, который запрашивает клиент.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-123">The tenant ID of the client making the request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1f0-124">-DefaultProfile</span></span>
<span data-ttu-id="ab1f0-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="ab1f0-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="ab1f0-127">Название оператора, который используется для импорта или экспорта дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-127">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="ab1f0-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="ab1f0-129">Количество дисков, включенных в пакет.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-129">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="ab1f0-131">Дата отгрузки пакета.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-131">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="ab1f0-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="ab1f0-133">Номер для отслеживания пакета.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-133">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="ab1f0-134">-DiagnosticsPath</span></span>
<span data-ttu-id="ab1f0-135">Виртуальный каталог BLOB-файлов, в котором будут храниться журналы копирования и резервные копии файлов манифеста диска (если они включены).</span><span class="sxs-lookup"><span data-stu-id="ab1f0-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="ab1f0-136">-DriveList</span></span>
<span data-ttu-id="ab1f0-137">Список из десяти дисков, которые входят в состав задания.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="ab1f0-138">Список дисков является элементом, требуемого для задания импорта. оно не задано для заданий экспорта.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="ab1f0-139">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств DRIVELIST и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="ab1f0-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="ab1f0-141">Относительный URI для BLOB-блоков, которые содержат список путей blob-блоков или префиксов путей BLOB-блоков, как определено выше, начиная с имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="ab1f0-142">Если BLOB-проект находится в корневом контейнере, URI должен начинаться с $root.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-142">If the blob is in root container, the URI must begin with $root.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="ab1f0-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="ab1f0-144">Путь к BLOB-пакету, который указывает на большой большой блок блока, содержащий список имен BLOB-блоков, которые не были экспортированы из-за нехватки места на диске.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="ab1f0-145">Если экспорт всех BLOB-элементов был успешно завершен, этот элемент не включается в ответ.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="ab1f0-146">-JobType</span></span>
<span data-ttu-id="ab1f0-147">Тип задания</span><span class="sxs-lookup"><span data-stu-id="ab1f0-147">The type of job</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-148">-Location</span><span class="sxs-lookup"><span data-stu-id="ab1f0-148">-Location</span></span>
<span data-ttu-id="ab1f0-149">Указывает поддерживаемую службу Azure, в которой должно быть создано задание.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-149">Specifies the supported Azure location where the job should be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="ab1f0-150">-LogLevel</span></span>
<span data-ttu-id="ab1f0-151">Значение по умолчанию — "Ошибка".</span><span class="sxs-lookup"><span data-stu-id="ab1f0-151">Default value is Error.</span></span>
<span data-ttu-id="ab1f0-152">Указывает, включено ли ведение журнала ошибок или подробное ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-153">-Name</span><span class="sxs-lookup"><span data-stu-id="ab1f0-153">-Name</span></span>
<span data-ttu-id="ab1f0-154">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="ab1f0-155">-PercentComplete</span></span>
<span data-ttu-id="ab1f0-156">Общий процент завершения задания.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-156">Overall percentage completed for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="ab1f0-157">-ProvisioningState</span></span>
<span data-ttu-id="ab1f0-158">Определяет состояние подготовка задания.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-158">Specifies the provisioning state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab1f0-159">-ResourceGroupName</span></span>
<span data-ttu-id="ab1f0-160">Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="ab1f0-161">-ReturnAddressCity</span></span>
<span data-ttu-id="ab1f0-162">Название города, которое будет использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-162">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="ab1f0-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="ab1f0-164">Страна или регион, которые будут применяться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-164">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="ab1f0-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="ab1f0-166">Адрес электронной почты получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-166">Email address of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="ab1f0-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="ab1f0-168">Номер телефона получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-168">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="ab1f0-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="ab1f0-170">Почтовый индекс, который будет применяться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-170">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="ab1f0-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="ab1f0-172">Имя получателя, который получит жесткие диски при возврате.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="ab1f0-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="ab1f0-174">Область или край, используемая при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-174">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="ab1f0-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="ab1f0-176">Первая строка адреса, используемого при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-176">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="ab1f0-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="ab1f0-178">Вторая строка адреса, используемого при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-178">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="ab1f0-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="ab1f0-180">Название оператора, который используется для импорта или экспорта дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-180">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="ab1f0-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="ab1f0-182">Количество дисков, включенных в пакет.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-182">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="ab1f0-184">Дата отгрузки пакета.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-184">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="ab1f0-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="ab1f0-186">Номер для отслеживания пакета.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-186">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="ab1f0-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="ab1f0-188">Номер счета клиента у оператора связи.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-188">The customer's account number with the carrier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="ab1f0-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="ab1f0-190">Имя оператора связи.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-190">The carrier's name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="ab1f0-191">-ShippingInformationCity</span></span>
<span data-ttu-id="ab1f0-192">Название города, которое будет использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-192">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="ab1f0-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="ab1f0-194">Страна или регион, которые будут применяться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-194">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="ab1f0-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="ab1f0-196">Номер телефона получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-196">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="ab1f0-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="ab1f0-198">Почтовый индекс, который будет применяться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-198">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="ab1f0-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="ab1f0-200">Имя получателя, который получит жесткие диски при возврате.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="ab1f0-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="ab1f0-202">Область или край, используемая при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-202">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="ab1f0-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="ab1f0-204">Первая строка адреса, используемого при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-204">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="ab1f0-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="ab1f0-206">Вторая строка адреса, используемого при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-206">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-207">-State</span><span class="sxs-lookup"><span data-stu-id="ab1f0-207">-State</span></span>
<span data-ttu-id="ab1f0-208">Текущее состояние задания.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-208">Current state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ab1f0-209">-StorageAccountId</span></span>
<span data-ttu-id="ab1f0-210">Идентификатор ресурса учетной записи хранения, в который будут импортироваться или экспортироваться данные.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab1f0-211">-SubscriptionId</span></span>
<span data-ttu-id="ab1f0-212">ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab1f0-213">-Tag</span></span>
<span data-ttu-id="ab1f0-214">Определяет теги, которые будут назначены задаче.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-215">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab1f0-215">-Confirm</span></span>
<span data-ttu-id="ab1f0-216">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab1f0-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab1f0-217">-WhatIf</span></span>
<span data-ttu-id="ab1f0-218">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab1f0-219">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab1f0-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1f0-220">CommonParameters</span></span>
<span data-ttu-id="ab1f0-221">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1f0-222">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab1f0-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1f0-223">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab1f0-223">INPUTS</span></span>

## <span data-ttu-id="ab1f0-224">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab1f0-224">OUTPUTS</span></span>

### <span data-ttu-id="ab1f0-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="ab1f0-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="ab1f0-226">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab1f0-226">NOTES</span></span>

<span data-ttu-id="ab1f0-227">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ab1f0-227">ALIASES</span></span>

<span data-ttu-id="ab1f0-228">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ab1f0-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab1f0-229">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab1f0-230">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab1f0-231">DriveLIST <IDriveStatus[]>: список из десяти дисков, которые входят в состав этой работы.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="ab1f0-232">Список дисков является элементом, требуемого для задания импорта. оно не задано для заданий экспорта.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="ab1f0-233">`[BitLockerKey <String>]`. Ключ BitLocker, используемый для шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="ab1f0-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="ab1f0-235">`[CopyStatus <String>]`: подробное состояние процесса передачи данных.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="ab1f0-236">Это поле не возвращается в ответе, пока диск не находится в состоянии переноса.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="ab1f0-237">`[DriveHeaderHash <String>]`. Hash value the drive header (Hash value).</span><span class="sxs-lookup"><span data-stu-id="ab1f0-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="ab1f0-238">`[DriveId <String>]`: серийный номер диска без пробелов.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="ab1f0-239">`[ErrorLogUri <String>]`: URI, который указывает на BLOB-проект, содержащий журнал ошибок для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="ab1f0-240">`[ManifestFile <String>]`: Относительный путь к файлу манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="ab1f0-241">`[ManifestHash <String>]`: Зашифрованный с кодом MD5(с кодом Base16) hash файла манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="ab1f0-242">`[ManifestUri <String>]`: URI, который указывает на BLOB-файл, содержащий файл манифеста диска.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="ab1f0-243">`[PercentComplete <Int32?>]`: процентное завершения для диска.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="ab1f0-244">`[State <DriveState?>]`. Текущее состояние диска.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="ab1f0-245">`[VerboseLogUri <String>]`: URI, который указывает на BLOB-проект, содержащий подробный журнал для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="ab1f0-246">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab1f0-246">RELATED LINKS</span></span>


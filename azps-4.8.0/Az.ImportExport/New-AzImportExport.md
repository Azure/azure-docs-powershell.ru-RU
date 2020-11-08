---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236689"
---
# <span data-ttu-id="2313e-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="2313e-101">New-AzImportExport</span></span>

## <span data-ttu-id="2313e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2313e-102">SYNOPSIS</span></span>
<span data-ttu-id="2313e-103">Создание нового задания или обновление существующего задания в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="2313e-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="2313e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2313e-104">SYNTAX</span></span>

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

## <span data-ttu-id="2313e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2313e-105">DESCRIPTION</span></span>
<span data-ttu-id="2313e-106">Создание нового задания или обновление существующего задания в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="2313e-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="2313e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2313e-107">EXAMPLES</span></span>

### <span data-ttu-id="2313e-108">Пример 1: создание нового задания ImportExport</span><span class="sxs-lookup"><span data-stu-id="2313e-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2313e-109">Эти командлеты создают новое задание ImportExport.</span><span class="sxs-lookup"><span data-stu-id="2313e-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="2313e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2313e-110">PARAMETERS</span></span>

### <span data-ttu-id="2313e-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2313e-111">-AcceptLanguage</span></span>
<span data-ttu-id="2313e-112">Указывает предпочтительный язык ответа.</span><span class="sxs-lookup"><span data-stu-id="2313e-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="2313e-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="2313e-113">-BackupDriveManifest</span></span>
<span data-ttu-id="2313e-114">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="2313e-114">Default value is false.</span></span>
<span data-ttu-id="2313e-115">Указывает, должны ли файлы манифестов на дисках быть скопированы в блоки больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="2313e-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="2313e-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="2313e-116">-BlobListBlobPath</span></span>
<span data-ttu-id="2313e-117">Коллекция строк двоичного объекта Path.</span><span class="sxs-lookup"><span data-stu-id="2313e-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="2313e-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="2313e-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="2313e-119">Коллекция строк префиксов BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="2313e-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="2313e-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="2313e-120">-CancelRequested</span></span>
<span data-ttu-id="2313e-121">Указывает, был ли отправлен запрос на отмену задания.</span><span class="sxs-lookup"><span data-stu-id="2313e-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="2313e-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="2313e-122">-ClientTenantId</span></span>
<span data-ttu-id="2313e-123">Идентификатор клиента, который выполнив запрос.</span><span class="sxs-lookup"><span data-stu-id="2313e-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="2313e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2313e-124">-DefaultProfile</span></span>
<span data-ttu-id="2313e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2313e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2313e-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="2313e-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="2313e-127">Имя несущей частоты, используемой для отправки и импорта и экспорта дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="2313e-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="2313e-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="2313e-129">Количество дисков, включенных в пакет.</span><span class="sxs-lookup"><span data-stu-id="2313e-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="2313e-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="2313e-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="2313e-131">Дата отгрузки пакета.</span><span class="sxs-lookup"><span data-stu-id="2313e-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="2313e-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="2313e-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="2313e-133">Номер отслеживания пакета.</span><span class="sxs-lookup"><span data-stu-id="2313e-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="2313e-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="2313e-134">-DiagnosticsPath</span></span>
<span data-ttu-id="2313e-135">Виртуальный каталог BLOB-объектов, на который будут храниться журналы копирования и резервные копии файлов манифеста диска (если она включена).</span><span class="sxs-lookup"><span data-stu-id="2313e-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="2313e-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="2313e-136">-DriveList</span></span>
<span data-ttu-id="2313e-137">Список до десяти дисков, составляющих задание.</span><span class="sxs-lookup"><span data-stu-id="2313e-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="2313e-138">Список дисков является обязательным элементом для задания импорта; Он не указан для задания экспорта.</span><span class="sxs-lookup"><span data-stu-id="2313e-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="2313e-139">Для конструирования ознакомьтесь с разделом "Заметки" для свойств DRIVELIST и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="2313e-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="2313e-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="2313e-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="2313e-141">Относительный URI для блочного большого двоичного объекта, содержащего список путей BLOB-объектов или префиксов двоичных объектов, описанных выше, начиная с имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="2313e-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="2313e-142">Если большой двоичный объект находится в корневом контейнере, URI должен начинаться с $root.</span><span class="sxs-lookup"><span data-stu-id="2313e-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="2313e-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="2313e-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="2313e-144">Путь к большому двоичному объекту, указывающий на большой двоичный объект, который содержит список имен BLOB-объектов, которые не были экспортированы вследствие недостатка места на диске.</span><span class="sxs-lookup"><span data-stu-id="2313e-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="2313e-145">Если все большие двоичные объекты были успешно экспортированы, этот элемент не будет включен в ответ.</span><span class="sxs-lookup"><span data-stu-id="2313e-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="2313e-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="2313e-146">-JobType</span></span>
<span data-ttu-id="2313e-147">Тип задания</span><span class="sxs-lookup"><span data-stu-id="2313e-147">The type of job</span></span>

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

### <span data-ttu-id="2313e-148">-Location</span><span class="sxs-lookup"><span data-stu-id="2313e-148">-Location</span></span>
<span data-ttu-id="2313e-149">Указывает расположение, в котором необходимо создать задание в Azure.</span><span class="sxs-lookup"><span data-stu-id="2313e-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="2313e-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="2313e-150">-LogLevel</span></span>
<span data-ttu-id="2313e-151">Значение по умолчанию — Error.</span><span class="sxs-lookup"><span data-stu-id="2313e-151">Default value is Error.</span></span>
<span data-ttu-id="2313e-152">Указывает, будет ли включена регистрация ошибок или подробное ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="2313e-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="2313e-153">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2313e-153">-Name</span></span>
<span data-ttu-id="2313e-154">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="2313e-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="2313e-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="2313e-155">-PercentComplete</span></span>
<span data-ttu-id="2313e-156">Общий процент выполнения для задания.</span><span class="sxs-lookup"><span data-stu-id="2313e-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="2313e-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="2313e-157">-ProvisioningState</span></span>
<span data-ttu-id="2313e-158">Задает состояние подготовки задания.</span><span class="sxs-lookup"><span data-stu-id="2313e-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="2313e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2313e-159">-ResourceGroupName</span></span>
<span data-ttu-id="2313e-160">Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="2313e-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="2313e-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="2313e-161">-ReturnAddressCity</span></span>
<span data-ttu-id="2313e-162">Название города, которое будет использоваться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="2313e-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="2313e-164">Страна или регион, которые нужно использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="2313e-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="2313e-166">Адрес электронной почты получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="2313e-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="2313e-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="2313e-168">Номер телефона получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="2313e-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="2313e-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="2313e-170">Почтовый индекс, который будет использоваться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="2313e-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="2313e-172">Имя получателя, который будет получать жесткие диски при их возвращении.</span><span class="sxs-lookup"><span data-stu-id="2313e-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="2313e-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="2313e-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="2313e-174">Область или край, которые нужно использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="2313e-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="2313e-176">Первая строка почтового адреса, который будет использоваться для возврата дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="2313e-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="2313e-178">Вторая строка почтового адреса, который будет использоваться для возврата дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="2313e-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="2313e-180">Имя несущей частоты, используемой для отправки и импорта и экспорта дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="2313e-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="2313e-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="2313e-182">Количество дисков, включенных в пакет.</span><span class="sxs-lookup"><span data-stu-id="2313e-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="2313e-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="2313e-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="2313e-184">Дата отгрузки пакета.</span><span class="sxs-lookup"><span data-stu-id="2313e-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="2313e-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="2313e-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="2313e-186">Номер отслеживания пакета.</span><span class="sxs-lookup"><span data-stu-id="2313e-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="2313e-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="2313e-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="2313e-188">Номер счета клиента с перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="2313e-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="2313e-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="2313e-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="2313e-190">Название несущей частоты.</span><span class="sxs-lookup"><span data-stu-id="2313e-190">The carrier's name.</span></span>

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

### <span data-ttu-id="2313e-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="2313e-191">-ShippingInformationCity</span></span>
<span data-ttu-id="2313e-192">Название города, которое будет использоваться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="2313e-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="2313e-194">Страна или регион, которые нужно использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="2313e-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="2313e-196">Номер телефона получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="2313e-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="2313e-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="2313e-198">Почтовый индекс, который будет использоваться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="2313e-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="2313e-200">Имя получателя, который будет получать жесткие диски при их возвращении.</span><span class="sxs-lookup"><span data-stu-id="2313e-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="2313e-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="2313e-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="2313e-202">Область или край, которые нужно использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="2313e-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="2313e-204">Первая строка почтового адреса, который будет использоваться для возврата дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="2313e-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="2313e-206">Вторая строка почтового адреса, который будет использоваться для возврата дисков.</span><span class="sxs-lookup"><span data-stu-id="2313e-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="2313e-207">-State</span><span class="sxs-lookup"><span data-stu-id="2313e-207">-State</span></span>
<span data-ttu-id="2313e-208">Текущее состояние задания.</span><span class="sxs-lookup"><span data-stu-id="2313e-208">Current state of the job.</span></span>

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

### <span data-ttu-id="2313e-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2313e-209">-StorageAccountId</span></span>
<span data-ttu-id="2313e-210">Идентификатор ресурса учетной записи хранения, из которой данные будут импортированы или из которых экспортируются.</span><span class="sxs-lookup"><span data-stu-id="2313e-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="2313e-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2313e-211">-SubscriptionId</span></span>
<span data-ttu-id="2313e-212">Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="2313e-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="2313e-213">-Тег</span><span class="sxs-lookup"><span data-stu-id="2313e-213">-Tag</span></span>
<span data-ttu-id="2313e-214">Указывает теги, которые будут назначены заданию.</span><span class="sxs-lookup"><span data-stu-id="2313e-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="2313e-215">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2313e-215">-Confirm</span></span>
<span data-ttu-id="2313e-216">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2313e-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2313e-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2313e-217">-WhatIf</span></span>
<span data-ttu-id="2313e-218">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2313e-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2313e-219">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2313e-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2313e-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2313e-220">CommonParameters</span></span>
<span data-ttu-id="2313e-221">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2313e-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2313e-222">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2313e-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2313e-223">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2313e-223">INPUTS</span></span>

## <span data-ttu-id="2313e-224">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2313e-224">OUTPUTS</span></span>

### <span data-ttu-id="2313e-225">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="2313e-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="2313e-226">Пуск</span><span class="sxs-lookup"><span data-stu-id="2313e-226">NOTES</span></span>

<span data-ttu-id="2313e-227">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="2313e-227">ALIASES</span></span>

<span data-ttu-id="2313e-228">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2313e-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2313e-229">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2313e-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2313e-230">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2313e-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2313e-231">DRIVELIST <IDriveStatus [] >: список до десяти дисков, составляющих задание.</span><span class="sxs-lookup"><span data-stu-id="2313e-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="2313e-232">Список дисков является обязательным элементом для задания импорта; Он не указан для задания экспорта.</span><span class="sxs-lookup"><span data-stu-id="2313e-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="2313e-233">`[BitLockerKey <String>]`: Ключ BitLocker, используемый для шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="2313e-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="2313e-234">`[BytesSucceeded <Int64?>]`: Байты успешно переданы на диск.</span><span class="sxs-lookup"><span data-stu-id="2313e-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="2313e-235">`[CopyStatus <String>]`: Подробные сведения о состоянии процесса передачи данных.</span><span class="sxs-lookup"><span data-stu-id="2313e-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="2313e-236">Это поле не возвращается в ответе до тех пор, пока диск не находится в состоянии перепередачи.</span><span class="sxs-lookup"><span data-stu-id="2313e-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="2313e-237">`[DriveHeaderHash <String>]`: Хэш-значение заголовка диска.</span><span class="sxs-lookup"><span data-stu-id="2313e-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="2313e-238">`[DriveId <String>]`: Серийный номер оборудования диска без пробелов.</span><span class="sxs-lookup"><span data-stu-id="2313e-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="2313e-239">`[ErrorLogUri <String>]`: URI, указывающий на большой двоичный объект, который содержит журнал ошибок для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="2313e-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="2313e-240">`[ManifestFile <String>]`: Относительный путь к файлу манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="2313e-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="2313e-241">`[ManifestHash <String>]`: Хэш MD5, закодированный Base16, для файла манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="2313e-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="2313e-242">`[ManifestUri <String>]`: URI, указывающий на большой двоичный объект, содержащий файл манифеста диска.</span><span class="sxs-lookup"><span data-stu-id="2313e-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="2313e-243">`[PercentComplete <Int32?>]`: Процент завершения для диска.</span><span class="sxs-lookup"><span data-stu-id="2313e-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="2313e-244">`[State <DriveState?>]`: Текущее состояние диска.</span><span class="sxs-lookup"><span data-stu-id="2313e-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="2313e-245">`[VerboseLogUri <String>]`: URI, указывающий на большой двоичный объект, содержащий подробный журнал для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="2313e-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="2313e-246">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2313e-246">RELATED LINKS</span></span>


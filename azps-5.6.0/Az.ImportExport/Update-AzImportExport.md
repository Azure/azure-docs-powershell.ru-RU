---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: 7b604c22878d3d76e66a6d615deb1b46cedaad32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974931"
---
# <span data-ttu-id="8df49-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="8df49-101">Update-AzImportExport</span></span>

## <span data-ttu-id="8df49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df49-102">SYNOPSIS</span></span>
<span data-ttu-id="8df49-103">Обновляет свойства задания.</span><span class="sxs-lookup"><span data-stu-id="8df49-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="8df49-104">Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, включающие задание импорта или экспорта, отправлены в центр обработки данных Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8df49-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="8df49-105">Его также можно использовать для отмены существующего задания.</span><span class="sxs-lookup"><span data-stu-id="8df49-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="8df49-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8df49-106">SYNTAX</span></span>

### <span data-ttu-id="8df49-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8df49-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8df49-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8df49-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8df49-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8df49-109">DESCRIPTION</span></span>
<span data-ttu-id="8df49-110">Обновляет свойства задания.</span><span class="sxs-lookup"><span data-stu-id="8df49-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="8df49-111">Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, включающие задание импорта или экспорта, отправлены в центр обработки данных Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8df49-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="8df49-112">Его также можно использовать для отмены существующего задания.</span><span class="sxs-lookup"><span data-stu-id="8df49-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="8df49-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8df49-113">EXAMPLES</span></span>

### <span data-ttu-id="8df49-114">Пример 1. Обновление задания ImportExport по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="8df49-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="8df49-115">Этот cmdlet обновляет задание ImportExport по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="8df49-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="8df49-116">Пример 2. Обновление задания ImportExport по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="8df49-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="8df49-117">Этот cmdlet обновляет задание ImportExport по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="8df49-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="8df49-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8df49-118">PARAMETERS</span></span>

### <span data-ttu-id="8df49-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="8df49-119">-AcceptLanguage</span></span>
<span data-ttu-id="8df49-120">Указывает предпочтительный язык для ответа.</span><span class="sxs-lookup"><span data-stu-id="8df49-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="8df49-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="8df49-121">-BackupDriveManifest</span></span>
<span data-ttu-id="8df49-122">Указывает на то, следует ли копировать файлы манифеста на дисках, чтобы блокировать BLOB-файлы.</span><span class="sxs-lookup"><span data-stu-id="8df49-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="8df49-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="8df49-123">-CancelRequested</span></span>
<span data-ttu-id="8df49-124">При этом значение должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="8df49-124">If specified, the value must be true.</span></span>
<span data-ttu-id="8df49-125">Служба попытается отменить задание.</span><span class="sxs-lookup"><span data-stu-id="8df49-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="8df49-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df49-126">-DefaultProfile</span></span>
<span data-ttu-id="8df49-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8df49-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8df49-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="8df49-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="8df49-129">Название оператора, который используется для импорта или экспорта дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="8df49-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="8df49-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="8df49-131">Количество дисков, включенных в пакет.</span><span class="sxs-lookup"><span data-stu-id="8df49-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="8df49-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="8df49-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="8df49-133">Дата отгрузки пакета.</span><span class="sxs-lookup"><span data-stu-id="8df49-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="8df49-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="8df49-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="8df49-135">Номер для отслеживания пакета.</span><span class="sxs-lookup"><span data-stu-id="8df49-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="8df49-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="8df49-136">-DriveList</span></span>
<span data-ttu-id="8df49-137">Список дисков, которые включают в себя задание.</span><span class="sxs-lookup"><span data-stu-id="8df49-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="8df49-138">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств DRIVELIST и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8df49-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="8df49-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8df49-139">-InputObject</span></span>
<span data-ttu-id="8df49-140">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8df49-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8df49-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="8df49-141">-LogLevel</span></span>
<span data-ttu-id="8df49-142">Указывает, включено ли ведение журнала ошибок или подробное ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="8df49-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="8df49-143">-Name</span><span class="sxs-lookup"><span data-stu-id="8df49-143">-Name</span></span>
<span data-ttu-id="8df49-144">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="8df49-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df49-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df49-145">-ResourceGroupName</span></span>
<span data-ttu-id="8df49-146">Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="8df49-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df49-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="8df49-147">-ReturnAddressCity</span></span>
<span data-ttu-id="8df49-148">Название города, которое будет использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="8df49-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="8df49-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="8df49-150">Страна или регион, которые будут применяться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="8df49-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="8df49-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="8df49-152">Адрес электронной почты получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="8df49-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="8df49-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="8df49-154">Номер телефона получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="8df49-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="8df49-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="8df49-156">Почтовый индекс, который будет применяться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="8df49-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="8df49-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="8df49-158">Имя получателя, который получит жесткие диски при возврате.</span><span class="sxs-lookup"><span data-stu-id="8df49-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="8df49-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="8df49-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="8df49-160">Область или край, используемая при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="8df49-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="8df49-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="8df49-162">Первая строка адреса, используемого при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="8df49-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="8df49-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="8df49-164">Вторая строка адреса, используемого при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="8df49-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="8df49-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="8df49-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="8df49-166">Номер счета клиента у оператора связи.</span><span class="sxs-lookup"><span data-stu-id="8df49-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="8df49-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="8df49-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="8df49-168">Имя оператора связи.</span><span class="sxs-lookup"><span data-stu-id="8df49-168">The carrier's name.</span></span>

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

### <span data-ttu-id="8df49-169">-State</span><span class="sxs-lookup"><span data-stu-id="8df49-169">-State</span></span>
<span data-ttu-id="8df49-170">Если указано, значение должно иметь значение "Отправка", которое указывает службе импорта и экспорта, что пакет отправлен.</span><span class="sxs-lookup"><span data-stu-id="8df49-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="8df49-171">Свойства ReturnAddress и DeliveryPackage должны быть за настроены в этом запросе или в предыдущем запросе. В противном случае запрос не будет создан.</span><span class="sxs-lookup"><span data-stu-id="8df49-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="8df49-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8df49-172">-SubscriptionId</span></span>
<span data-ttu-id="8df49-173">ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="8df49-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df49-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="8df49-174">-Tag</span></span>
<span data-ttu-id="8df49-175">Определяет теги, которые будут назначены заданиям.</span><span class="sxs-lookup"><span data-stu-id="8df49-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df49-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8df49-176">-Confirm</span></span>
<span data-ttu-id="8df49-177">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8df49-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df49-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df49-178">-WhatIf</span></span>
<span data-ttu-id="8df49-179">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8df49-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df49-180">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8df49-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df49-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df49-181">CommonParameters</span></span>
<span data-ttu-id="8df49-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df49-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df49-183">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8df49-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df49-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8df49-184">INPUTS</span></span>

### <span data-ttu-id="8df49-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="8df49-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="8df49-186">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8df49-186">OUTPUTS</span></span>

### <span data-ttu-id="8df49-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="8df49-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="8df49-188">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8df49-188">NOTES</span></span>

<span data-ttu-id="8df49-189">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8df49-189">ALIASES</span></span>

<span data-ttu-id="8df49-190">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8df49-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8df49-191">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8df49-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8df49-192">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8df49-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8df49-193">DRIVELIST <IDriveStatus[]>: список дисков, которые входят в состав этой работы.</span><span class="sxs-lookup"><span data-stu-id="8df49-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="8df49-194">`[BitLockerKey <String>]`. Ключ BitLocker, используемый для шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="8df49-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="8df49-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span><span class="sxs-lookup"><span data-stu-id="8df49-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="8df49-196">`[CopyStatus <String>]`: подробное состояние процесса передачи данных.</span><span class="sxs-lookup"><span data-stu-id="8df49-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="8df49-197">Это поле не возвращается в ответе, пока диск не находится в состоянии переноса.</span><span class="sxs-lookup"><span data-stu-id="8df49-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="8df49-198">`[DriveHeaderHash <String>]`. Hash value the drive header (Hash value).</span><span class="sxs-lookup"><span data-stu-id="8df49-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="8df49-199">`[DriveId <String>]`: серийный номер диска без пробелов.</span><span class="sxs-lookup"><span data-stu-id="8df49-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="8df49-200">`[ErrorLogUri <String>]`: URI, который указывает на BLOB-проект, содержащий журнал ошибок для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="8df49-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="8df49-201">`[ManifestFile <String>]`: Относительный путь к файлу манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="8df49-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="8df49-202">`[ManifestHash <String>]`: Зашифрованный с кодом MD5(с кодом Base16) hash файла манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="8df49-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="8df49-203">`[ManifestUri <String>]`: URI, который указывает на BLOB-файл, содержащий файл манифеста диска.</span><span class="sxs-lookup"><span data-stu-id="8df49-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="8df49-204">`[PercentComplete <Int32?>]`: процентное завершения для диска.</span><span class="sxs-lookup"><span data-stu-id="8df49-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="8df49-205">`[State <DriveState?>]`. Текущее состояние диска.</span><span class="sxs-lookup"><span data-stu-id="8df49-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="8df49-206">`[VerboseLogUri <String>]`: URI, который указывает на BLOB-проект, содержащий подробный журнал для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="8df49-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="8df49-207">INPUTOBJECT <IImportExportIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8df49-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8df49-208">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8df49-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8df49-209">`[JobName <String>]`: имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="8df49-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="8df49-210">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="8df49-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="8df49-211">Например, "Запад США" или "запад".</span><span class="sxs-lookup"><span data-stu-id="8df49-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="8df49-212">`[ResourceGroupName <String>]`. Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="8df49-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="8df49-213">`[SubscriptionId <String>]`: ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="8df49-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="8df49-214">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8df49-214">RELATED LINKS</span></span>


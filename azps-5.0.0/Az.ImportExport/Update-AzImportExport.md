---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247799"
---
# <span data-ttu-id="be8b2-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="be8b2-101">Update-AzImportExport</span></span>

## <span data-ttu-id="be8b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="be8b2-103">Обновляет определенные свойства задания.</span><span class="sxs-lookup"><span data-stu-id="be8b2-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="be8b2-104">Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, содержащие задания импорта или экспорта, отправлены в центр обработки данных Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="be8b2-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="be8b2-105">Она также может использоваться для отмены существующего задания.</span><span class="sxs-lookup"><span data-stu-id="be8b2-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="be8b2-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be8b2-106">SYNTAX</span></span>

### <span data-ttu-id="be8b2-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be8b2-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="be8b2-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="be8b2-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="be8b2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be8b2-109">DESCRIPTION</span></span>
<span data-ttu-id="be8b2-110">Обновляет определенные свойства задания.</span><span class="sxs-lookup"><span data-stu-id="be8b2-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="be8b2-111">Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, содержащие задания импорта или экспорта, отправлены в центр обработки данных Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="be8b2-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="be8b2-112">Она также может использоваться для отмены существующего задания.</span><span class="sxs-lookup"><span data-stu-id="be8b2-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="be8b2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be8b2-113">EXAMPLES</span></span>

### <span data-ttu-id="be8b2-114">Пример 1: обновление задания ImportExport по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="be8b2-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="be8b2-115">Этот командлет обновляет ImportExport задание по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="be8b2-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="be8b2-116">Пример 2: обновление задания ImportExport по идентификационным данными.</span><span class="sxs-lookup"><span data-stu-id="be8b2-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="be8b2-117">Этот командлет обновляет ImportExport задание с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="be8b2-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="be8b2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be8b2-118">PARAMETERS</span></span>

### <span data-ttu-id="be8b2-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="be8b2-119">-AcceptLanguage</span></span>
<span data-ttu-id="be8b2-120">Указывает предпочтительный язык ответа.</span><span class="sxs-lookup"><span data-stu-id="be8b2-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="be8b2-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="be8b2-121">-BackupDriveManifest</span></span>
<span data-ttu-id="be8b2-122">Указывает, должны ли файлы манифестов на дисках быть скопированы в блоки больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="be8b2-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="be8b2-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="be8b2-123">-CancelRequested</span></span>
<span data-ttu-id="be8b2-124">Если задано значение, оно должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="be8b2-124">If specified, the value must be true.</span></span>
<span data-ttu-id="be8b2-125">Служба пытается отменить задание.</span><span class="sxs-lookup"><span data-stu-id="be8b2-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="be8b2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8b2-126">-DefaultProfile</span></span>
<span data-ttu-id="be8b2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be8b2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be8b2-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="be8b2-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="be8b2-129">Имя несущей частоты, используемой для отправки и импорта и экспорта дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="be8b2-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="be8b2-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="be8b2-131">Количество дисков, включенных в пакет.</span><span class="sxs-lookup"><span data-stu-id="be8b2-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="be8b2-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="be8b2-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="be8b2-133">Дата отгрузки пакета.</span><span class="sxs-lookup"><span data-stu-id="be8b2-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="be8b2-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="be8b2-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="be8b2-135">Номер отслеживания пакета.</span><span class="sxs-lookup"><span data-stu-id="be8b2-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="be8b2-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="be8b2-136">-DriveList</span></span>
<span data-ttu-id="be8b2-137">Список дисков, составляющих задание.</span><span class="sxs-lookup"><span data-stu-id="be8b2-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="be8b2-138">Для конструирования ознакомьтесь с разделом "Заметки" для свойств DRIVELIST и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="be8b2-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="be8b2-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be8b2-139">-InputObject</span></span>
<span data-ttu-id="be8b2-140">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="be8b2-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be8b2-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="be8b2-141">-LogLevel</span></span>
<span data-ttu-id="be8b2-142">Указывает, включено ли ведение журнала ошибок или подробный журнал.</span><span class="sxs-lookup"><span data-stu-id="be8b2-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="be8b2-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be8b2-143">-Name</span></span>
<span data-ttu-id="be8b2-144">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="be8b2-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="be8b2-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be8b2-145">-ResourceGroupName</span></span>
<span data-ttu-id="be8b2-146">Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="be8b2-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="be8b2-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="be8b2-147">-ReturnAddressCity</span></span>
<span data-ttu-id="be8b2-148">Название города, которое будет использоваться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="be8b2-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="be8b2-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="be8b2-150">Страна или регион, которые нужно использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="be8b2-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="be8b2-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="be8b2-152">Адрес электронной почты получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="be8b2-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="be8b2-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="be8b2-154">Номер телефона получателя возвращенных дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="be8b2-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="be8b2-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="be8b2-156">Почтовый индекс, который будет использоваться при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="be8b2-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="be8b2-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="be8b2-158">Имя получателя, который будет получать жесткие диски при их возвращении.</span><span class="sxs-lookup"><span data-stu-id="be8b2-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="be8b2-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="be8b2-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="be8b2-160">Область или край, которые нужно использовать при возврате дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="be8b2-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="be8b2-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="be8b2-162">Первая строка почтового адреса, который будет использоваться для возврата дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="be8b2-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="be8b2-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="be8b2-164">Вторая строка почтового адреса, который будет использоваться для возврата дисков.</span><span class="sxs-lookup"><span data-stu-id="be8b2-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="be8b2-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="be8b2-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="be8b2-166">Номер счета клиента с перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="be8b2-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="be8b2-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="be8b2-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="be8b2-168">Название несущей частоты.</span><span class="sxs-lookup"><span data-stu-id="be8b2-168">The carrier's name.</span></span>

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

### <span data-ttu-id="be8b2-169">-State</span><span class="sxs-lookup"><span data-stu-id="be8b2-169">-State</span></span>
<span data-ttu-id="be8b2-170">Если задано значение, оно должно быть доставлено, которое сообщает службе импорта и экспорта о том, что пакет для задания отгружен.</span><span class="sxs-lookup"><span data-stu-id="be8b2-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="be8b2-171">Свойства ReturnAddress и DeliveryPackage должны быть заданы либо в этом запросе, либо в предыдущем запросе, в противном случае запрос завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="be8b2-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="be8b2-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be8b2-172">-SubscriptionId</span></span>
<span data-ttu-id="be8b2-173">Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="be8b2-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="be8b2-174">-Тег</span><span class="sxs-lookup"><span data-stu-id="be8b2-174">-Tag</span></span>
<span data-ttu-id="be8b2-175">Указывает теги, которые будут назначены заданию</span><span class="sxs-lookup"><span data-stu-id="be8b2-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="be8b2-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be8b2-176">-Confirm</span></span>
<span data-ttu-id="be8b2-177">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be8b2-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be8b2-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be8b2-178">-WhatIf</span></span>
<span data-ttu-id="be8b2-179">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be8b2-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be8b2-180">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be8b2-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be8b2-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8b2-181">CommonParameters</span></span>
<span data-ttu-id="be8b2-182">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be8b2-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8b2-183">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be8b2-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8b2-184">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be8b2-184">INPUTS</span></span>

### <span data-ttu-id="be8b2-185">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="be8b2-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="be8b2-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be8b2-186">OUTPUTS</span></span>

### <span data-ttu-id="be8b2-187">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="be8b2-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="be8b2-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="be8b2-188">NOTES</span></span>

<span data-ttu-id="be8b2-189">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="be8b2-189">ALIASES</span></span>

<span data-ttu-id="be8b2-190">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="be8b2-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be8b2-191">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be8b2-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be8b2-192">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be8b2-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be8b2-193">DRIVELIST <IDriveStatus [] >: список дисков, составляющих задание.</span><span class="sxs-lookup"><span data-stu-id="be8b2-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="be8b2-194">`[BitLockerKey <String>]`: Ключ BitLocker, используемый для шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="be8b2-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="be8b2-195">`[BytesSucceeded <Int64?>]`: Байты успешно переданы на диск.</span><span class="sxs-lookup"><span data-stu-id="be8b2-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="be8b2-196">`[CopyStatus <String>]`: Подробные сведения о состоянии процесса передачи данных.</span><span class="sxs-lookup"><span data-stu-id="be8b2-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="be8b2-197">Это поле не возвращается в ответе до тех пор, пока диск не находится в состоянии перепередачи.</span><span class="sxs-lookup"><span data-stu-id="be8b2-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="be8b2-198">`[DriveHeaderHash <String>]`: Хэш-значение заголовка диска.</span><span class="sxs-lookup"><span data-stu-id="be8b2-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="be8b2-199">`[DriveId <String>]`: Серийный номер оборудования диска без пробелов.</span><span class="sxs-lookup"><span data-stu-id="be8b2-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="be8b2-200">`[ErrorLogUri <String>]`: URI, указывающий на большой двоичный объект, который содержит журнал ошибок для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="be8b2-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="be8b2-201">`[ManifestFile <String>]`: Относительный путь к файлу манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="be8b2-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="be8b2-202">`[ManifestHash <String>]`: Хэш MD5, закодированный Base16, для файла манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="be8b2-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="be8b2-203">`[ManifestUri <String>]`: URI, указывающий на большой двоичный объект, содержащий файл манифеста диска.</span><span class="sxs-lookup"><span data-stu-id="be8b2-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="be8b2-204">`[PercentComplete <Int32?>]`: Процент завершения для диска.</span><span class="sxs-lookup"><span data-stu-id="be8b2-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="be8b2-205">`[State <DriveState?>]`: Текущее состояние диска.</span><span class="sxs-lookup"><span data-stu-id="be8b2-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="be8b2-206">`[VerboseLogUri <String>]`: URI, указывающий на большой двоичный объект, содержащий подробный журнал для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="be8b2-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="be8b2-207">INPUTOBJECT <IImportExportIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="be8b2-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be8b2-208">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="be8b2-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be8b2-209">`[JobName <String>]`: Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="be8b2-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="be8b2-210">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="be8b2-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="be8b2-211">Например, "Западная США" или "westus".</span><span class="sxs-lookup"><span data-stu-id="be8b2-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="be8b2-212">`[ResourceGroupName <String>]`: Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="be8b2-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="be8b2-213">`[SubscriptionId <String>]`: Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="be8b2-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="be8b2-214">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be8b2-214">RELATED LINKS</span></span>


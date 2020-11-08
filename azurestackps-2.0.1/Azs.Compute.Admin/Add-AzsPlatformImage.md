---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075342"
---
# <span data-ttu-id="2ba17-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="2ba17-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="2ba17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ba17-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba17-103">Создает новый образ платформы с заданными издателем, предложением, SKU и версией.</span><span class="sxs-lookup"><span data-stu-id="2ba17-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="2ba17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ba17-104">SYNTAX</span></span>

### <span data-ttu-id="2ba17-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ba17-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ba17-106">Заново</span><span class="sxs-lookup"><span data-stu-id="2ba17-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ba17-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ba17-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ba17-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2ba17-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ba17-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ba17-109">DESCRIPTION</span></span>
<span data-ttu-id="2ba17-110">Создает новый образ платформы с заданными издателем, предложением, SKU и версией.</span><span class="sxs-lookup"><span data-stu-id="2ba17-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="2ba17-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ba17-111">EXAMPLES</span></span>

### <span data-ttu-id="2ba17-112">Пример 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="2ba17-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="2ba17-113">Добавьте изображение платформы из хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="2ba17-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="2ba17-114">С помощью SasUri можно указать расположение PlatformImage или использовать общедоступный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2ba17-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="2ba17-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ba17-115">PARAMETERS</span></span>

### <span data-ttu-id="2ba17-116">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="2ba17-116">Exception.Message</span></span>
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

### <span data-ttu-id="2ba17-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="2ba17-117">-BillingPartNumber</span></span>
<span data-ttu-id="2ba17-118">Номер детали используется для выставления счетов за программные расходы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-119">-Диски</span><span class="sxs-lookup"><span data-stu-id="2ba17-119">-DataDisks</span></span>
<span data-ttu-id="2ba17-120">Диски данных, используемые образом платформы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="2ba17-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств "диски" и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="2ba17-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba17-122">-DefaultProfile</span></span>
<span data-ttu-id="2ba17-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba17-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ba17-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba17-124">-InputObject</span></span>
<span data-ttu-id="2ba17-125">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="2ba17-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-126">-Location</span><span class="sxs-lookup"><span data-stu-id="2ba17-126">-Location</span></span>
<span data-ttu-id="2ba17-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ba17-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="2ba17-128">-NewImage</span></span>
<span data-ttu-id="2ba17-129">Параметры, используемые для создания нового образа платформы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="2ba17-130">Для конструирования ознакомьтесь с разделом "Заметки" для свойств NEWIMAGE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="2ba17-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-131">-Wait</span><span class="sxs-lookup"><span data-stu-id="2ba17-131">-NoWait</span></span>
<span data-ttu-id="2ba17-132">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="2ba17-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ba17-133">-Предложение</span><span class="sxs-lookup"><span data-stu-id="2ba17-133">-Offer</span></span>
<span data-ttu-id="2ba17-134">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="2ba17-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="2ba17-135">-OsType</span></span>
<span data-ttu-id="2ba17-136">Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="2ba17-137">-OsUri</span></span>
<span data-ttu-id="2ba17-138">Расположение диска.</span><span class="sxs-lookup"><span data-stu-id="2ba17-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="2ba17-139">-ProvisioningState</span></span>
<span data-ttu-id="2ba17-140">Состояние подготовки образа платформы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2ba17-141">-Publisher</span></span>
<span data-ttu-id="2ba17-142">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="2ba17-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ba17-143">-Sku</span></span>
<span data-ttu-id="2ba17-144">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="2ba17-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ba17-145">-SubscriptionId</span></span>
<span data-ttu-id="2ba17-146">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba17-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ba17-147">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-148">-Version</span><span class="sxs-lookup"><span data-stu-id="2ba17-148">-Version</span></span>
<span data-ttu-id="2ba17-149">Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ba17-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ba17-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ba17-150">-Confirm</span></span>
<span data-ttu-id="2ba17-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ba17-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba17-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba17-152">-WhatIf</span></span>
<span data-ttu-id="2ba17-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ba17-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba17-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ba17-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="2ba17-155">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="2ba17-155">Exception.Message</span></span>

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

### <span data-ttu-id="2ba17-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba17-156">CommonParameters</span></span>
<span data-ttu-id="2ba17-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ba17-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba17-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ba17-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba17-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ba17-159">INPUTS</span></span>

### <span data-ttu-id="2ba17-160">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20151201Preview. IPlatformImageParameters</span><span class="sxs-lookup"><span data-stu-id="2ba17-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="2ba17-161">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2ba17-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="2ba17-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ba17-162">OUTPUTS</span></span>

### <span data-ttu-id="2ba17-163">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="2ba17-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="2ba17-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ba17-164">NOTES</span></span>

<span data-ttu-id="2ba17-165">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2ba17-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ba17-166">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ba17-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2ba17-167">ДИСКИ с данными <IDataDisk [] >: диски данных, используемые образом платформы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="2ba17-168">`[Lun <Int32?>]`: Логический номер устройства.</span><span class="sxs-lookup"><span data-stu-id="2ba17-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="2ba17-169">`[Uri <String>]`: Расположение шаблона диска.</span><span class="sxs-lookup"><span data-stu-id="2ba17-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="2ba17-170">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="2ba17-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ba17-171">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="2ba17-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="2ba17-172">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="2ba17-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ba17-173">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ba17-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2ba17-174">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="2ba17-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="2ba17-175">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="2ba17-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="2ba17-176">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="2ba17-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="2ba17-177">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="2ba17-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2ba17-178">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="2ba17-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="2ba17-179">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba17-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2ba17-180">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2ba17-181">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="2ba17-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="2ba17-182">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ba17-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="2ba17-183">NEWIMAGE <IPlatformImageParameters> : параметры, используемые для создания нового образа платформы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="2ba17-184">`[DataDisk <IDataDisk[]>]`: Диски данных, используемые образом платформы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="2ba17-185">`[Lun <Int32?>]`: Логический номер устройства.</span><span class="sxs-lookup"><span data-stu-id="2ba17-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="2ba17-186">`[Uri <String>]`: Расположение шаблона диска.</span><span class="sxs-lookup"><span data-stu-id="2ba17-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="2ba17-187">`[DetailBillingPartNumber <String>]`: Номер детали используется для выставления счетов за программные расходы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="2ba17-188">`[OSDiskOstype <OSType?>]`: Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="2ba17-189">`[OSDiskUri <String>]`: Расположение диска.</span><span class="sxs-lookup"><span data-stu-id="2ba17-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="2ba17-190">`[ProvisioningState <ProvisioningState?>]`: Состояние подготовки образа платформы.</span><span class="sxs-lookup"><span data-stu-id="2ba17-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="2ba17-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ba17-191">RELATED LINKS</span></span>


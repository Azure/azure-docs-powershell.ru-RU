---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075341"
---
# <span data-ttu-id="c9a60-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="c9a60-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="c9a60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9a60-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a60-103">Создание изображения расширения виртуальной машины с помощью Publisher, версия.</span><span class="sxs-lookup"><span data-stu-id="c9a60-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="c9a60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9a60-104">SYNTAX</span></span>

### <span data-ttu-id="c9a60-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9a60-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c9a60-106">Заново</span><span class="sxs-lookup"><span data-stu-id="c9a60-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c9a60-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9a60-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c9a60-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c9a60-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c9a60-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9a60-109">DESCRIPTION</span></span>
<span data-ttu-id="c9a60-110">Создание изображения расширения виртуальной машины с помощью Publisher, версия.</span><span class="sxs-lookup"><span data-stu-id="c9a60-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="c9a60-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9a60-111">EXAMPLES</span></span>

### <span data-ttu-id="c9a60-112">Пример 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="c9a60-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="c9a60-113">Используйте общедоступную ссылку, чтобы указать расположение расширения или URI для блоба Azure с помощью SasUri.</span><span class="sxs-lookup"><span data-stu-id="c9a60-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="c9a60-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9a60-114">PARAMETERS</span></span>

### <span data-ttu-id="c9a60-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="c9a60-115">-ComputeRole</span></span>
<span data-ttu-id="c9a60-116">Вычислительная роль</span><span class="sxs-lookup"><span data-stu-id="c9a60-116">Compute role</span></span>

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

### <span data-ttu-id="c9a60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a60-117">-DefaultProfile</span></span>
<span data-ttu-id="c9a60-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a60-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a60-119">-Расширение</span><span class="sxs-lookup"><span data-stu-id="c9a60-119">-Extension</span></span>
<span data-ttu-id="c9a60-120">Параметры, используемые для создания нового образа расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c9a60-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="c9a60-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств расширения и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c9a60-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c9a60-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9a60-122">-InputObject</span></span>
<span data-ttu-id="c9a60-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c9a60-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9a60-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="c9a60-124">-IsSystemExtension</span></span>
<span data-ttu-id="c9a60-125">Указывает, является ли расширение для системы.</span><span class="sxs-lookup"><span data-stu-id="c9a60-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c9a60-126">-Location</span><span class="sxs-lookup"><span data-stu-id="c9a60-126">-Location</span></span>
<span data-ttu-id="c9a60-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9a60-127">Location of the resource.</span></span>

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

### <span data-ttu-id="c9a60-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="c9a60-128">-PropertiesPublisher</span></span>
<span data-ttu-id="c9a60-129">Издатель расширения ВМ</span><span class="sxs-lookup"><span data-stu-id="c9a60-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c9a60-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="c9a60-130">-ProvisioningState</span></span>
<span data-ttu-id="c9a60-131">Состояние подготовки расширения.</span><span class="sxs-lookup"><span data-stu-id="c9a60-131">Provisioning state of extension.</span></span>

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

### <span data-ttu-id="c9a60-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c9a60-132">-Publisher</span></span>
<span data-ttu-id="c9a60-133">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="c9a60-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c9a60-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="c9a60-134">-SourceBlob</span></span>
<span data-ttu-id="c9a60-135">Универсальный код ресурса (URI) для Azure или AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c9a60-135">URI to Azure or AzureStack blob.</span></span>

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

### <span data-ttu-id="c9a60-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9a60-136">-SubscriptionId</span></span>
<span data-ttu-id="c9a60-137">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a60-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c9a60-138">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c9a60-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c9a60-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="c9a60-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="c9a60-140">Значение true, если поддерживается несколько расширений.</span><span class="sxs-lookup"><span data-stu-id="c9a60-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c9a60-141">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="c9a60-141">-Type</span></span>
<span data-ttu-id="c9a60-142">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="c9a60-142">Type of extension.</span></span>

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

### <span data-ttu-id="c9a60-143">-Version</span><span class="sxs-lookup"><span data-stu-id="c9a60-143">-Version</span></span>
<span data-ttu-id="c9a60-144">Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9a60-144">The version of the resource.</span></span>

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

### <span data-ttu-id="c9a60-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="c9a60-145">-VmOsType</span></span>
<span data-ttu-id="c9a60-146">Целевой тип операционной системы для виртуальной машины, необходимый для развертывания обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="c9a60-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="c9a60-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="c9a60-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="c9a60-148">Значение, указывающее на то, включено ли расширение для поддержки установки масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c9a60-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c9a60-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9a60-149">-Confirm</span></span>
<span data-ttu-id="c9a60-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9a60-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a60-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a60-151">-WhatIf</span></span>
<span data-ttu-id="c9a60-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9a60-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9a60-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9a60-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a60-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a60-154">CommonParameters</span></span>
<span data-ttu-id="c9a60-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9a60-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a60-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9a60-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a60-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9a60-157">INPUTS</span></span>

### <span data-ttu-id="c9a60-158">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20151201Preview. IVMExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="c9a60-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="c9a60-159">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c9a60-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="c9a60-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9a60-160">OUTPUTS</span></span>

### <span data-ttu-id="c9a60-161">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="c9a60-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="c9a60-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9a60-162">NOTES</span></span>

<span data-ttu-id="c9a60-163">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c9a60-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9a60-164">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9a60-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c9a60-165">РАСШИРЕНИЕ <IVMExtensionParameters> : параметры, используемые для создания нового образа расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c9a60-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="c9a60-166">`[ComputeRole <String>]`: COMPUTE Role (роль)</span><span class="sxs-lookup"><span data-stu-id="c9a60-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="c9a60-167">`[IsSystemExtension <Boolean?>]`: Указывает, является ли расширение для системы.</span><span class="sxs-lookup"><span data-stu-id="c9a60-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="c9a60-168">`[ProvisioningState <ProvisioningState?>]`: Состояние подготовки расширения.</span><span class="sxs-lookup"><span data-stu-id="c9a60-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="c9a60-169">`[Publisher <String>]`: Издатель расширения ВМ</span><span class="sxs-lookup"><span data-stu-id="c9a60-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="c9a60-170">`[SourceBlobUri <String>]`: URI в Azure или AzureStack BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="c9a60-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="c9a60-171">`[SupportMultipleExtension <Boolean?>]`: Значение true, если поддерживается несколько расширений.</span><span class="sxs-lookup"><span data-stu-id="c9a60-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="c9a60-172">`[VMScaleSetEnabled <Boolean?>]`: Значение, показывающее, включено ли расширение для поддержки настройки масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c9a60-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="c9a60-173">`[VmosType <OSType?>]`: Целевой тип операционной системы для виртуальной машины, необходимый для развертывания обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="c9a60-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="c9a60-174">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c9a60-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9a60-175">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="c9a60-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="c9a60-176">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c9a60-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9a60-177">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9a60-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c9a60-178">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="c9a60-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="c9a60-179">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="c9a60-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c9a60-180">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="c9a60-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="c9a60-181">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="c9a60-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c9a60-182">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="c9a60-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="c9a60-183">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a60-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c9a60-184">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c9a60-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c9a60-185">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="c9a60-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="c9a60-186">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9a60-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="c9a60-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9a60-187">RELATED LINKS</span></span>


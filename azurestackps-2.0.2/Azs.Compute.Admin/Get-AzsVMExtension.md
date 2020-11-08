---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076731"
---
# <span data-ttu-id="d731f-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="d731f-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="d731f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d731f-102">SYNOPSIS</span></span>
<span data-ttu-id="d731f-103">Возвращает запрашиваемое изображение расширения виртуальной машины издателя, тип, версия.</span><span class="sxs-lookup"><span data-stu-id="d731f-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="d731f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d731f-104">SYNTAX</span></span>

### <span data-ttu-id="d731f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d731f-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d731f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d731f-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d731f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d731f-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d731f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d731f-108">DESCRIPTION</span></span>
<span data-ttu-id="d731f-109">Возвращает запрашиваемое изображение расширения виртуальной машины издателя, тип, версия.</span><span class="sxs-lookup"><span data-stu-id="d731f-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="d731f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d731f-110">EXAMPLES</span></span>

### <span data-ttu-id="d731f-111">Пример 1: получение всех расширений ВМ</span><span class="sxs-lookup"><span data-stu-id="d731f-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="d731f-112">Получите список всех VMExtensions, оставив все параметры пустыми.</span><span class="sxs-lookup"><span data-stu-id="d731f-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="d731f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d731f-113">PARAMETERS</span></span>

### <span data-ttu-id="d731f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d731f-114">-DefaultProfile</span></span>
<span data-ttu-id="d731f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d731f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d731f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d731f-116">-InputObject</span></span>
<span data-ttu-id="d731f-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d731f-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d731f-118">-Location</span><span class="sxs-lookup"><span data-stu-id="d731f-118">-Location</span></span>
<span data-ttu-id="d731f-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d731f-119">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d731f-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d731f-120">-Publisher</span></span>
<span data-ttu-id="d731f-121">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="d731f-121">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d731f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d731f-122">-SubscriptionId</span></span>
<span data-ttu-id="d731f-123">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d731f-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d731f-124">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d731f-124">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d731f-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="d731f-125">-Type</span></span>
<span data-ttu-id="d731f-126">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="d731f-126">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d731f-127">-Version</span><span class="sxs-lookup"><span data-stu-id="d731f-127">-Version</span></span>
<span data-ttu-id="d731f-128">Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="d731f-128">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d731f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d731f-129">CommonParameters</span></span>
<span data-ttu-id="d731f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d731f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d731f-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d731f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d731f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d731f-132">INPUTS</span></span>

### <span data-ttu-id="d731f-133">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d731f-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="d731f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d731f-134">OUTPUTS</span></span>

### <span data-ttu-id="d731f-135">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="d731f-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="d731f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d731f-136">NOTES</span></span>

<span data-ttu-id="d731f-137">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d731f-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d731f-138">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d731f-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d731f-139">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d731f-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d731f-140">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="d731f-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="d731f-141">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d731f-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d731f-142">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d731f-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d731f-143">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="d731f-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="d731f-144">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="d731f-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="d731f-145">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="d731f-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="d731f-146">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="d731f-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d731f-147">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="d731f-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="d731f-148">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d731f-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d731f-149">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d731f-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d731f-150">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="d731f-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="d731f-151">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="d731f-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="d731f-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d731f-152">RELATED LINKS</span></span>


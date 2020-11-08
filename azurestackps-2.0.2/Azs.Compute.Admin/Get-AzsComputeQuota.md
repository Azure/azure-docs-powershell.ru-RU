---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076691"
---
# <span data-ttu-id="76a8a-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="76a8a-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="76a8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="76a8a-103">Получить существующую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="76a8a-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="76a8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76a8a-104">SYNTAX</span></span>

### <span data-ttu-id="76a8a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76a8a-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="76a8a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="76a8a-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76a8a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76a8a-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="76a8a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a8a-108">DESCRIPTION</span></span>
<span data-ttu-id="76a8a-109">Получить существующую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="76a8a-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="76a8a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76a8a-110">EXAMPLES</span></span>

### <span data-ttu-id="76a8a-111">Пример 1: получение всех расчетных квот</span><span class="sxs-lookup"><span data-stu-id="76a8a-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="76a8a-112">Выполняйте без `Get-AzsComputeQuota` параметров, чтобы получить список всех расчетных квот.</span><span class="sxs-lookup"><span data-stu-id="76a8a-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="76a8a-113">Пример 2: получение вычислительной квоты по имени</span><span class="sxs-lookup"><span data-stu-id="76a8a-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="76a8a-114">Укажите имя квоты в командной строке, чтобы получить определенную квоту.</span><span class="sxs-lookup"><span data-stu-id="76a8a-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="76a8a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76a8a-115">PARAMETERS</span></span>

### <span data-ttu-id="76a8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a8a-116">-DefaultProfile</span></span>
<span data-ttu-id="76a8a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76a8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a8a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76a8a-118">-InputObject</span></span>
<span data-ttu-id="76a8a-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="76a8a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76a8a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="76a8a-120">-Location</span></span>
<span data-ttu-id="76a8a-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="76a8a-121">Location of the resource.</span></span>

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

### <span data-ttu-id="76a8a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76a8a-122">-Name</span></span>
<span data-ttu-id="76a8a-123">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="76a8a-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76a8a-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76a8a-124">-SubscriptionId</span></span>
<span data-ttu-id="76a8a-125">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="76a8a-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76a8a-126">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="76a8a-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="76a8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a8a-127">CommonParameters</span></span>
<span data-ttu-id="76a8a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76a8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a8a-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76a8a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a8a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76a8a-130">INPUTS</span></span>

### <span data-ttu-id="76a8a-131">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="76a8a-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="76a8a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a8a-132">OUTPUTS</span></span>

### <span data-ttu-id="76a8a-133">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="76a8a-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="76a8a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="76a8a-134">NOTES</span></span>

<span data-ttu-id="76a8a-135">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="76a8a-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76a8a-136">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76a8a-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="76a8a-137">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="76a8a-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76a8a-138">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="76a8a-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="76a8a-139">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="76a8a-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76a8a-140">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="76a8a-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="76a8a-141">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="76a8a-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="76a8a-142">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="76a8a-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="76a8a-143">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="76a8a-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="76a8a-144">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="76a8a-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="76a8a-145">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="76a8a-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="76a8a-146">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="76a8a-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76a8a-147">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="76a8a-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="76a8a-148">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="76a8a-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="76a8a-149">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="76a8a-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="76a8a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76a8a-150">RELATED LINKS</span></span>


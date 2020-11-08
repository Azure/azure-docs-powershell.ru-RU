---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077075"
---
# <span data-ttu-id="9cce3-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="9cce3-101">Get-AzsDisk</span></span>

## <span data-ttu-id="9cce3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cce3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cce3-103">Возвращает диск.</span><span class="sxs-lookup"><span data-stu-id="9cce3-103">Returns the disk.</span></span>

## <span data-ttu-id="9cce3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cce3-104">SYNTAX</span></span>

### <span data-ttu-id="9cce3-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9cce3-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9cce3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="9cce3-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9cce3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9cce3-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9cce3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cce3-108">DESCRIPTION</span></span>
<span data-ttu-id="9cce3-109">Возвращает диск.</span><span class="sxs-lookup"><span data-stu-id="9cce3-109">Returns the disk.</span></span>

## <span data-ttu-id="9cce3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cce3-110">EXAMPLES</span></span>

### <span data-ttu-id="9cce3-111">Пример 1: получение всех дисков</span><span class="sxs-lookup"><span data-stu-id="9cce3-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="9cce3-112">При отсутствии каких бы то ни было параметров, `Get-AzsDisk` будут перечислены все диски.</span><span class="sxs-lookup"><span data-stu-id="9cce3-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="9cce3-113">Пример 2: получение дискового имени</span><span class="sxs-lookup"><span data-stu-id="9cce3-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="9cce3-114">Укажите диск, `Name` который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="9cce3-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="9cce3-115">Пример 3: получение указанного количества дисков</span><span class="sxs-lookup"><span data-stu-id="9cce3-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="9cce3-116">Используйте этот `Count` параметр для получения определенного количества дисков.</span><span class="sxs-lookup"><span data-stu-id="9cce3-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="9cce3-117">Пример 4: получение всех дисков в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="9cce3-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="9cce3-118">Использование `ScaleUnit` параметра или `VolumeLabel` для перечисления всех дисков в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="9cce3-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="9cce3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cce3-119">PARAMETERS</span></span>

### <span data-ttu-id="9cce3-120">— Количество</span><span class="sxs-lookup"><span data-stu-id="9cce3-120">-Count</span></span>
<span data-ttu-id="9cce3-121">Максимальное количество возвращаемых дисков.</span><span class="sxs-lookup"><span data-stu-id="9cce3-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cce3-122">-DefaultProfile</span></span>
<span data-ttu-id="9cce3-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cce3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cce3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cce3-124">-InputObject</span></span>
<span data-ttu-id="9cce3-125">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9cce3-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9cce3-126">-Location</span><span class="sxs-lookup"><span data-stu-id="9cce3-126">-Location</span></span>
<span data-ttu-id="9cce3-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9cce3-127">Location of the resource.</span></span>

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

### <span data-ttu-id="9cce3-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9cce3-128">-Name</span></span>
<span data-ttu-id="9cce3-129">Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="9cce3-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="9cce3-130">-ScaleUnit</span></span>
<span data-ttu-id="9cce3-131">Единица масштабирования, к которой относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="9cce3-131">The scale unit which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="9cce3-132">-SharePath</span></span>
<span data-ttu-id="9cce3-133">Общий доступ, к которому относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="9cce3-133">The share which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-134">-Start</span><span class="sxs-lookup"><span data-stu-id="9cce3-134">-Start</span></span>
<span data-ttu-id="9cce3-135">Начальный индекс дисков в запросе.</span><span class="sxs-lookup"><span data-stu-id="9cce3-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-136">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="9cce3-136">-Status</span></span>
<span data-ttu-id="9cce3-137">Параметры состояния диска.</span><span class="sxs-lookup"><span data-stu-id="9cce3-137">The parameters of disk state.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cce3-138">-SubscriptionId</span></span>
<span data-ttu-id="9cce3-139">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9cce3-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9cce3-140">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9cce3-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9cce3-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cce3-141">-UserSubscriptionId</span></span>
<span data-ttu-id="9cce3-142">Идентификатор подписки пользователя, которому принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="9cce3-142">User Subscription Id which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="9cce3-143">-VolumeLabel</span></span>
<span data-ttu-id="9cce3-144">Метка тома, к которому относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="9cce3-144">The volume label of the volume which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cce3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cce3-145">CommonParameters</span></span>
<span data-ttu-id="9cce3-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cce3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cce3-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cce3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cce3-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cce3-148">INPUTS</span></span>

### <span data-ttu-id="9cce3-149">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9cce3-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="9cce3-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cce3-150">OUTPUTS</span></span>

### <span data-ttu-id="9cce3-151">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180730Preview. IDisk</span><span class="sxs-lookup"><span data-stu-id="9cce3-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="9cce3-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cce3-152">NOTES</span></span>

<span data-ttu-id="9cce3-153">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9cce3-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cce3-154">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9cce3-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9cce3-155">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9cce3-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cce3-156">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="9cce3-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="9cce3-157">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9cce3-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cce3-158">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9cce3-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9cce3-159">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="9cce3-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="9cce3-160">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="9cce3-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="9cce3-161">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="9cce3-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="9cce3-162">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="9cce3-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9cce3-163">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="9cce3-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="9cce3-164">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9cce3-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9cce3-165">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9cce3-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9cce3-166">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="9cce3-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="9cce3-167">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="9cce3-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="9cce3-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cce3-168">RELATED LINKS</span></span>

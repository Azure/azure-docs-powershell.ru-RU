---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911671"
---
# <span data-ttu-id="c8e8c-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="c8e8c-101">Get-AzsDisk</span></span>

## <span data-ttu-id="c8e8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e8c-103">Возвращает диск.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-103">Returns the disk.</span></span>

## <span data-ttu-id="c8e8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8e8c-104">SYNTAX</span></span>

### <span data-ttu-id="c8e8c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8e8c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c8e8c-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8e8c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8e8c-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c8e8c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8e8c-108">DESCRIPTION</span></span>
<span data-ttu-id="c8e8c-109">Возвращает диск.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-109">Returns the disk.</span></span>

## <span data-ttu-id="c8e8c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8e8c-110">EXAMPLES</span></span>

### <span data-ttu-id="c8e8c-111">Пример 1: получение всех дисков</span><span class="sxs-lookup"><span data-stu-id="c8e8c-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="c8e8c-112">При отсутствии каких бы то ни было параметров, `Get-AzsDisk` будут перечислены все диски.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="c8e8c-113">Пример 2: получение дискового имени</span><span class="sxs-lookup"><span data-stu-id="c8e8c-113">Example 2: Get a Disk by Name</span></span>
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

<span data-ttu-id="c8e8c-114">Укажите диск, `Name` который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="c8e8c-115">Пример 3: получение указанного количества дисков</span><span class="sxs-lookup"><span data-stu-id="c8e8c-115">Example 3: Get a Specified number of Disks</span></span>
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

<span data-ttu-id="c8e8c-116">Используйте этот `Count` параметр для получения определенного количества дисков.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="c8e8c-117">Пример 4: получение всех дисков в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="c8e8c-117">Example 4: Get all disks in specific location</span></span>
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

<span data-ttu-id="c8e8c-118">Использование `ScaleUnit` параметра или `VolumeLabel` для перечисления всех дисков в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="c8e8c-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="c8e8c-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8e8c-119">PARAMETERS</span></span>

### <span data-ttu-id="c8e8c-120">— Количество</span><span class="sxs-lookup"><span data-stu-id="c8e8c-120">-Count</span></span>
<span data-ttu-id="c8e8c-121">Максимальное количество возвращаемых дисков.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-121">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="c8e8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e8c-122">-DefaultProfile</span></span>
<span data-ttu-id="c8e8c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8e8c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8e8c-124">-InputObject</span></span>
<span data-ttu-id="c8e8c-125">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8e8c-126">-Location</span><span class="sxs-lookup"><span data-stu-id="c8e8c-126">-Location</span></span>
<span data-ttu-id="c8e8c-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-127">Location of the resource.</span></span>

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

### <span data-ttu-id="c8e8c-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-128">-Name</span></span>
<span data-ttu-id="c8e8c-129">Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-129">The disk guid as identity.</span></span>

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

### <span data-ttu-id="c8e8c-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c8e8c-130">-ScaleUnit</span></span>
<span data-ttu-id="c8e8c-131">Единица масштабирования, к которой относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="c8e8c-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="c8e8c-132">-SharePath</span></span>
<span data-ttu-id="c8e8c-133">Общий доступ, к которому относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="c8e8c-134">-Start</span><span class="sxs-lookup"><span data-stu-id="c8e8c-134">-Start</span></span>
<span data-ttu-id="c8e8c-135">Начальный индекс дисков в запросе.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-135">The start index of disks in query.</span></span>

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

### <span data-ttu-id="c8e8c-136">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-136">-Status</span></span>
<span data-ttu-id="c8e8c-137">Параметры состояния диска.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="c8e8c-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8e8c-138">-SubscriptionId</span></span>
<span data-ttu-id="c8e8c-139">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c8e8c-140">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c8e8c-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8e8c-141">-UserSubscriptionId</span></span>
<span data-ttu-id="c8e8c-142">Идентификатор подписки пользователя, которому принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="c8e8c-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="c8e8c-143">-VolumeLabel</span></span>
<span data-ttu-id="c8e8c-144">Метка тома, к которому относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="c8e8c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e8c-145">CommonParameters</span></span>
<span data-ttu-id="c8e8c-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e8c-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8e8c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e8c-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8e8c-148">INPUTS</span></span>

### <span data-ttu-id="c8e8c-149">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c8e8c-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="c8e8c-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8e8c-150">OUTPUTS</span></span>

### <span data-ttu-id="c8e8c-151">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180730Preview. IDisk</span><span class="sxs-lookup"><span data-stu-id="c8e8c-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="c8e8c-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8e8c-152">NOTES</span></span>

<span data-ttu-id="c8e8c-153">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8e8c-154">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c8e8c-155">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c8e8c-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8e8c-156">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="c8e8c-157">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c8e8c-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8e8c-158">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c8e8c-159">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="c8e8c-160">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c8e8c-161">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="c8e8c-162">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c8e8c-163">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="c8e8c-164">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c8e8c-165">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c8e8c-166">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="c8e8c-167">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="c8e8c-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8e8c-168">RELATED LINKS</span></span>


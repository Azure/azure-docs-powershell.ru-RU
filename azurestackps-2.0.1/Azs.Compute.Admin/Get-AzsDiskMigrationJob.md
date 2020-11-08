---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075275"
---
# <span data-ttu-id="c117a-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="c117a-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="c117a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c117a-102">SYNOPSIS</span></span>
<span data-ttu-id="c117a-103">Возвращает запрошенное задание миграции диска.</span><span class="sxs-lookup"><span data-stu-id="c117a-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="c117a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c117a-104">SYNTAX</span></span>

### <span data-ttu-id="c117a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c117a-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c117a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c117a-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c117a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c117a-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c117a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c117a-108">DESCRIPTION</span></span>
<span data-ttu-id="c117a-109">Возвращает запрошенное задание миграции диска.</span><span class="sxs-lookup"><span data-stu-id="c117a-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="c117a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c117a-110">EXAMPLES</span></span>

### <span data-ttu-id="c117a-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="c117a-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="c117a-112">Возвращает список управляемых заданий миграции дисков на локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="c117a-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="c117a-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="c117a-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="c117a-114">Получение определенного задания миграции управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c117a-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="c117a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c117a-115">PARAMETERS</span></span>

### <span data-ttu-id="c117a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c117a-116">-DefaultProfile</span></span>
<span data-ttu-id="c117a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c117a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c117a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c117a-118">-InputObject</span></span>
<span data-ttu-id="c117a-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c117a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c117a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c117a-120">-Location</span></span>
<span data-ttu-id="c117a-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c117a-121">Location of the resource.</span></span>

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

### <span data-ttu-id="c117a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c117a-122">-Name</span></span>
<span data-ttu-id="c117a-123">Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="c117a-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c117a-124">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c117a-124">-Status</span></span>
<span data-ttu-id="c117a-125">Параметры состояния задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="c117a-125">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="c117a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c117a-126">-SubscriptionId</span></span>
<span data-ttu-id="c117a-127">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c117a-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c117a-128">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c117a-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c117a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c117a-129">CommonParameters</span></span>
<span data-ttu-id="c117a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c117a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c117a-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c117a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c117a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c117a-132">INPUTS</span></span>

### <span data-ttu-id="c117a-133">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c117a-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="c117a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c117a-134">OUTPUTS</span></span>

### <span data-ttu-id="c117a-135">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="c117a-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="c117a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c117a-136">NOTES</span></span>

<span data-ttu-id="c117a-137">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c117a-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c117a-138">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c117a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c117a-139">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c117a-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c117a-140">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="c117a-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="c117a-141">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c117a-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c117a-142">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c117a-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c117a-143">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="c117a-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="c117a-144">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="c117a-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c117a-145">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="c117a-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="c117a-146">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="c117a-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c117a-147">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="c117a-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="c117a-148">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c117a-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c117a-149">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c117a-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c117a-150">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="c117a-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="c117a-151">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="c117a-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="c117a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c117a-152">RELATED LINKS</span></span>


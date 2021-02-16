---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227116"
---
# <span data-ttu-id="b887e-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="b887e-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="b887e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b887e-102">SYNOPSIS</span></span>
<span data-ttu-id="b887e-103">Получает сведения о событиях восстановления сайта Azure в хранилище.</span><span class="sxs-lookup"><span data-stu-id="b887e-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="b887e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b887e-104">SYNTAX</span></span>

### <span data-ttu-id="b887e-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b887e-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b887e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b887e-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b887e-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="b887e-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b887e-108">ByName</span><span class="sxs-lookup"><span data-stu-id="b887e-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b887e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b887e-109">DESCRIPTION</span></span>
<span data-ttu-id="b887e-110">**Get-AzRecoveryServicesAsrEvent** получает список событий в хранилище на основе указанных фильтров выбора.</span><span class="sxs-lookup"><span data-stu-id="b887e-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="b887e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b887e-111">EXAMPLES</span></span>

### <span data-ttu-id="b887e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b887e-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="b887e-113">Список всех событий.</span><span class="sxs-lookup"><span data-stu-id="b887e-113">List of all events.</span></span>

### <span data-ttu-id="b887e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b887e-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="b887e-115">Получить событие по имени.</span><span class="sxs-lookup"><span data-stu-id="b887e-115">Get event by name.</span></span>

### <span data-ttu-id="b887e-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b887e-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="b887e-117">Список событий для затронутых объектов.</span><span class="sxs-lookup"><span data-stu-id="b887e-117">List of event for affected Object.</span></span>

### <span data-ttu-id="b887e-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b887e-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="b887e-119">Список событий между временем начала и временем окончания, критической серьезности и типа VmHealth.</span><span class="sxs-lookup"><span data-stu-id="b887e-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="b887e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b887e-120">PARAMETERS</span></span>

### <span data-ttu-id="b887e-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b887e-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="b887e-122">Определяет затронутыйОбыватель friendlyName для поиска.</span><span class="sxs-lookup"><span data-stu-id="b887e-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b887e-123">-DefaultProfile</span></span>
<span data-ttu-id="b887e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b887e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b887e-125">-EndTime</span></span>
<span data-ttu-id="b887e-126">Время окончания окна поиска.</span><span class="sxs-lookup"><span data-stu-id="b887e-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="b887e-127">Используйте этот параметр, чтобы получить только те события, которые произошли до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="b887e-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="b887e-128">-EventType</span></span>
<span data-ttu-id="b887e-129">Фильтрация событий по типу события.</span><span class="sxs-lookup"><span data-stu-id="b887e-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-130">-Ткань</span><span class="sxs-lookup"><span data-stu-id="b887e-130">-Fabric</span></span>
<span data-ttu-id="b887e-131">Отфильтровать события по указанному материалу.</span><span class="sxs-lookup"><span data-stu-id="b887e-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="b887e-132">-FabricId</span></span>
<span data-ttu-id="b887e-133">Определяет, что нужно отфильтровать fabricId.</span><span class="sxs-lookup"><span data-stu-id="b887e-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b887e-134">-Name</span></span>
<span data-ttu-id="b887e-135">Указывает имя события, которое будет искаться.</span><span class="sxs-lookup"><span data-stu-id="b887e-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b887e-136">-ResourceId</span></span>
<span data-ttu-id="b887e-137">Определяет событие ResourceId события.</span><span class="sxs-lookup"><span data-stu-id="b887e-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-138">-Severity</span><span class="sxs-lookup"><span data-stu-id="b887e-138">-Severity</span></span>
<span data-ttu-id="b887e-139">Серьезность отфильтрованного события.</span><span class="sxs-lookup"><span data-stu-id="b887e-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b887e-140">-StartTime</span></span>
<span data-ttu-id="b887e-141">Время начала окна поиска.</span><span class="sxs-lookup"><span data-stu-id="b887e-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="b887e-142">Используйте этот параметр, чтобы получить только те события, которые произошли после указанного времени.</span><span class="sxs-lookup"><span data-stu-id="b887e-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b887e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b887e-143">CommonParameters</span></span>
<span data-ttu-id="b887e-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b887e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b887e-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b887e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b887e-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b887e-146">INPUTS</span></span>

### <span data-ttu-id="b887e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b887e-147">System.String</span></span>

## <span data-ttu-id="b887e-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b887e-148">OUTPUTS</span></span>

### <span data-ttu-id="b887e-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span><span class="sxs-lookup"><span data-stu-id="b887e-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="b887e-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b887e-150">NOTES</span></span>

## <span data-ttu-id="b887e-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b887e-151">RELATED LINKS</span></span>

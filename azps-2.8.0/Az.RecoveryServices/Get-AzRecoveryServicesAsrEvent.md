---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 673343029608935c629c6240d1bc1f5ec5a7d4e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905005"
---
# <span data-ttu-id="b0e93-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="b0e93-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="b0e93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0e93-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e93-103">Получение сведений о событиях Azure Site Recovery в хранилище.</span><span class="sxs-lookup"><span data-stu-id="b0e93-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="b0e93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0e93-104">SYNTAX</span></span>

### <span data-ttu-id="b0e93-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0e93-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0e93-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e93-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e93-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="b0e93-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e93-108">ByName</span><span class="sxs-lookup"><span data-stu-id="b0e93-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0e93-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0e93-109">DESCRIPTION</span></span>
<span data-ttu-id="b0e93-110">Параметр **Get-AzRecoveryServicesAsrEvent** получает список событий в хранилище на основе указанных фильтров выделения.</span><span class="sxs-lookup"><span data-stu-id="b0e93-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="b0e93-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0e93-111">EXAMPLES</span></span>

### <span data-ttu-id="b0e93-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0e93-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="b0e93-113">Список всех событий.</span><span class="sxs-lookup"><span data-stu-id="b0e93-113">List of all events.</span></span>

### <span data-ttu-id="b0e93-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b0e93-114">Example 2</span></span>
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

<span data-ttu-id="b0e93-115">Получить событие по имени.</span><span class="sxs-lookup"><span data-stu-id="b0e93-115">Get event by name.</span></span>

### <span data-ttu-id="b0e93-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b0e93-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="b0e93-117">Список событий для затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="b0e93-117">List of event for affected Object.</span></span>

### <span data-ttu-id="b0e93-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b0e93-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="b0e93-119">Список событий между временем начала и временем окончания, критической важности и типом работоспособности VmHealth.</span><span class="sxs-lookup"><span data-stu-id="b0e93-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="b0e93-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0e93-120">PARAMETERS</span></span>

### <span data-ttu-id="b0e93-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b0e93-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="b0e93-122">Указывает AffectedObject FriendlyName для поиска.</span><span class="sxs-lookup"><span data-stu-id="b0e93-122">Specifies AffectedObject FriendlyName for the search.</span></span>

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

### <span data-ttu-id="b0e93-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e93-123">-DefaultProfile</span></span>
<span data-ttu-id="b0e93-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e93-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0e93-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b0e93-125">-EndTime</span></span>
<span data-ttu-id="b0e93-126">Указывает время окончания окна поиска.</span><span class="sxs-lookup"><span data-stu-id="b0e93-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="b0e93-127">Используйте этот параметр, чтобы получать только те события, которые происходили до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="b0e93-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

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

### <span data-ttu-id="b0e93-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="b0e93-128">-EventType</span></span>
<span data-ttu-id="b0e93-129">Фильтрация событий по типу события.</span><span class="sxs-lookup"><span data-stu-id="b0e93-129">Filter events by the event type.</span></span>

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

### <span data-ttu-id="b0e93-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="b0e93-130">-Fabric</span></span>
<span data-ttu-id="b0e93-131">Фильтрация событий по указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="b0e93-131">Filter events by the specified fabric.</span></span>

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

### <span data-ttu-id="b0e93-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="b0e93-132">-FabricId</span></span>
<span data-ttu-id="b0e93-133">Указывает fabricId, который нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="b0e93-133">Specifies the fabricId to filter.</span></span>

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

### <span data-ttu-id="b0e93-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b0e93-134">-Name</span></span>
<span data-ttu-id="b0e93-135">Указывает имя события для поиска.</span><span class="sxs-lookup"><span data-stu-id="b0e93-135">Specifies name of the event for search.</span></span>

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

### <span data-ttu-id="b0e93-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e93-136">-ResourceId</span></span>
<span data-ttu-id="b0e93-137">Указывает ResourceId события для события.</span><span class="sxs-lookup"><span data-stu-id="b0e93-137">Specifies the event ResourceId of event.</span></span>

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

### <span data-ttu-id="b0e93-138">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="b0e93-138">-Severity</span></span>
<span data-ttu-id="b0e93-139">Уровень серьезности события для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="b0e93-139">Event severity to filter on.</span></span>

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

### <span data-ttu-id="b0e93-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b0e93-140">-StartTime</span></span>
<span data-ttu-id="b0e93-141">Указывает время запуска окна поиска.</span><span class="sxs-lookup"><span data-stu-id="b0e93-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="b0e93-142">Используйте этот параметр, чтобы получать только те события, которые произошли по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="b0e93-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

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

### <span data-ttu-id="b0e93-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e93-143">CommonParameters</span></span>
<span data-ttu-id="b0e93-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0e93-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e93-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e93-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e93-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0e93-146">INPUTS</span></span>

### <span data-ttu-id="b0e93-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b0e93-147">System.String</span></span>

## <span data-ttu-id="b0e93-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0e93-148">OUTPUTS</span></span>

### <span data-ttu-id="b0e93-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="b0e93-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="b0e93-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0e93-150">NOTES</span></span>

## <span data-ttu-id="b0e93-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0e93-151">RELATED LINKS</span></span>

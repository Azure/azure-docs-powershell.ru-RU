---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566930"
---
# <span data-ttu-id="4dac9-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="4dac9-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="4dac9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4dac9-102">SYNOPSIS</span></span>
<span data-ttu-id="4dac9-103">Получение сведений о событиях Azure Site Recovery в хранилище.</span><span class="sxs-lookup"><span data-stu-id="4dac9-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dac9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4dac9-104">SYNTAX</span></span>

### <span data-ttu-id="4dac9-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4dac9-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dac9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4dac9-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dac9-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="4dac9-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dac9-108">ByName</span><span class="sxs-lookup"><span data-stu-id="4dac9-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dac9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dac9-109">DESCRIPTION</span></span>
<span data-ttu-id="4dac9-110">Параметр **Get-AzureRmRecoveryServicesAsrEvent** получает список событий в хранилище на основе указанных фильтров выделения.</span><span class="sxs-lookup"><span data-stu-id="4dac9-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="4dac9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4dac9-111">EXAMPLES</span></span>

### <span data-ttu-id="4dac9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4dac9-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="4dac9-113">Список всех событий.</span><span class="sxs-lookup"><span data-stu-id="4dac9-113">List of all events.</span></span>

### <span data-ttu-id="4dac9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4dac9-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="4dac9-115">Получить событие по имени.</span><span class="sxs-lookup"><span data-stu-id="4dac9-115">Get event by name.</span></span>

### <span data-ttu-id="4dac9-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4dac9-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="4dac9-117">Список событий для затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="4dac9-117">List of event for affected Object.</span></span>

### <span data-ttu-id="4dac9-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4dac9-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="4dac9-119">Список событий между временем начала и временем окончания, критической важности и типом работоспособности VmHealth.</span><span class="sxs-lookup"><span data-stu-id="4dac9-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="4dac9-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4dac9-120">PARAMETERS</span></span>

### <span data-ttu-id="4dac9-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4dac9-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="4dac9-122">Указывает AffectedObject FriendlyName для поиска.</span><span class="sxs-lookup"><span data-stu-id="4dac9-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dac9-123">-DefaultProfile</span></span>
<span data-ttu-id="4dac9-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dac9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4dac9-125">-EndTime</span></span>
<span data-ttu-id="4dac9-126">Указывает время окончания окна поиска.</span><span class="sxs-lookup"><span data-stu-id="4dac9-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="4dac9-127">Используйте этот параметр, чтобы получать только те события, которые происходили до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="4dac9-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="4dac9-128">-EventType</span></span>
<span data-ttu-id="4dac9-129">Фильтрация событий по типу события.</span><span class="sxs-lookup"><span data-stu-id="4dac9-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="4dac9-130">-Fabric</span></span>
<span data-ttu-id="4dac9-131">Фильтрация событий по указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="4dac9-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="4dac9-132">-FabricId</span></span>
<span data-ttu-id="4dac9-133">Указывает fabricId, который нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="4dac9-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4dac9-134">-Name</span></span>
<span data-ttu-id="4dac9-135">Указывает имя события для поиска.</span><span class="sxs-lookup"><span data-stu-id="4dac9-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dac9-136">-ResourceId</span></span>
<span data-ttu-id="4dac9-137">Specifes событие ReourceId события.</span><span class="sxs-lookup"><span data-stu-id="4dac9-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-138">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="4dac9-138">-Severity</span></span>
<span data-ttu-id="4dac9-139">Уровень серьезности события для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4dac9-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4dac9-140">-StartTime</span></span>
<span data-ttu-id="4dac9-141">Указывает время запуска окна поиска.</span><span class="sxs-lookup"><span data-stu-id="4dac9-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="4dac9-142">Используйте этот параметр, чтобы получать только те события, которые произошли по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="4dac9-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dac9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dac9-143">CommonParameters</span></span>
<span data-ttu-id="4dac9-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4dac9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dac9-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dac9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dac9-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4dac9-146">INPUTS</span></span>

### <span data-ttu-id="4dac9-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4dac9-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4dac9-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dac9-148">OUTPUTS</span></span>

### <span data-ttu-id="4dac9-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4dac9-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4dac9-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="4dac9-150">NOTES</span></span>

## <span data-ttu-id="4dac9-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dac9-151">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078607"
---
# <span data-ttu-id="e7ece-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e7ece-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="e7ece-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7ece-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ece-103">Получает сведения о расписаниях пропускной способности</span><span class="sxs-lookup"><span data-stu-id="e7ece-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="e7ece-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7ece-104">SYNTAX</span></span>

### <span data-ttu-id="e7ece-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7ece-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7ece-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7ece-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ece-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7ece-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7ece-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7ece-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e7ece-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7ece-109">DESCRIPTION</span></span>
<span data-ttu-id="e7ece-110">Командлет **Get-AzStackEdgeBandwidthSchedule** получает сведения о расписании пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e7ece-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="e7ece-111">Вы можете указать имя расписания вместе с именем группы ресурсов и именем устройства, чтобы получить сведения о конкретном расписании пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e7ece-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="e7ece-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7ece-112">EXAMPLES</span></span>

### <span data-ttu-id="e7ece-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7ece-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="e7ece-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e7ece-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="e7ece-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7ece-115">PARAMETERS</span></span>

### <span data-ttu-id="e7ece-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ece-116">-DefaultProfile</span></span>
<span data-ttu-id="e7ece-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ece-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7ece-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="e7ece-118">-DeviceName</span></span>
<span data-ttu-id="e7ece-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="e7ece-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ece-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e7ece-120">-DeviceObject</span></span>
<span data-ttu-id="e7ece-121">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="e7ece-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ece-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7ece-122">-Name</span></span>
<span data-ttu-id="e7ece-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="e7ece-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ece-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ece-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7ece-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e7ece-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ece-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ece-126">-ResourceId</span></span>
<span data-ttu-id="e7ece-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ece-127">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ece-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ece-128">CommonParameters</span></span>
<span data-ttu-id="e7ece-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7ece-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ece-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7ece-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ece-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7ece-131">INPUTS</span></span>

### <span data-ttu-id="e7ece-132">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e7ece-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="e7ece-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7ece-133">OUTPUTS</span></span>

### <span data-ttu-id="e7ece-134">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e7ece-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="e7ece-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7ece-135">NOTES</span></span>

## <span data-ttu-id="e7ece-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7ece-136">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236827"
---
# <span data-ttu-id="f6661-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="f6661-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="f6661-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6661-102">SYNOPSIS</span></span>
<span data-ttu-id="f6661-103">Получает сведения о расписаниях пропускной способности</span><span class="sxs-lookup"><span data-stu-id="f6661-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="f6661-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6661-104">SYNTAX</span></span>

### <span data-ttu-id="f6661-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6661-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6661-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6661-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6661-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6661-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6661-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6661-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f6661-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6661-109">DESCRIPTION</span></span>
<span data-ttu-id="f6661-110">Командлет **Get-AzDataBoxEdgeBandwidthSchedule** получает сведения о расписании пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="f6661-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="f6661-111">Вы можете указать имя расписания вместе с именем группы ресурсов и именем устройства, чтобы получить сведения о конкретном расписании пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="f6661-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="f6661-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6661-112">EXAMPLES</span></span>

### <span data-ttu-id="f6661-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6661-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="f6661-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f6661-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="f6661-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6661-115">PARAMETERS</span></span>

### <span data-ttu-id="f6661-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6661-116">-DefaultProfile</span></span>
<span data-ttu-id="f6661-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6661-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6661-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="f6661-118">-DeviceName</span></span>
<span data-ttu-id="f6661-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f6661-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6661-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f6661-120">-DeviceObject</span></span>
<span data-ttu-id="f6661-121">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="f6661-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6661-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6661-122">-Name</span></span>
<span data-ttu-id="f6661-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f6661-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6661-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6661-124">-ResourceGroupName</span></span>
<span data-ttu-id="f6661-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f6661-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6661-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6661-126">-ResourceId</span></span>
<span data-ttu-id="f6661-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6661-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="f6661-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6661-128">CommonParameters</span></span>
<span data-ttu-id="f6661-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6661-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6661-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6661-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6661-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6661-131">INPUTS</span></span>

### <span data-ttu-id="f6661-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f6661-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f6661-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6661-133">OUTPUTS</span></span>

### <span data-ttu-id="f6661-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="f6661-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="f6661-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6661-135">NOTES</span></span>

## <span data-ttu-id="f6661-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6661-136">RELATED LINKS</span></span>

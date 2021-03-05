---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: f02cda5fe04ed72a5e6defd382c372b40c9c039b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998094"
---
# <span data-ttu-id="d70dc-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d70dc-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d70dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d70dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d70dc-103">Возвращает сведения о доступных устройствах Edge Box Data Box.</span><span class="sxs-lookup"><span data-stu-id="d70dc-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="d70dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d70dc-104">SYNTAX</span></span>

### <span data-ttu-id="d70dc-105">ListByParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d70dc-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d70dc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70dc-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d70dc-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d70dc-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d70dc-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d70dc-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70dc-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70dc-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70dc-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70dc-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70dc-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d70dc-116">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d70dc-116">DESCRIPTION</span></span>
<span data-ttu-id="d70dc-117">Чтобы получить сведения о доступных устройствах Edge Box, можно получить сведения о **get-AzDataBoxEdgeDevice.**</span><span class="sxs-lookup"><span data-stu-id="d70dc-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="d70dc-118">Вы можете указать имя устройства вместе с именем группы ресурсов, чтобы получить сведения о конкретном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d70dc-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="d70dc-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d70dc-119">EXAMPLES</span></span>

### <span data-ttu-id="d70dc-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d70dc-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="d70dc-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d70dc-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="d70dc-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d70dc-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="d70dc-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d70dc-123">PARAMETERS</span></span>

### <span data-ttu-id="d70dc-124">-Оповещение</span><span class="sxs-lookup"><span data-stu-id="d70dc-124">-Alert</span></span>
<span data-ttu-id="d70dc-125">Извлечение оповещений на устройстве границы или шлюза в поле данных</span><span class="sxs-lookup"><span data-stu-id="d70dc-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70dc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70dc-126">-DefaultProfile</span></span>
<span data-ttu-id="d70dc-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d70dc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d70dc-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="d70dc-128">-ExtendedInfo</span></span>
<span data-ttu-id="d70dc-129">Получает дополнительные сведения для указанного устройства шлюза Box или Data Box.</span><span class="sxs-lookup"><span data-stu-id="d70dc-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70dc-130">-Name</span><span class="sxs-lookup"><span data-stu-id="d70dc-130">-Name</span></span>
<span data-ttu-id="d70dc-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d70dc-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70dc-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="d70dc-132">-NetworkSetting</span></span>
<span data-ttu-id="d70dc-133">Получает параметры сети для указанного устройства шлюза Box или Data Box.</span><span class="sxs-lookup"><span data-stu-id="d70dc-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70dc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d70dc-134">-ResourceGroupName</span></span>
<span data-ttu-id="d70dc-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d70dc-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70dc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d70dc-136">-ResourceId</span></span>
<span data-ttu-id="d70dc-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d70dc-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70dc-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="d70dc-138">-UpdateSummary</span></span>
<span data-ttu-id="d70dc-139">Сведения о доступности обновлений на основе последнего сканирования устройства.</span><span class="sxs-lookup"><span data-stu-id="d70dc-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="d70dc-140">Она также получает сведения обо всех текущих заданиях скачивания и установки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d70dc-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70dc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70dc-141">CommonParameters</span></span>
<span data-ttu-id="d70dc-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d70dc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70dc-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d70dc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d70dc-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d70dc-144">INPUTS</span></span>

### <span data-ttu-id="d70dc-145">Нет</span><span class="sxs-lookup"><span data-stu-id="d70dc-145">None</span></span>

## <span data-ttu-id="d70dc-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d70dc-146">OUTPUTS</span></span>

### <span data-ttu-id="d70dc-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d70dc-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="d70dc-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="d70dc-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="d70dc-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="d70dc-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="d70dc-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="d70dc-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="d70dc-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="d70dc-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="d70dc-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d70dc-152">NOTES</span></span>

## <span data-ttu-id="d70dc-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d70dc-153">RELATED LINKS</span></span>

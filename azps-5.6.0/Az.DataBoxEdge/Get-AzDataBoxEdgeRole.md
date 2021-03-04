---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9dd4925224f2ed91770caff422b8ab6f5d924754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998637"
---
# <span data-ttu-id="8f9e0-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8f9e0-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="8f9e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f9e0-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9e0-103">Извлекает доступные роли для устройства.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="8f9e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f9e0-104">SYNTAX</span></span>

### <span data-ttu-id="8f9e0-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f9e0-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f9e0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f9e0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f9e0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f9e0-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f9e0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f9e0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8f9e0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f9e0-109">DESCRIPTION</span></span>
<span data-ttu-id="8f9e0-110">С **его роли** извлекается доступ к ролям IoT для устройства Edge data Box.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="8f9e0-111">Вы можете упомянуть параметр Name, чтобы получить сведения о конкретной роли IoT.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="8f9e0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f9e0-112">EXAMPLES</span></span>

### <span data-ttu-id="8f9e0-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f9e0-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="8f9e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f9e0-114">PARAMETERS</span></span>

### <span data-ttu-id="8f9e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f9e0-115">-DefaultProfile</span></span>
<span data-ttu-id="8f9e0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f9e0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8f9e0-117">-DeviceName</span></span>
<span data-ttu-id="8f9e0-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="8f9e0-118">Device Name</span></span>

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

### <span data-ttu-id="8f9e0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8f9e0-119">-DeviceObject</span></span>
<span data-ttu-id="8f9e0-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="8f9e0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8f9e0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8f9e0-121">-Name</span></span>
<span data-ttu-id="8f9e0-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="8f9e0-122">Resource Name</span></span>

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

### <span data-ttu-id="8f9e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f9e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f9e0-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8f9e0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8f9e0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f9e0-125">-ResourceId</span></span>
<span data-ttu-id="8f9e0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f9e0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="8f9e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f9e0-127">CommonParameters</span></span>
<span data-ttu-id="8f9e0-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f9e0-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f9e0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f9e0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f9e0-130">INPUTS</span></span>

### <span data-ttu-id="8f9e0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8f9e0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8f9e0-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f9e0-132">OUTPUTS</span></span>

### <span data-ttu-id="8f9e0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8f9e0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="8f9e0-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f9e0-134">NOTES</span></span>

## <span data-ttu-id="8f9e0-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f9e0-135">RELATED LINKS</span></span>

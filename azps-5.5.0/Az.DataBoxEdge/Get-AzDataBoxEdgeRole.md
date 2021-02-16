---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238396"
---
# <span data-ttu-id="31b6e-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="31b6e-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="31b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="31b6e-103">Извлекает доступные роли для устройства.</span><span class="sxs-lookup"><span data-stu-id="31b6e-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="31b6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31b6e-104">SYNTAX</span></span>

### <span data-ttu-id="31b6e-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31b6e-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b6e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b6e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b6e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b6e-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b6e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b6e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="31b6e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31b6e-109">DESCRIPTION</span></span>
<span data-ttu-id="31b6e-110">Для получения доступных ролей IoT на устройстве Edge data Box можно получить доступ к ролям **Get-AzDataBoxEdgeRole.**</span><span class="sxs-lookup"><span data-stu-id="31b6e-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="31b6e-111">Вы можете упомянуть параметр Name, чтобы получить сведения о конкретной роли IoT.</span><span class="sxs-lookup"><span data-stu-id="31b6e-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="31b6e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31b6e-112">EXAMPLES</span></span>

### <span data-ttu-id="31b6e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31b6e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="31b6e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31b6e-114">PARAMETERS</span></span>

### <span data-ttu-id="31b6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b6e-115">-DefaultProfile</span></span>
<span data-ttu-id="31b6e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31b6e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b6e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="31b6e-117">-DeviceName</span></span>
<span data-ttu-id="31b6e-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="31b6e-118">Device Name</span></span>

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

### <span data-ttu-id="31b6e-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="31b6e-119">-DeviceObject</span></span>
<span data-ttu-id="31b6e-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="31b6e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="31b6e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="31b6e-121">-Name</span></span>
<span data-ttu-id="31b6e-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="31b6e-122">Resource Name</span></span>

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

### <span data-ttu-id="31b6e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b6e-123">-ResourceGroupName</span></span>
<span data-ttu-id="31b6e-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="31b6e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="31b6e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31b6e-125">-ResourceId</span></span>
<span data-ttu-id="31b6e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="31b6e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="31b6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b6e-127">CommonParameters</span></span>
<span data-ttu-id="31b6e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b6e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31b6e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b6e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31b6e-130">INPUTS</span></span>

### <span data-ttu-id="31b6e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="31b6e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="31b6e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31b6e-132">OUTPUTS</span></span>

### <span data-ttu-id="31b6e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="31b6e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="31b6e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31b6e-134">NOTES</span></span>

## <span data-ttu-id="31b6e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31b6e-135">RELATED LINKS</span></span>

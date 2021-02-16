---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235449"
---
# <span data-ttu-id="0eadc-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0eadc-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="0eadc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eadc-102">SYNOPSIS</span></span>
<span data-ttu-id="0eadc-103">Извлекает доступные роли для устройства.</span><span class="sxs-lookup"><span data-stu-id="0eadc-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="0eadc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0eadc-104">SYNTAX</span></span>

### <span data-ttu-id="0eadc-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0eadc-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eadc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eadc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eadc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eadc-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eadc-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eadc-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0eadc-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0eadc-109">DESCRIPTION</span></span>
<span data-ttu-id="0eadc-110">С **его роли извлекается** доступные роли IoT для устройства с Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="0eadc-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="0eadc-111">Вы можете упомянуть параметр Name, чтобы получить сведения о конкретной роли IoT.</span><span class="sxs-lookup"><span data-stu-id="0eadc-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="0eadc-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0eadc-112">EXAMPLES</span></span>

### <span data-ttu-id="0eadc-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0eadc-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="0eadc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eadc-114">PARAMETERS</span></span>

### <span data-ttu-id="0eadc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eadc-115">-DefaultProfile</span></span>
<span data-ttu-id="0eadc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0eadc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eadc-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0eadc-117">-DeviceName</span></span>
<span data-ttu-id="0eadc-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="0eadc-118">Device Name</span></span>

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

### <span data-ttu-id="0eadc-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="0eadc-119">-DeviceObject</span></span>
<span data-ttu-id="0eadc-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="0eadc-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="0eadc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0eadc-121">-Name</span></span>
<span data-ttu-id="0eadc-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="0eadc-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eadc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eadc-123">-ResourceGroupName</span></span>
<span data-ttu-id="0eadc-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0eadc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0eadc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eadc-125">-ResourceId</span></span>
<span data-ttu-id="0eadc-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eadc-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eadc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eadc-127">CommonParameters</span></span>
<span data-ttu-id="0eadc-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eadc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eadc-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eadc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eadc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0eadc-130">INPUTS</span></span>

### <span data-ttu-id="0eadc-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0eadc-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="0eadc-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0eadc-132">OUTPUTS</span></span>

### <span data-ttu-id="0eadc-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0eadc-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="0eadc-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0eadc-134">NOTES</span></span>

## <span data-ttu-id="0eadc-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0eadc-135">RELATED LINKS</span></span>

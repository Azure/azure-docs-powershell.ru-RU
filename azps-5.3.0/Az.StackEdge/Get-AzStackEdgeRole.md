---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518754"
---
# <span data-ttu-id="47dca-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="47dca-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="47dca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47dca-102">SYNOPSIS</span></span>
<span data-ttu-id="47dca-103">Извлекает доступные роли для устройства.</span><span class="sxs-lookup"><span data-stu-id="47dca-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="47dca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47dca-104">SYNTAX</span></span>

### <span data-ttu-id="47dca-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47dca-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47dca-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47dca-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47dca-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47dca-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47dca-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47dca-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="47dca-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47dca-109">DESCRIPTION</span></span>
<span data-ttu-id="47dca-110">С **его роли извлекается** доступ к ролям IoT для устройства с Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="47dca-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="47dca-111">Вы можете упомянуть параметр Name, чтобы получить сведения о конкретной роли IoT.</span><span class="sxs-lookup"><span data-stu-id="47dca-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="47dca-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47dca-112">EXAMPLES</span></span>

### <span data-ttu-id="47dca-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47dca-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="47dca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47dca-114">PARAMETERS</span></span>

### <span data-ttu-id="47dca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dca-115">-DefaultProfile</span></span>
<span data-ttu-id="47dca-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47dca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47dca-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="47dca-117">-DeviceName</span></span>
<span data-ttu-id="47dca-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="47dca-118">Device Name</span></span>

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

### <span data-ttu-id="47dca-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="47dca-119">-DeviceObject</span></span>
<span data-ttu-id="47dca-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="47dca-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="47dca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="47dca-121">-Name</span></span>
<span data-ttu-id="47dca-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="47dca-122">Resource Name</span></span>

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

### <span data-ttu-id="47dca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47dca-123">-ResourceGroupName</span></span>
<span data-ttu-id="47dca-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="47dca-124">Resource Group Name</span></span>

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

### <span data-ttu-id="47dca-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47dca-125">-ResourceId</span></span>
<span data-ttu-id="47dca-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="47dca-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="47dca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dca-127">CommonParameters</span></span>
<span data-ttu-id="47dca-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47dca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dca-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47dca-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dca-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47dca-130">INPUTS</span></span>

### <span data-ttu-id="47dca-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="47dca-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="47dca-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47dca-132">OUTPUTS</span></span>

### <span data-ttu-id="47dca-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="47dca-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="47dca-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47dca-134">NOTES</span></span>

## <span data-ttu-id="47dca-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47dca-135">RELATED LINKS</span></span>

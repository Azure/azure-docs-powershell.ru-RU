---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073418"
---
# <span data-ttu-id="e80dc-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e80dc-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="e80dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e80dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e80dc-103">Извлекает доступные роли для устройства.</span><span class="sxs-lookup"><span data-stu-id="e80dc-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="e80dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e80dc-104">SYNTAX</span></span>

### <span data-ttu-id="e80dc-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e80dc-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80dc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80dc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80dc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80dc-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80dc-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80dc-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e80dc-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e80dc-109">DESCRIPTION</span></span>
<span data-ttu-id="e80dc-110">Командлет **Get-AzDataBoxEdgeRole** извлекает доступные роли IOT для поля данных, расположенного на пограничном устройстве.</span><span class="sxs-lookup"><span data-stu-id="e80dc-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="e80dc-111">Вы можете упомянуть о параметре name, чтобы получить сведения о конкретной роли Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="e80dc-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="e80dc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e80dc-112">EXAMPLES</span></span>

### <span data-ttu-id="e80dc-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e80dc-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="e80dc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e80dc-114">PARAMETERS</span></span>

### <span data-ttu-id="e80dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80dc-115">-DefaultProfile</span></span>
<span data-ttu-id="e80dc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e80dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e80dc-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="e80dc-117">-DeviceName</span></span>
<span data-ttu-id="e80dc-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="e80dc-118">Device Name</span></span>

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

### <span data-ttu-id="e80dc-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e80dc-119">-DeviceObject</span></span>
<span data-ttu-id="e80dc-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="e80dc-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e80dc-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e80dc-121">-Name</span></span>
<span data-ttu-id="e80dc-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="e80dc-122">Resource Name</span></span>

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

### <span data-ttu-id="e80dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e80dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="e80dc-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e80dc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e80dc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e80dc-125">-ResourceId</span></span>
<span data-ttu-id="e80dc-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e80dc-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="e80dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80dc-127">CommonParameters</span></span>
<span data-ttu-id="e80dc-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e80dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80dc-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e80dc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80dc-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e80dc-130">INPUTS</span></span>

### <span data-ttu-id="e80dc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e80dc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e80dc-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e80dc-132">OUTPUTS</span></span>

### <span data-ttu-id="e80dc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e80dc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e80dc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e80dc-134">NOTES</span></span>

## <span data-ttu-id="e80dc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e80dc-135">RELATED LINKS</span></span>

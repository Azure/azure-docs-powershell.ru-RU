---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519109"
---
# <span data-ttu-id="93881-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="93881-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="93881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93881-102">SYNOPSIS</span></span>
<span data-ttu-id="93881-103">Получает задания, запланированные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="93881-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="93881-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93881-104">SYNTAX</span></span>

### <span data-ttu-id="93881-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93881-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93881-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="93881-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93881-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93881-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="93881-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93881-108">DESCRIPTION</span></span>
<span data-ttu-id="93881-109">На **устройстве Get-AzDataBoxEdgeJob** происходит набор активных заданий на устройстве Edge box data Box.</span><span class="sxs-lookup"><span data-stu-id="93881-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="93881-110">Вы можете упомянуть параметр Name, чтобы получить сведения об определенном заданиях.</span><span class="sxs-lookup"><span data-stu-id="93881-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="93881-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93881-111">EXAMPLES</span></span>

### <span data-ttu-id="93881-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93881-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="93881-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93881-113">PARAMETERS</span></span>

### <span data-ttu-id="93881-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93881-114">-DefaultProfile</span></span>
<span data-ttu-id="93881-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93881-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93881-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="93881-116">-DeviceName</span></span>
<span data-ttu-id="93881-117">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="93881-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93881-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="93881-118">-DeviceObject</span></span>
<span data-ttu-id="93881-119">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="93881-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="93881-120">-Name</span><span class="sxs-lookup"><span data-stu-id="93881-120">-Name</span></span>
<span data-ttu-id="93881-121">Имя задания (как правило, GUID)</span><span class="sxs-lookup"><span data-stu-id="93881-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93881-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93881-122">-ResourceGroupName</span></span>
<span data-ttu-id="93881-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="93881-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93881-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93881-124">-ResourceId</span></span>
<span data-ttu-id="93881-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="93881-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93881-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93881-126">CommonParameters</span></span>
<span data-ttu-id="93881-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93881-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93881-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93881-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93881-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93881-129">INPUTS</span></span>

### <span data-ttu-id="93881-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="93881-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="93881-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93881-131">OUTPUTS</span></span>

### <span data-ttu-id="93881-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="93881-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="93881-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93881-133">NOTES</span></span>

## <span data-ttu-id="93881-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93881-134">RELATED LINKS</span></span>

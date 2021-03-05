---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 14e19068d3634acfd558f976b13661af28495321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007576"
---
# <span data-ttu-id="a02f0-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="a02f0-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="a02f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a02f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a02f0-103">Получает задания, запланированные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a02f0-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="a02f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a02f0-104">SYNTAX</span></span>

### <span data-ttu-id="a02f0-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a02f0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a02f0-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="a02f0-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a02f0-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a02f0-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a02f0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a02f0-108">DESCRIPTION</span></span>
<span data-ttu-id="a02f0-109">Для работы на устройстве Stack Edge можно получить активные задания с его предназначением — **Get-AzStackEdgeJob.**</span><span class="sxs-lookup"><span data-stu-id="a02f0-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="a02f0-110">Вы можете упомянуть параметр Name, чтобы получить сведения об определенном заданиях.</span><span class="sxs-lookup"><span data-stu-id="a02f0-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="a02f0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a02f0-111">EXAMPLES</span></span>

### <span data-ttu-id="a02f0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a02f0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="a02f0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a02f0-113">PARAMETERS</span></span>

### <span data-ttu-id="a02f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02f0-114">-DefaultProfile</span></span>
<span data-ttu-id="a02f0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a02f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a02f0-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a02f0-116">-DeviceName</span></span>
<span data-ttu-id="a02f0-117">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="a02f0-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02f0-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a02f0-118">-DeviceObject</span></span>
<span data-ttu-id="a02f0-119">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="a02f0-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a02f0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a02f0-120">-Name</span></span>
<span data-ttu-id="a02f0-121">Имя задания (как правило, GUID)</span><span class="sxs-lookup"><span data-stu-id="a02f0-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02f0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02f0-122">-ResourceGroupName</span></span>
<span data-ttu-id="a02f0-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a02f0-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02f0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a02f0-124">-ResourceId</span></span>
<span data-ttu-id="a02f0-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a02f0-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02f0-126">CommonParameters</span></span>
<span data-ttu-id="a02f0-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02f0-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a02f0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02f0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a02f0-129">INPUTS</span></span>

### <span data-ttu-id="a02f0-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a02f0-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a02f0-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a02f0-131">OUTPUTS</span></span>

### <span data-ttu-id="a02f0-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="a02f0-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="a02f0-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a02f0-133">NOTES</span></span>

## <span data-ttu-id="a02f0-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a02f0-134">RELATED LINKS</span></span>

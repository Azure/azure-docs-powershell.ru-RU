---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236561"
---
# <span data-ttu-id="372b8-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="372b8-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="372b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="372b8-102">SYNOPSIS</span></span>
<span data-ttu-id="372b8-103">Возвращает задания, запланированные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="372b8-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="372b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="372b8-104">SYNTAX</span></span>

### <span data-ttu-id="372b8-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="372b8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="372b8-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="372b8-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="372b8-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="372b8-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="372b8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="372b8-108">DESCRIPTION</span></span>
<span data-ttu-id="372b8-109">Командлет **Get-AzStackEdgeJob** получает активные задания на пограничном устройстве стопки.</span><span class="sxs-lookup"><span data-stu-id="372b8-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="372b8-110">Вы можете упомянуть о параметре Name для получения сведений о конкретном задании.</span><span class="sxs-lookup"><span data-stu-id="372b8-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="372b8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="372b8-111">EXAMPLES</span></span>

### <span data-ttu-id="372b8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="372b8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="372b8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="372b8-113">PARAMETERS</span></span>

### <span data-ttu-id="372b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372b8-114">-DefaultProfile</span></span>
<span data-ttu-id="372b8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="372b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372b8-116">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="372b8-116">-DeviceName</span></span>
<span data-ttu-id="372b8-117">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="372b8-117">Name of the device</span></span>

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

### <span data-ttu-id="372b8-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="372b8-118">-DeviceObject</span></span>
<span data-ttu-id="372b8-119">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="372b8-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="372b8-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="372b8-120">-Name</span></span>
<span data-ttu-id="372b8-121">Имя задания, обычно GUID</span><span class="sxs-lookup"><span data-stu-id="372b8-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="372b8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372b8-122">-ResourceGroupName</span></span>
<span data-ttu-id="372b8-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="372b8-123">Resource Group Name</span></span>

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

### <span data-ttu-id="372b8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="372b8-124">-ResourceId</span></span>
<span data-ttu-id="372b8-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="372b8-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="372b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372b8-126">CommonParameters</span></span>
<span data-ttu-id="372b8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="372b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372b8-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="372b8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372b8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="372b8-129">INPUTS</span></span>

### <span data-ttu-id="372b8-130">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="372b8-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="372b8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="372b8-131">OUTPUTS</span></span>

### <span data-ttu-id="372b8-132">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="372b8-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="372b8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="372b8-133">NOTES</span></span>

## <span data-ttu-id="372b8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="372b8-134">RELATED LINKS</span></span>
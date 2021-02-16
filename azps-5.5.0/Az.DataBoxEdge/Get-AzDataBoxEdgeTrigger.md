---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220377"
---
# <span data-ttu-id="78da3-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="78da3-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="78da3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78da3-102">SYNOPSIS</span></span>
<span data-ttu-id="78da3-103">Настройка триггеров на устройстве</span><span class="sxs-lookup"><span data-stu-id="78da3-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="78da3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78da3-104">SYNTAX</span></span>

### <span data-ttu-id="78da3-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78da3-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78da3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78da3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78da3-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78da3-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78da3-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78da3-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="78da3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78da3-109">DESCRIPTION</span></span>
<span data-ttu-id="78da3-110">**Cmdlet Get-AzDataBoxEdgeTriger** получает триггеры для устройства.</span><span class="sxs-lookup"><span data-stu-id="78da3-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="78da3-111">Вы можете указать имя в качестве параметра в cmdlet для получения сведений об определенных триггерах.</span><span class="sxs-lookup"><span data-stu-id="78da3-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="78da3-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78da3-112">EXAMPLES</span></span>

### <span data-ttu-id="78da3-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78da3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="78da3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78da3-114">PARAMETERS</span></span>

### <span data-ttu-id="78da3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78da3-115">-DefaultProfile</span></span>
<span data-ttu-id="78da3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78da3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78da3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="78da3-117">-DeviceName</span></span>
<span data-ttu-id="78da3-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="78da3-118">Device Name</span></span>

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

### <span data-ttu-id="78da3-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="78da3-119">-DeviceObject</span></span>
<span data-ttu-id="78da3-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="78da3-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="78da3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78da3-121">-Name</span></span>
<span data-ttu-id="78da3-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="78da3-122">Resource Name</span></span>

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

### <span data-ttu-id="78da3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78da3-123">-ResourceGroupName</span></span>
<span data-ttu-id="78da3-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="78da3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="78da3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78da3-125">-ResourceId</span></span>
<span data-ttu-id="78da3-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="78da3-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="78da3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78da3-127">CommonParameters</span></span>
<span data-ttu-id="78da3-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78da3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78da3-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78da3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78da3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78da3-130">INPUTS</span></span>

### <span data-ttu-id="78da3-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="78da3-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="78da3-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78da3-132">OUTPUTS</span></span>

### <span data-ttu-id="78da3-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="78da3-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="78da3-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78da3-134">NOTES</span></span>

## <span data-ttu-id="78da3-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78da3-135">RELATED LINKS</span></span>

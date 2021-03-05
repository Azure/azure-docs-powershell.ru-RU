---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: a4bcbad5f595efe126ed232b94d5deb368515bc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976243"
---
# <span data-ttu-id="67ea9-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="67ea9-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="67ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="67ea9-103">Настройка триггеров на устройстве</span><span class="sxs-lookup"><span data-stu-id="67ea9-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="67ea9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67ea9-104">SYNTAX</span></span>

### <span data-ttu-id="67ea9-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67ea9-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ea9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ea9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ea9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ea9-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ea9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ea9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="67ea9-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67ea9-109">DESCRIPTION</span></span>
<span data-ttu-id="67ea9-110">Триггеры для устройства **получает cmdlet Get-AzStackEdgeTriger.**</span><span class="sxs-lookup"><span data-stu-id="67ea9-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="67ea9-111">Вы можете указать имя в качестве параметра в cmdlet для получения сведений об определенных триггерах.</span><span class="sxs-lookup"><span data-stu-id="67ea9-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="67ea9-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67ea9-112">EXAMPLES</span></span>

### <span data-ttu-id="67ea9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67ea9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="67ea9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67ea9-114">PARAMETERS</span></span>

### <span data-ttu-id="67ea9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ea9-115">-DefaultProfile</span></span>
<span data-ttu-id="67ea9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67ea9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ea9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="67ea9-117">-DeviceName</span></span>
<span data-ttu-id="67ea9-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="67ea9-118">Device Name</span></span>

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

### <span data-ttu-id="67ea9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="67ea9-119">-DeviceObject</span></span>
<span data-ttu-id="67ea9-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="67ea9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="67ea9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="67ea9-121">-Name</span></span>
<span data-ttu-id="67ea9-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="67ea9-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ea9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ea9-123">-ResourceGroupName</span></span>
<span data-ttu-id="67ea9-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="67ea9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="67ea9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ea9-125">-ResourceId</span></span>
<span data-ttu-id="67ea9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ea9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="67ea9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ea9-127">CommonParameters</span></span>
<span data-ttu-id="67ea9-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ea9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ea9-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67ea9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ea9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67ea9-130">INPUTS</span></span>

### <span data-ttu-id="67ea9-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="67ea9-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="67ea9-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67ea9-132">OUTPUTS</span></span>

### <span data-ttu-id="67ea9-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="67ea9-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="67ea9-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67ea9-134">NOTES</span></span>

## <span data-ttu-id="67ea9-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67ea9-135">RELATED LINKS</span></span>

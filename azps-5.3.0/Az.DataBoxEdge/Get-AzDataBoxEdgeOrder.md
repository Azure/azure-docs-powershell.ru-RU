---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508638"
---
# <span data-ttu-id="f706b-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f706b-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f706b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f706b-102">SYNOPSIS</span></span>
<span data-ttu-id="f706b-103">Получить сведения о заказе для устройства</span><span class="sxs-lookup"><span data-stu-id="f706b-103">Get the order details for a device</span></span>

## <span data-ttu-id="f706b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f706b-104">SYNTAX</span></span>

### <span data-ttu-id="f706b-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f706b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f706b-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f706b-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f706b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f706b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f706b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f706b-108">DESCRIPTION</span></span>
<span data-ttu-id="f706b-109">**Cmdlet Get-AzDataBoxEdgeOrder получает** сведения о заказе для устройства Edge box data Box.</span><span class="sxs-lookup"><span data-stu-id="f706b-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="f706b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f706b-110">EXAMPLES</span></span>

### <span data-ttu-id="f706b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f706b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="f706b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f706b-112">PARAMETERS</span></span>

### <span data-ttu-id="f706b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f706b-113">-DefaultProfile</span></span>
<span data-ttu-id="f706b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f706b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f706b-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f706b-115">-DeviceName</span></span>
<span data-ttu-id="f706b-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f706b-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f706b-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f706b-117">-DeviceObject</span></span>
<span data-ttu-id="f706b-118">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="f706b-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f706b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f706b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f706b-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f706b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="f706b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f706b-121">-ResourceId</span></span>
<span data-ttu-id="f706b-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f706b-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="f706b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f706b-123">CommonParameters</span></span>
<span data-ttu-id="f706b-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f706b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f706b-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f706b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f706b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f706b-126">INPUTS</span></span>

### <span data-ttu-id="f706b-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f706b-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="f706b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f706b-128">System.String</span></span>

## <span data-ttu-id="f706b-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f706b-129">OUTPUTS</span></span>

### <span data-ttu-id="f706b-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f706b-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f706b-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f706b-131">NOTES</span></span>

## <span data-ttu-id="f706b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f706b-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402087"
---
# <span data-ttu-id="8bc34-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8bc34-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="8bc34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc34-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc34-103">Получить сведения о заказе для устройства</span><span class="sxs-lookup"><span data-stu-id="8bc34-103">Get the order details for a device</span></span>

## <span data-ttu-id="8bc34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8bc34-104">SYNTAX</span></span>

### <span data-ttu-id="8bc34-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bc34-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bc34-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bc34-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc34-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bc34-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bc34-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bc34-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc34-109">Чтобы **получить сведения о заказе для** устройства Stack Edge, можно получить сведения о его заказе.</span><span class="sxs-lookup"><span data-stu-id="8bc34-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="8bc34-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8bc34-110">EXAMPLES</span></span>

### <span data-ttu-id="8bc34-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bc34-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="8bc34-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bc34-112">PARAMETERS</span></span>

### <span data-ttu-id="8bc34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc34-113">-DefaultProfile</span></span>
<span data-ttu-id="8bc34-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc34-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc34-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8bc34-115">-DeviceName</span></span>
<span data-ttu-id="8bc34-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8bc34-116">Resource Group Name</span></span>

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

### <span data-ttu-id="8bc34-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8bc34-117">-DeviceObject</span></span>
<span data-ttu-id="8bc34-118">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="8bc34-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc34-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc34-119">-ResourceGroupName</span></span>
<span data-ttu-id="8bc34-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8bc34-120">Resource Group Name</span></span>

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

### <span data-ttu-id="8bc34-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc34-121">-ResourceId</span></span>
<span data-ttu-id="8bc34-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc34-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="8bc34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc34-123">CommonParameters</span></span>
<span data-ttu-id="8bc34-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc34-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bc34-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc34-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bc34-126">INPUTS</span></span>

### <span data-ttu-id="8bc34-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8bc34-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="8bc34-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8bc34-128">System.String</span></span>

## <span data-ttu-id="8bc34-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8bc34-129">OUTPUTS</span></span>

### <span data-ttu-id="8bc34-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8bc34-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="8bc34-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8bc34-131">NOTES</span></span>

## <span data-ttu-id="8bc34-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bc34-132">RELATED LINKS</span></span>

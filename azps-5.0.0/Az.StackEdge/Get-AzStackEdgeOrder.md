---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316907"
---
# <span data-ttu-id="5378a-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="5378a-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="5378a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5378a-102">SYNOPSIS</span></span>
<span data-ttu-id="5378a-103">Получение сведений о заказе для устройства</span><span class="sxs-lookup"><span data-stu-id="5378a-103">Get the order details for a device</span></span>

## <span data-ttu-id="5378a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5378a-104">SYNTAX</span></span>

### <span data-ttu-id="5378a-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5378a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5378a-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5378a-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5378a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5378a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5378a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5378a-108">DESCRIPTION</span></span>
<span data-ttu-id="5378a-109">Командлет **Get-AzStackEdgeOrder** получает сведения о заказе для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="5378a-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="5378a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5378a-110">EXAMPLES</span></span>

### <span data-ttu-id="5378a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5378a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="5378a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5378a-112">PARAMETERS</span></span>

### <span data-ttu-id="5378a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5378a-113">-DefaultProfile</span></span>
<span data-ttu-id="5378a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5378a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5378a-115">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="5378a-115">-DeviceName</span></span>
<span data-ttu-id="5378a-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5378a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="5378a-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5378a-117">-DeviceObject</span></span>
<span data-ttu-id="5378a-118">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="5378a-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5378a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5378a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5378a-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5378a-120">Resource Group Name</span></span>

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

### <span data-ttu-id="5378a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5378a-121">-ResourceId</span></span>
<span data-ttu-id="5378a-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5378a-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="5378a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5378a-123">CommonParameters</span></span>
<span data-ttu-id="5378a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5378a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5378a-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5378a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5378a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5378a-126">INPUTS</span></span>

### <span data-ttu-id="5378a-127">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5378a-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="5378a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5378a-128">System.String</span></span>

## <span data-ttu-id="5378a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5378a-129">OUTPUTS</span></span>

### <span data-ttu-id="5378a-130">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="5378a-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="5378a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5378a-131">NOTES</span></span>

## <span data-ttu-id="5378a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5378a-132">RELATED LINKS</span></span>

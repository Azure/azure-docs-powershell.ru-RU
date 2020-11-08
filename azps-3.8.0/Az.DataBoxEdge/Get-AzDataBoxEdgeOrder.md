---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073419"
---
# <span data-ttu-id="10cdb-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="10cdb-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="10cdb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="10cdb-103">Получение сведений о заказе для устройства</span><span class="sxs-lookup"><span data-stu-id="10cdb-103">Get the order details for a device</span></span>

## <span data-ttu-id="10cdb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10cdb-104">SYNTAX</span></span>

### <span data-ttu-id="10cdb-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10cdb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cdb-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10cdb-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10cdb-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10cdb-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10cdb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10cdb-108">DESCRIPTION</span></span>
<span data-ttu-id="10cdb-109">Командлет **Get-AzDataBoxEdgeOrder** получает сведения о заказе на пограничном устройстве для поля данных.</span><span class="sxs-lookup"><span data-stu-id="10cdb-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="10cdb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10cdb-110">EXAMPLES</span></span>

### <span data-ttu-id="10cdb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10cdb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="10cdb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10cdb-112">PARAMETERS</span></span>

### <span data-ttu-id="10cdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cdb-113">-DefaultProfile</span></span>
<span data-ttu-id="10cdb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10cdb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10cdb-115">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="10cdb-115">-DeviceName</span></span>
<span data-ttu-id="10cdb-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="10cdb-116">Resource Group Name</span></span>

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

### <span data-ttu-id="10cdb-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="10cdb-117">-DeviceObject</span></span>
<span data-ttu-id="10cdb-118">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="10cdb-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="10cdb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10cdb-119">-ResourceGroupName</span></span>
<span data-ttu-id="10cdb-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="10cdb-120">Resource Group Name</span></span>

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

### <span data-ttu-id="10cdb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10cdb-121">-ResourceId</span></span>
<span data-ttu-id="10cdb-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="10cdb-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="10cdb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cdb-123">CommonParameters</span></span>
<span data-ttu-id="10cdb-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10cdb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cdb-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10cdb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cdb-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10cdb-126">INPUTS</span></span>

### <span data-ttu-id="10cdb-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="10cdb-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="10cdb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="10cdb-128">System.String</span></span>

## <span data-ttu-id="10cdb-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10cdb-129">OUTPUTS</span></span>

### <span data-ttu-id="10cdb-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="10cdb-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="10cdb-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="10cdb-131">NOTES</span></span>

## <span data-ttu-id="10cdb-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10cdb-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243837"
---
# <span data-ttu-id="9a1b1-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="9a1b1-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="9a1b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1b1-103">Возвращает доступные общие ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="9a1b1-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="9a1b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a1b1-104">SYNTAX</span></span>

### <span data-ttu-id="9a1b1-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a1b1-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a1b1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1b1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a1b1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1b1-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a1b1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1b1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9a1b1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a1b1-109">DESCRIPTION</span></span>
<span data-ttu-id="9a1b1-110">Командлет **Get-AzStackEdgeShare** получает доступные общие ресурсы для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="9a1b1-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="9a1b1-111">Если указано имя, будет получен общий доступ по имени.</span><span class="sxs-lookup"><span data-stu-id="9a1b1-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="9a1b1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a1b1-112">EXAMPLES</span></span>

### <span data-ttu-id="9a1b1-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a1b1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="9a1b1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a1b1-114">PARAMETERS</span></span>

### <span data-ttu-id="9a1b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1b1-115">-DefaultProfile</span></span>
<span data-ttu-id="9a1b1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a1b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a1b1-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="9a1b1-117">-DeviceName</span></span>
<span data-ttu-id="9a1b1-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="9a1b1-118">Device Name</span></span>

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

### <span data-ttu-id="9a1b1-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9a1b1-119">-DeviceObject</span></span>
<span data-ttu-id="9a1b1-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="9a1b1-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="9a1b1-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a1b1-121">-Name</span></span>
<span data-ttu-id="9a1b1-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="9a1b1-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a1b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="9a1b1-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9a1b1-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9a1b1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a1b1-125">-ResourceId</span></span>
<span data-ttu-id="9a1b1-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a1b1-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="9a1b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1b1-127">CommonParameters</span></span>
<span data-ttu-id="9a1b1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a1b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1b1-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a1b1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1b1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a1b1-130">INPUTS</span></span>

### <span data-ttu-id="9a1b1-131">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9a1b1-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="9a1b1-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a1b1-132">OUTPUTS</span></span>

### <span data-ttu-id="9a1b1-133">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="9a1b1-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="9a1b1-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a1b1-134">NOTES</span></span>

## <span data-ttu-id="9a1b1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a1b1-135">RELATED LINKS</span></span>

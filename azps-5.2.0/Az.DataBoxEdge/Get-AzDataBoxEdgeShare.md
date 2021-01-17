---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412372"
---
# <span data-ttu-id="a3abf-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a3abf-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="a3abf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3abf-102">SYNOPSIS</span></span>
<span data-ttu-id="a3abf-103">Возвращает доступные акции для устройства.</span><span class="sxs-lookup"><span data-stu-id="a3abf-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="a3abf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3abf-104">SYNTAX</span></span>

### <span data-ttu-id="a3abf-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3abf-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3abf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3abf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3abf-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3abf-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3abf-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3abf-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a3abf-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3abf-109">DESCRIPTION</span></span>
<span data-ttu-id="a3abf-110">Для устройства Edge Data Box доступны все доступные акции для **get-AzDataBoxEdgeShare.**</span><span class="sxs-lookup"><span data-stu-id="a3abf-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="a3abf-111">Если у вас есть имя, это позволит получить обойму по имени.</span><span class="sxs-lookup"><span data-stu-id="a3abf-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="a3abf-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3abf-112">EXAMPLES</span></span>

### <span data-ttu-id="a3abf-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3abf-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="a3abf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3abf-114">PARAMETERS</span></span>

### <span data-ttu-id="a3abf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3abf-115">-DefaultProfile</span></span>
<span data-ttu-id="a3abf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3abf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3abf-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a3abf-117">-DeviceName</span></span>
<span data-ttu-id="a3abf-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="a3abf-118">Device Name</span></span>

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

### <span data-ttu-id="a3abf-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a3abf-119">-DeviceObject</span></span>
<span data-ttu-id="a3abf-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="a3abf-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a3abf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3abf-121">-Name</span></span>
<span data-ttu-id="a3abf-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="a3abf-122">Resource Name</span></span>

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

### <span data-ttu-id="a3abf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3abf-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3abf-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3abf-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a3abf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3abf-125">-ResourceId</span></span>
<span data-ttu-id="a3abf-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3abf-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a3abf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3abf-127">CommonParameters</span></span>
<span data-ttu-id="a3abf-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3abf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3abf-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3abf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3abf-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3abf-130">INPUTS</span></span>

### <span data-ttu-id="a3abf-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a3abf-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a3abf-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3abf-132">OUTPUTS</span></span>

### <span data-ttu-id="a3abf-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a3abf-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="a3abf-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3abf-134">NOTES</span></span>

## <span data-ttu-id="a3abf-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3abf-135">RELATED LINKS</span></span>

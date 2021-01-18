---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504963"
---
# <span data-ttu-id="ac1f6-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ac1f6-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="ac1f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1f6-103">Возвращает доступные акции для устройства.</span><span class="sxs-lookup"><span data-stu-id="ac1f6-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="ac1f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac1f6-104">SYNTAX</span></span>

### <span data-ttu-id="ac1f6-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac1f6-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac1f6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac1f6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac1f6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac1f6-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac1f6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac1f6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ac1f6-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac1f6-109">DESCRIPTION</span></span>
<span data-ttu-id="ac1f6-110">Для устройства Stack Edge доступны все доступные акции для **get-AzStackEdgeShare.**</span><span class="sxs-lookup"><span data-stu-id="ac1f6-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="ac1f6-111">Если у вас есть имя, это позволит получить обойму по имени.</span><span class="sxs-lookup"><span data-stu-id="ac1f6-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="ac1f6-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac1f6-112">EXAMPLES</span></span>

### <span data-ttu-id="ac1f6-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac1f6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="ac1f6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac1f6-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1f6-115">-DefaultProfile</span></span>
<span data-ttu-id="ac1f6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac1f6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ac1f6-117">-DeviceName</span></span>
<span data-ttu-id="ac1f6-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="ac1f6-118">Device Name</span></span>

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

### <span data-ttu-id="ac1f6-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ac1f6-119">-DeviceObject</span></span>
<span data-ttu-id="ac1f6-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="ac1f6-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="ac1f6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ac1f6-121">-Name</span></span>
<span data-ttu-id="ac1f6-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="ac1f6-122">Resource Name</span></span>

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

### <span data-ttu-id="ac1f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac1f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac1f6-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ac1f6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ac1f6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac1f6-125">-ResourceId</span></span>
<span data-ttu-id="ac1f6-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac1f6-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="ac1f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1f6-127">CommonParameters</span></span>
<span data-ttu-id="ac1f6-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1f6-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac1f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1f6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac1f6-130">INPUTS</span></span>

### <span data-ttu-id="ac1f6-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ac1f6-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ac1f6-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac1f6-132">OUTPUTS</span></span>

### <span data-ttu-id="ac1f6-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ac1f6-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="ac1f6-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac1f6-134">NOTES</span></span>

## <span data-ttu-id="ac1f6-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac1f6-135">RELATED LINKS</span></span>

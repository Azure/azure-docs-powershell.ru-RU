---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410271"
---
# <span data-ttu-id="64647-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="64647-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="64647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64647-102">SYNOPSIS</span></span>
<span data-ttu-id="64647-103">Возвращает доступные акции для устройства.</span><span class="sxs-lookup"><span data-stu-id="64647-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="64647-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64647-104">SYNTAX</span></span>

### <span data-ttu-id="64647-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64647-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64647-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64647-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64647-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64647-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64647-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64647-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="64647-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64647-109">DESCRIPTION</span></span>
<span data-ttu-id="64647-110">Для устройства Stack Edge доступны все доступные акции для **get-AzStackEdgeShare.**</span><span class="sxs-lookup"><span data-stu-id="64647-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="64647-111">Если у вас есть имя, это позволит получить обойму по имени.</span><span class="sxs-lookup"><span data-stu-id="64647-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="64647-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64647-112">EXAMPLES</span></span>

### <span data-ttu-id="64647-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64647-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="64647-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64647-114">PARAMETERS</span></span>

### <span data-ttu-id="64647-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64647-115">-DefaultProfile</span></span>
<span data-ttu-id="64647-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64647-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64647-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="64647-117">-DeviceName</span></span>
<span data-ttu-id="64647-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="64647-118">Device Name</span></span>

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

### <span data-ttu-id="64647-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="64647-119">-DeviceObject</span></span>
<span data-ttu-id="64647-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="64647-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="64647-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64647-121">-Name</span></span>
<span data-ttu-id="64647-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="64647-122">Resource Name</span></span>

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

### <span data-ttu-id="64647-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64647-123">-ResourceGroupName</span></span>
<span data-ttu-id="64647-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="64647-124">Resource Group Name</span></span>

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

### <span data-ttu-id="64647-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64647-125">-ResourceId</span></span>
<span data-ttu-id="64647-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="64647-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="64647-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64647-127">CommonParameters</span></span>
<span data-ttu-id="64647-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64647-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64647-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64647-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64647-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64647-130">INPUTS</span></span>

### <span data-ttu-id="64647-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="64647-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="64647-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64647-132">OUTPUTS</span></span>

### <span data-ttu-id="64647-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="64647-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="64647-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64647-134">NOTES</span></span>

## <span data-ttu-id="64647-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64647-135">RELATED LINKS</span></span>

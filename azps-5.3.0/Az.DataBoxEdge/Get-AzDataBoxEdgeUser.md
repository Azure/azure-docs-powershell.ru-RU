---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519093"
---
# <span data-ttu-id="28dfd-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="28dfd-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="28dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="28dfd-103">Настраивает пользователей для устройства.</span><span class="sxs-lookup"><span data-stu-id="28dfd-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="28dfd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28dfd-104">SYNTAX</span></span>

### <span data-ttu-id="28dfd-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28dfd-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28dfd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dfd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28dfd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dfd-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28dfd-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dfd-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="28dfd-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28dfd-109">DESCRIPTION</span></span>
<span data-ttu-id="28dfd-110">В **этом списке перечислены** пользователи, настроенные для устройства Edge data Box.</span><span class="sxs-lookup"><span data-stu-id="28dfd-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="28dfd-111">Вы можете упомянуть имя в параметрах, чтобы получить сведения о конкретном пользователе.</span><span class="sxs-lookup"><span data-stu-id="28dfd-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="28dfd-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28dfd-112">EXAMPLES</span></span>

### <span data-ttu-id="28dfd-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28dfd-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="28dfd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28dfd-114">PARAMETERS</span></span>

### <span data-ttu-id="28dfd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28dfd-115">-DefaultProfile</span></span>
<span data-ttu-id="28dfd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28dfd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28dfd-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="28dfd-117">-DeviceName</span></span>
<span data-ttu-id="28dfd-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="28dfd-118">Device Name</span></span>

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

### <span data-ttu-id="28dfd-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="28dfd-119">-DeviceObject</span></span>
<span data-ttu-id="28dfd-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="28dfd-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="28dfd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28dfd-121">-Name</span></span>
<span data-ttu-id="28dfd-122">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="28dfd-122">Username</span></span>

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

### <span data-ttu-id="28dfd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28dfd-123">-ResourceGroupName</span></span>
<span data-ttu-id="28dfd-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="28dfd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="28dfd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28dfd-125">-ResourceId</span></span>
<span data-ttu-id="28dfd-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="28dfd-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="28dfd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28dfd-127">CommonParameters</span></span>
<span data-ttu-id="28dfd-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28dfd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28dfd-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28dfd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28dfd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28dfd-130">INPUTS</span></span>

### <span data-ttu-id="28dfd-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="28dfd-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="28dfd-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28dfd-132">OUTPUTS</span></span>

### <span data-ttu-id="28dfd-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="28dfd-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="28dfd-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28dfd-134">NOTES</span></span>

## <span data-ttu-id="28dfd-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28dfd-135">RELATED LINKS</span></span>

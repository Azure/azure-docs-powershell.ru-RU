---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507985"
---
# <span data-ttu-id="4af21-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4af21-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="4af21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4af21-102">SYNOPSIS</span></span>
<span data-ttu-id="4af21-103">Настраивает пользователей для устройства.</span><span class="sxs-lookup"><span data-stu-id="4af21-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="4af21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4af21-104">SYNTAX</span></span>

### <span data-ttu-id="4af21-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4af21-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af21-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4af21-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af21-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4af21-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af21-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4af21-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="4af21-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af21-109">DESCRIPTION</span></span>
<span data-ttu-id="4af21-110">В **этом списке перечислены** пользователи, настроенные для устройства Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="4af21-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="4af21-111">Вы можете упомянуть имя в параметрах, чтобы получить сведения о конкретном пользователе.</span><span class="sxs-lookup"><span data-stu-id="4af21-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="4af21-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4af21-112">EXAMPLES</span></span>

### <span data-ttu-id="4af21-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4af21-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="4af21-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4af21-114">PARAMETERS</span></span>

### <span data-ttu-id="4af21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af21-115">-DefaultProfile</span></span>
<span data-ttu-id="4af21-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4af21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4af21-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4af21-117">-DeviceName</span></span>
<span data-ttu-id="4af21-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="4af21-118">Device Name</span></span>

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

### <span data-ttu-id="4af21-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4af21-119">-DeviceObject</span></span>
<span data-ttu-id="4af21-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="4af21-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="4af21-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4af21-121">-Name</span></span>
<span data-ttu-id="4af21-122">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="4af21-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4af21-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af21-123">-ResourceGroupName</span></span>
<span data-ttu-id="4af21-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4af21-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4af21-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4af21-125">-ResourceId</span></span>
<span data-ttu-id="4af21-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4af21-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="4af21-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af21-127">CommonParameters</span></span>
<span data-ttu-id="4af21-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af21-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af21-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4af21-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af21-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4af21-130">INPUTS</span></span>

### <span data-ttu-id="4af21-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4af21-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="4af21-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4af21-132">OUTPUTS</span></span>

### <span data-ttu-id="4af21-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4af21-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="4af21-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4af21-134">NOTES</span></span>

## <span data-ttu-id="4af21-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4af21-135">RELATED LINKS</span></span>
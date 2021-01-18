---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518617"
---
# <span data-ttu-id="312ba-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="312ba-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="312ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="312ba-102">SYNOPSIS</span></span>
<span data-ttu-id="312ba-103">Распечатайте список устройств, которые назначены ребенку, разделенные запятой.</span><span class="sxs-lookup"><span data-stu-id="312ba-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="312ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="312ba-104">SYNTAX</span></span>

### <span data-ttu-id="312ba-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="312ba-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="312ba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="312ba-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="312ba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="312ba-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="312ba-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="312ba-108">DESCRIPTION</span></span>
<span data-ttu-id="312ba-109">Откажите все устройства, не правительственные, в список всех устройств с разделами-запятой или указанное устройство.</span><span class="sxs-lookup"><span data-stu-id="312ba-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="312ba-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="312ba-110">EXAMPLES</span></span>

### <span data-ttu-id="312ba-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="312ba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="312ba-112">Откажите все устройства, не соответствующие границам, в список с разделами-запятами.</span><span class="sxs-lookup"><span data-stu-id="312ba-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="312ba-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="312ba-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="312ba-114">Откажите все устройства, не правительственные, в список всех устройств, не влияя на границы, с разделив их запятой.</span><span class="sxs-lookup"><span data-stu-id="312ba-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="312ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="312ba-115">PARAMETERS</span></span>

### <span data-ttu-id="312ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312ba-116">-DefaultProfile</span></span>
<span data-ttu-id="312ba-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="312ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="312ba-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="312ba-118">-DeviceId</span></span>
<span data-ttu-id="312ba-119">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="312ba-119">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312ba-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="312ba-120">-InputObject</span></span>
<span data-ttu-id="312ba-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="312ba-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="312ba-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="312ba-122">-IotHubName</span></span>
<span data-ttu-id="312ba-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="312ba-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="312ba-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="312ba-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="312ba-126">-ResourceId</span></span>
<span data-ttu-id="312ba-127">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="312ba-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312ba-128">CommonParameters</span></span>
<span data-ttu-id="312ba-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="312ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312ba-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="312ba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312ba-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="312ba-131">INPUTS</span></span>

### <span data-ttu-id="312ba-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="312ba-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="312ba-133">System.String</span><span class="sxs-lookup"><span data-stu-id="312ba-133">System.String</span></span>

## <span data-ttu-id="312ba-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="312ba-134">OUTPUTS</span></span>

### <span data-ttu-id="312ba-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Темы</span><span class="sxs-lookup"><span data-stu-id="312ba-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="312ba-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices Темы[]</span><span class="sxs-lookup"><span data-stu-id="312ba-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="312ba-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="312ba-137">NOTES</span></span>

## <span data-ttu-id="312ba-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="312ba-138">RELATED LINKS</span></span>

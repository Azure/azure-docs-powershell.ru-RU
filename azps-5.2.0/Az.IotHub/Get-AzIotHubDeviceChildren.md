---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391111"
---
# <span data-ttu-id="5f99f-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="5f99f-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="5f99f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f99f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f99f-103">Распечатайте список устройств, которые назначены ребенку, разделенные запятой.</span><span class="sxs-lookup"><span data-stu-id="5f99f-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="5f99f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f99f-104">SYNTAX</span></span>

### <span data-ttu-id="5f99f-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f99f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f99f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5f99f-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f99f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5f99f-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f99f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f99f-108">DESCRIPTION</span></span>
<span data-ttu-id="5f99f-109">Показать все устройства, не правительственные службы, в качестве списка всех устройств с раздельными запятой или указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="5f99f-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="5f99f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f99f-110">EXAMPLES</span></span>

### <span data-ttu-id="5f99f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f99f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="5f99f-112">Откажите все устройства, не соответствующие границам, в список с разделами-запятами.</span><span class="sxs-lookup"><span data-stu-id="5f99f-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="5f99f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5f99f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="5f99f-114">Откажите все назначенные вне границы устройства в качестве списка всех устройств с разделиными запятой.</span><span class="sxs-lookup"><span data-stu-id="5f99f-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="5f99f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f99f-115">PARAMETERS</span></span>

### <span data-ttu-id="5f99f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f99f-116">-DefaultProfile</span></span>
<span data-ttu-id="5f99f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f99f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f99f-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5f99f-118">-DeviceId</span></span>
<span data-ttu-id="5f99f-119">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="5f99f-119">Id of edge device.</span></span>

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

### <span data-ttu-id="5f99f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f99f-120">-InputObject</span></span>
<span data-ttu-id="5f99f-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="5f99f-121">IotHub object</span></span>

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

### <span data-ttu-id="5f99f-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5f99f-122">-IotHubName</span></span>
<span data-ttu-id="5f99f-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="5f99f-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5f99f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f99f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f99f-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5f99f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5f99f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f99f-126">-ResourceId</span></span>
<span data-ttu-id="5f99f-127">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="5f99f-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5f99f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f99f-128">CommonParameters</span></span>
<span data-ttu-id="5f99f-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f99f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f99f-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f99f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f99f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f99f-131">INPUTS</span></span>

### <span data-ttu-id="5f99f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5f99f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5f99f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5f99f-133">System.String</span></span>

## <span data-ttu-id="5f99f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f99f-134">OUTPUTS</span></span>

### <span data-ttu-id="5f99f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Темы</span><span class="sxs-lookup"><span data-stu-id="5f99f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="5f99f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices Темы[]</span><span class="sxs-lookup"><span data-stu-id="5f99f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="5f99f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f99f-137">NOTES</span></span>

## <span data-ttu-id="5f99f-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f99f-138">RELATED LINKS</span></span>

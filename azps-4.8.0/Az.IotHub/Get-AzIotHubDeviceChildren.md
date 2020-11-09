---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243555"
---
# <span data-ttu-id="c9ceb-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="c9ceb-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="c9ceb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ceb-103">Распечатайте список выделенных дочерних устройств, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="c9ceb-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="c9ceb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9ceb-104">SYNTAX</span></span>

### <span data-ttu-id="c9ceb-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9ceb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9ceb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c9ceb-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9ceb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c9ceb-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ceb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9ceb-108">DESCRIPTION</span></span>
<span data-ttu-id="c9ceb-109">Показать все назначенные пограничные устройства как список всех пограничных устройств или указанное устройство, разделенные запятыми.</span><span class="sxs-lookup"><span data-stu-id="c9ceb-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="c9ceb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9ceb-110">EXAMPLES</span></span>

### <span data-ttu-id="c9ceb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9ceb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="c9ceb-112">Показывать все назначенные устройства, кроме пограничного, в виде списка с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="c9ceb-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="c9ceb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c9ceb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="c9ceb-114">Показать все назначенные пограничные устройства как список всех пограничных устройств, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="c9ceb-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="c9ceb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9ceb-115">PARAMETERS</span></span>

### <span data-ttu-id="c9ceb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ceb-116">-DefaultProfile</span></span>
<span data-ttu-id="c9ceb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ceb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9ceb-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c9ceb-118">-DeviceId</span></span>
<span data-ttu-id="c9ceb-119">Идентификатор устройства Edge.</span><span class="sxs-lookup"><span data-stu-id="c9ceb-119">Id of edge device.</span></span>

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

### <span data-ttu-id="c9ceb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9ceb-120">-InputObject</span></span>
<span data-ttu-id="c9ceb-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="c9ceb-121">IotHub object</span></span>

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

### <span data-ttu-id="c9ceb-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c9ceb-122">-IotHubName</span></span>
<span data-ttu-id="c9ceb-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="c9ceb-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c9ceb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ceb-124">-ResourceGroupName</span></span>
<span data-ttu-id="c9ceb-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c9ceb-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c9ceb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9ceb-126">-ResourceId</span></span>
<span data-ttu-id="c9ceb-127">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="c9ceb-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c9ceb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ceb-128">CommonParameters</span></span>
<span data-ttu-id="c9ceb-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9ceb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ceb-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ceb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ceb-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9ceb-131">INPUTS</span></span>

### <span data-ttu-id="c9ceb-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c9ceb-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c9ceb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c9ceb-133">System.String</span></span>

## <span data-ttu-id="c9ceb-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9ceb-134">OUTPUTS</span></span>

### <span data-ttu-id="c9ceb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="c9ceb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="c9ceb-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="c9ceb-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="c9ceb-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9ceb-137">NOTES</span></span>

## <span data-ttu-id="c9ceb-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9ceb-138">RELATED LINKS</span></span>
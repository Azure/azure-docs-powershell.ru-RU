---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518613"
---
# <span data-ttu-id="6f428-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="6f428-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="6f428-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f428-102">SYNOPSIS</span></span>
<span data-ttu-id="6f428-103">Получите параметры распределенной трассии для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f428-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6f428-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f428-104">SYNTAX</span></span>

### <span data-ttu-id="6f428-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f428-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f428-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f428-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f428-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f428-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f428-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f428-108">DESCRIPTION</span></span>
<span data-ttu-id="6f428-109">Получите параметры распределенной трассии для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f428-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6f428-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f428-110">EXAMPLES</span></span>

### <span data-ttu-id="6f428-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f428-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="6f428-112">Получите параметры распределенной трассии для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f428-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6f428-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f428-113">PARAMETERS</span></span>

### <span data-ttu-id="6f428-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f428-114">-DefaultProfile</span></span>
<span data-ttu-id="6f428-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f428-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f428-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6f428-116">-DeviceId</span></span>
<span data-ttu-id="6f428-117">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="6f428-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f428-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f428-118">-InputObject</span></span>
<span data-ttu-id="6f428-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="6f428-119">IotHub object</span></span>

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

### <span data-ttu-id="6f428-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6f428-120">-IotHubName</span></span>
<span data-ttu-id="6f428-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="6f428-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6f428-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f428-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f428-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6f428-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6f428-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f428-124">-ResourceId</span></span>
<span data-ttu-id="6f428-125">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="6f428-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6f428-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f428-126">CommonParameters</span></span>
<span data-ttu-id="6f428-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f428-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f428-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f428-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f428-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f428-129">INPUTS</span></span>

### <span data-ttu-id="6f428-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6f428-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6f428-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6f428-131">System.String</span></span>

## <span data-ttu-id="6f428-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f428-132">OUTPUTS</span></span>

### <span data-ttu-id="6f428-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="6f428-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="6f428-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f428-134">NOTES</span></span>

## <span data-ttu-id="6f428-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f428-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 45966042a2c2c6a660f052280039204a1d5eb908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988028"
---
# <span data-ttu-id="7da38-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7da38-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="7da38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da38-102">SYNOPSIS</span></span>
<span data-ttu-id="7da38-103">Возвращает дейс.</span><span class="sxs-lookup"><span data-stu-id="7da38-103">Gets a device twin.</span></span>

## <span data-ttu-id="7da38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7da38-104">SYNTAX</span></span>

### <span data-ttu-id="7da38-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7da38-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7da38-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7da38-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7da38-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7da38-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7da38-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7da38-108">DESCRIPTION</span></span>
<span data-ttu-id="7da38-109">Возвращает дейс.</span><span class="sxs-lookup"><span data-stu-id="7da38-109">Gets a device twin.</span></span> <span data-ttu-id="7da38-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="7da38-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="7da38-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7da38-111">EXAMPLES</span></span>

### <span data-ttu-id="7da38-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7da38-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="7da38-113">Возвращает объект "устройство".</span><span class="sxs-lookup"><span data-stu-id="7da38-113">Returns the device twin object.</span></span>

## <span data-ttu-id="7da38-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7da38-114">PARAMETERS</span></span>

### <span data-ttu-id="7da38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da38-115">-DefaultProfile</span></span>
<span data-ttu-id="7da38-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7da38-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7da38-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7da38-117">-DeviceId</span></span>
<span data-ttu-id="7da38-118">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="7da38-118">Target Device Id.</span></span>

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

### <span data-ttu-id="7da38-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7da38-119">-InputObject</span></span>
<span data-ttu-id="7da38-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="7da38-120">IotHub object</span></span>

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

### <span data-ttu-id="7da38-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7da38-121">-IotHubName</span></span>
<span data-ttu-id="7da38-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="7da38-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7da38-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da38-123">-ResourceGroupName</span></span>
<span data-ttu-id="7da38-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7da38-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7da38-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7da38-125">-ResourceId</span></span>
<span data-ttu-id="7da38-126">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="7da38-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7da38-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da38-127">CommonParameters</span></span>
<span data-ttu-id="7da38-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da38-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da38-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da38-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da38-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7da38-130">INPUTS</span></span>

### <span data-ttu-id="7da38-131">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7da38-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7da38-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7da38-132">System.String</span></span>

## <span data-ttu-id="7da38-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7da38-133">OUTPUTS</span></span>

### <span data-ttu-id="7da38-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7da38-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="7da38-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7da38-135">NOTES</span></span>

## <span data-ttu-id="7da38-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7da38-136">RELATED LINKS</span></span>

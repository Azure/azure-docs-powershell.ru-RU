---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391103"
---
# <span data-ttu-id="760d3-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="760d3-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="760d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="760d3-102">SYNOPSIS</span></span>
<span data-ttu-id="760d3-103">Возвращает дейс.</span><span class="sxs-lookup"><span data-stu-id="760d3-103">Gets a device twin.</span></span>

## <span data-ttu-id="760d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="760d3-104">SYNTAX</span></span>

### <span data-ttu-id="760d3-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="760d3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="760d3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="760d3-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="760d3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="760d3-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="760d3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="760d3-108">DESCRIPTION</span></span>
<span data-ttu-id="760d3-109">Возвращает дейс.</span><span class="sxs-lookup"><span data-stu-id="760d3-109">Gets a device twin.</span></span> <span data-ttu-id="760d3-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="760d3-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="760d3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="760d3-111">EXAMPLES</span></span>

### <span data-ttu-id="760d3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="760d3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="760d3-113">Возвращает объект "устройство".</span><span class="sxs-lookup"><span data-stu-id="760d3-113">Returns the device twin object.</span></span>

## <span data-ttu-id="760d3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="760d3-114">PARAMETERS</span></span>

### <span data-ttu-id="760d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="760d3-115">-DefaultProfile</span></span>
<span data-ttu-id="760d3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="760d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="760d3-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="760d3-117">-DeviceId</span></span>
<span data-ttu-id="760d3-118">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="760d3-118">Target Device Id.</span></span>

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

### <span data-ttu-id="760d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="760d3-119">-InputObject</span></span>
<span data-ttu-id="760d3-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="760d3-120">IotHub object</span></span>

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

### <span data-ttu-id="760d3-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="760d3-121">-IotHubName</span></span>
<span data-ttu-id="760d3-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="760d3-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="760d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="760d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="760d3-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="760d3-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="760d3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="760d3-125">-ResourceId</span></span>
<span data-ttu-id="760d3-126">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="760d3-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="760d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760d3-127">CommonParameters</span></span>
<span data-ttu-id="760d3-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="760d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760d3-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="760d3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760d3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="760d3-130">INPUTS</span></span>

### <span data-ttu-id="760d3-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="760d3-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="760d3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="760d3-132">System.String</span></span>

## <span data-ttu-id="760d3-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="760d3-133">OUTPUTS</span></span>

### <span data-ttu-id="760d3-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="760d3-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="760d3-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="760d3-135">NOTES</span></span>

## <span data-ttu-id="760d3-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="760d3-136">RELATED LINKS</span></span>

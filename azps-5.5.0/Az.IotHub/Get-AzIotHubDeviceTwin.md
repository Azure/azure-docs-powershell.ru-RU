---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219788"
---
# <span data-ttu-id="62564-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="62564-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="62564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62564-102">SYNOPSIS</span></span>
<span data-ttu-id="62564-103">Возвращает дейс.</span><span class="sxs-lookup"><span data-stu-id="62564-103">Gets a device twin.</span></span>

## <span data-ttu-id="62564-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62564-104">SYNTAX</span></span>

### <span data-ttu-id="62564-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62564-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62564-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62564-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62564-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62564-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62564-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62564-108">DESCRIPTION</span></span>
<span data-ttu-id="62564-109">Возвращает дейс.</span><span class="sxs-lookup"><span data-stu-id="62564-109">Gets a device twin.</span></span> <span data-ttu-id="62564-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="62564-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="62564-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62564-111">EXAMPLES</span></span>

### <span data-ttu-id="62564-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62564-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="62564-113">Возвращает объект "устройство".</span><span class="sxs-lookup"><span data-stu-id="62564-113">Returns the device twin object.</span></span>

## <span data-ttu-id="62564-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62564-114">PARAMETERS</span></span>

### <span data-ttu-id="62564-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62564-115">-DefaultProfile</span></span>
<span data-ttu-id="62564-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62564-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62564-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="62564-117">-DeviceId</span></span>
<span data-ttu-id="62564-118">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="62564-118">Target Device Id.</span></span>

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

### <span data-ttu-id="62564-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62564-119">-InputObject</span></span>
<span data-ttu-id="62564-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="62564-120">IotHub object</span></span>

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

### <span data-ttu-id="62564-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62564-121">-IotHubName</span></span>
<span data-ttu-id="62564-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="62564-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62564-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62564-123">-ResourceGroupName</span></span>
<span data-ttu-id="62564-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="62564-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62564-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62564-125">-ResourceId</span></span>
<span data-ttu-id="62564-126">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="62564-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62564-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62564-127">CommonParameters</span></span>
<span data-ttu-id="62564-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62564-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62564-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62564-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62564-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62564-130">INPUTS</span></span>

### <span data-ttu-id="62564-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="62564-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62564-132">System.String</span><span class="sxs-lookup"><span data-stu-id="62564-132">System.String</span></span>

## <span data-ttu-id="62564-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62564-133">OUTPUTS</span></span>

### <span data-ttu-id="62564-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="62564-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="62564-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62564-135">NOTES</span></span>

## <span data-ttu-id="62564-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62564-136">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 915fdf5bd0e53e7e8ed2817d83438597d515007d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987930"
---
# <span data-ttu-id="ca77d-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="ca77d-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="ca77d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca77d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca77d-103">Возвращает модуль устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="ca77d-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="ca77d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca77d-104">SYNTAX</span></span>

### <span data-ttu-id="ca77d-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca77d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca77d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca77d-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca77d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca77d-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca77d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca77d-108">DESCRIPTION</span></span>
<span data-ttu-id="ca77d-109">Возвращает модуль устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="ca77d-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="ca77d-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="ca77d-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="ca77d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca77d-111">EXAMPLES</span></span>

### <span data-ttu-id="ca77d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca77d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="ca77d-113">Возвращает объект module device.</span><span class="sxs-lookup"><span data-stu-id="ca77d-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="ca77d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca77d-114">PARAMETERS</span></span>

### <span data-ttu-id="ca77d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca77d-115">-DefaultProfile</span></span>
<span data-ttu-id="ca77d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca77d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca77d-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ca77d-117">-DeviceId</span></span>
<span data-ttu-id="ca77d-118">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="ca77d-118">Target Device Id.</span></span>

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

### <span data-ttu-id="ca77d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca77d-119">-InputObject</span></span>
<span data-ttu-id="ca77d-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="ca77d-120">IotHub object</span></span>

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

### <span data-ttu-id="ca77d-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ca77d-121">-IotHubName</span></span>
<span data-ttu-id="ca77d-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="ca77d-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ca77d-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="ca77d-123">-ModuleId</span></span>
<span data-ttu-id="ca77d-124">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="ca77d-124">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca77d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca77d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca77d-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ca77d-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ca77d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca77d-127">-ResourceId</span></span>
<span data-ttu-id="ca77d-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="ca77d-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ca77d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca77d-129">CommonParameters</span></span>
<span data-ttu-id="ca77d-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca77d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca77d-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca77d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca77d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca77d-132">INPUTS</span></span>

### <span data-ttu-id="ca77d-133">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ca77d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ca77d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ca77d-134">System.String</span></span>

## <span data-ttu-id="ca77d-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca77d-135">OUTPUTS</span></span>

### <span data-ttu-id="ca77d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="ca77d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="ca77d-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca77d-137">NOTES</span></span>

## <span data-ttu-id="ca77d-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca77d-138">RELATED LINKS</span></span>

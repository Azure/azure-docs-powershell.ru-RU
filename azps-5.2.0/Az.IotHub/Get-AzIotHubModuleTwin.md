---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407023"
---
# <span data-ttu-id="a4514-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a4514-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="a4514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4514-102">SYNOPSIS</span></span>
<span data-ttu-id="a4514-103">Возвращает модуль устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="a4514-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="a4514-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4514-104">SYNTAX</span></span>

### <span data-ttu-id="a4514-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4514-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4514-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4514-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4514-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4514-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4514-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4514-108">DESCRIPTION</span></span>
<span data-ttu-id="a4514-109">Возвращает модуль устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="a4514-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="a4514-110">Дополнительные https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="a4514-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="a4514-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4514-111">EXAMPLES</span></span>

### <span data-ttu-id="a4514-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4514-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="a4514-113">Возвращает объект module device.</span><span class="sxs-lookup"><span data-stu-id="a4514-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="a4514-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4514-114">PARAMETERS</span></span>

### <span data-ttu-id="a4514-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4514-115">-DefaultProfile</span></span>
<span data-ttu-id="a4514-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4514-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4514-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a4514-117">-DeviceId</span></span>
<span data-ttu-id="a4514-118">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="a4514-118">Target Device Id.</span></span>

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

### <span data-ttu-id="a4514-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4514-119">-InputObject</span></span>
<span data-ttu-id="a4514-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="a4514-120">IotHub object</span></span>

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

### <span data-ttu-id="a4514-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a4514-121">-IotHubName</span></span>
<span data-ttu-id="a4514-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="a4514-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a4514-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="a4514-123">-ModuleId</span></span>
<span data-ttu-id="a4514-124">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="a4514-124">Target Module Id.</span></span>

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

### <span data-ttu-id="a4514-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4514-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4514-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a4514-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a4514-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4514-127">-ResourceId</span></span>
<span data-ttu-id="a4514-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="a4514-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a4514-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4514-129">CommonParameters</span></span>
<span data-ttu-id="a4514-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4514-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4514-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4514-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4514-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4514-132">INPUTS</span></span>

### <span data-ttu-id="a4514-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a4514-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a4514-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a4514-134">System.String</span></span>

## <span data-ttu-id="a4514-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4514-135">OUTPUTS</span></span>

### <span data-ttu-id="a4514-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a4514-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="a4514-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4514-137">NOTES</span></span>

## <span data-ttu-id="a4514-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4514-138">RELATED LINKS</span></span>

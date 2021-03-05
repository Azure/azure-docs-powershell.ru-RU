---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: b50d0b493243a07632403890d0324fefaba7dc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988123"
---
# <span data-ttu-id="18af9-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="18af9-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="18af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18af9-102">SYNOPSIS</span></span>
<span data-ttu-id="18af9-103">Здесь перечислены все или конкретная конфигурация автоматического управления устройствами в режиме IoT.</span><span class="sxs-lookup"><span data-stu-id="18af9-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="18af9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18af9-104">SYNTAX</span></span>

### <span data-ttu-id="18af9-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18af9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18af9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="18af9-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18af9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="18af9-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18af9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18af9-108">DESCRIPTION</span></span>
<span data-ttu-id="18af9-109">Сведения о настройке автоматического управления устройствами в режиме IoT или списке конфигураций автоматического управления устройствами в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="18af9-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="18af9-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="18af9-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="18af9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18af9-111">EXAMPLES</span></span>

### <span data-ttu-id="18af9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18af9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="18af9-113">Получите сведения о настройке автоматического управления устройствами в режиме IoT.</span><span class="sxs-lookup"><span data-stu-id="18af9-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="18af9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="18af9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="18af9-115">Автоматические настройки управления устройствами со списком IoT в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="18af9-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="18af9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18af9-116">PARAMETERS</span></span>

### <span data-ttu-id="18af9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18af9-117">-DefaultProfile</span></span>
<span data-ttu-id="18af9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18af9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18af9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18af9-119">-InputObject</span></span>
<span data-ttu-id="18af9-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="18af9-120">IotHub object</span></span>

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

### <span data-ttu-id="18af9-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="18af9-121">-IotHubName</span></span>
<span data-ttu-id="18af9-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="18af9-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="18af9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="18af9-123">-Name</span></span>
<span data-ttu-id="18af9-124">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="18af9-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="18af9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18af9-125">-ResourceGroupName</span></span>
<span data-ttu-id="18af9-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="18af9-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="18af9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18af9-127">-ResourceId</span></span>
<span data-ttu-id="18af9-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="18af9-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="18af9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18af9-129">CommonParameters</span></span>
<span data-ttu-id="18af9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18af9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18af9-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18af9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18af9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18af9-132">INPUTS</span></span>

### <span data-ttu-id="18af9-133">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="18af9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="18af9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="18af9-134">System.String</span></span>

## <span data-ttu-id="18af9-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18af9-135">OUTPUTS</span></span>

### <span data-ttu-id="18af9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="18af9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="18af9-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="18af9-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="18af9-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18af9-138">NOTES</span></span>

## <span data-ttu-id="18af9-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18af9-139">RELATED LINKS</span></span>

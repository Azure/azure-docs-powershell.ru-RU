---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064920"
---
# <span data-ttu-id="ef16b-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef16b-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="ef16b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef16b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef16b-103">В этой статье перечислены все или некоторые параметры автоматической настройки управления устройствами в IoT.</span><span class="sxs-lookup"><span data-stu-id="ef16b-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="ef16b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef16b-104">SYNTAX</span></span>

### <span data-ttu-id="ef16b-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef16b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef16b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef16b-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef16b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ef16b-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef16b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef16b-108">DESCRIPTION</span></span>
<span data-ttu-id="ef16b-109">Узнайте о том, как настроить автоматическое управление устройствами в Интернет-центре Интернета вещей и включить в него автоматические конфигурации управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="ef16b-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="ef16b-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="ef16b-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="ef16b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef16b-111">EXAMPLES</span></span>

### <span data-ttu-id="ef16b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef16b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="ef16b-113">Получение подробных сведений о настройке автоматического управления устройствами IoT.</span><span class="sxs-lookup"><span data-stu-id="ef16b-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="ef16b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ef16b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="ef16b-115">Список автоматических конфигураций управления устройствами в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="ef16b-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="ef16b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef16b-116">PARAMETERS</span></span>

### <span data-ttu-id="ef16b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef16b-117">-DefaultProfile</span></span>
<span data-ttu-id="ef16b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef16b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef16b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef16b-119">-InputObject</span></span>
<span data-ttu-id="ef16b-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="ef16b-120">IotHub object</span></span>

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

### <span data-ttu-id="ef16b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ef16b-121">-IotHubName</span></span>
<span data-ttu-id="ef16b-122">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="ef16b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ef16b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef16b-123">-Name</span></span>
<span data-ttu-id="ef16b-124">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ef16b-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="ef16b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef16b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef16b-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ef16b-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ef16b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef16b-127">-ResourceId</span></span>
<span data-ttu-id="ef16b-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="ef16b-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ef16b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef16b-129">CommonParameters</span></span>
<span data-ttu-id="ef16b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef16b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef16b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef16b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef16b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef16b-132">INPUTS</span></span>

### <span data-ttu-id="ef16b-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ef16b-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ef16b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ef16b-134">System.String</span></span>

## <span data-ttu-id="ef16b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef16b-135">OUTPUTS</span></span>

### <span data-ttu-id="ef16b-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef16b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="ef16b-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="ef16b-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="ef16b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef16b-138">NOTES</span></span>

## <span data-ttu-id="ef16b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef16b-139">RELATED LINKS</span></span>

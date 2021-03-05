---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 0e9b26b4bd22d167dffbee4449aa811381960732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004131"
---
# <span data-ttu-id="38dfc-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="38dfc-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="38dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="38dfc-103">Обновите обогащение сообщений в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="38dfc-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="38dfc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38dfc-104">SYNTAX</span></span>

### <span data-ttu-id="38dfc-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38dfc-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38dfc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38dfc-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38dfc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38dfc-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38dfc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38dfc-108">DESCRIPTION</span></span>
<span data-ttu-id="38dfc-109">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="38dfc-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="38dfc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38dfc-110">EXAMPLES</span></span>

### <span data-ttu-id="38dfc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38dfc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="38dfc-112">Обновляет значение обогащения на значение updatedValue для ключа "newKey".</span><span class="sxs-lookup"><span data-stu-id="38dfc-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="38dfc-113">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="38dfc-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="38dfc-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="38dfc-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="38dfc-115">Обновляет конечную точку обогащения на "конечная точка1, конечная точка2, конечная точка3" для ключа "newKey".</span><span class="sxs-lookup"><span data-stu-id="38dfc-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="38dfc-116">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="38dfc-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="38dfc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38dfc-117">PARAMETERS</span></span>

### <span data-ttu-id="38dfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38dfc-118">-DefaultProfile</span></span>
<span data-ttu-id="38dfc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38dfc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38dfc-120">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="38dfc-120">-Endpoint</span></span>
<span data-ttu-id="38dfc-121">Конечные точки, к которые нужно применить обогащение.</span><span class="sxs-lookup"><span data-stu-id="38dfc-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dfc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38dfc-122">-InputObject</span></span>
<span data-ttu-id="38dfc-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="38dfc-123">IotHub Object</span></span>

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

### <span data-ttu-id="38dfc-124">-Key</span><span class="sxs-lookup"><span data-stu-id="38dfc-124">-Key</span></span>
<span data-ttu-id="38dfc-125">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="38dfc-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="38dfc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="38dfc-126">-Name</span></span>
<span data-ttu-id="38dfc-127">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="38dfc-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="38dfc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38dfc-128">-ResourceGroupName</span></span>
<span data-ttu-id="38dfc-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="38dfc-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="38dfc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38dfc-130">-ResourceId</span></span>
<span data-ttu-id="38dfc-131">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="38dfc-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="38dfc-132">-Значение</span><span class="sxs-lookup"><span data-stu-id="38dfc-132">-Value</span></span>
<span data-ttu-id="38dfc-133">Стоимость обогащения.</span><span class="sxs-lookup"><span data-stu-id="38dfc-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="38dfc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38dfc-134">-Confirm</span></span>
<span data-ttu-id="38dfc-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="38dfc-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dfc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38dfc-136">-WhatIf</span></span>
<span data-ttu-id="38dfc-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38dfc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38dfc-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38dfc-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dfc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dfc-139">CommonParameters</span></span>
<span data-ttu-id="38dfc-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38dfc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dfc-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38dfc-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dfc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38dfc-142">INPUTS</span></span>

### <span data-ttu-id="38dfc-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="38dfc-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="38dfc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="38dfc-144">System.String</span></span>

## <span data-ttu-id="38dfc-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38dfc-145">OUTPUTS</span></span>

### <span data-ttu-id="38dfc-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="38dfc-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="38dfc-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38dfc-147">NOTES</span></span>

## <span data-ttu-id="38dfc-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38dfc-148">RELATED LINKS</span></span>

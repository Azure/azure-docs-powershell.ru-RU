---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214569"
---
# <span data-ttu-id="c4178-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c4178-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="c4178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4178-102">SYNOPSIS</span></span>
<span data-ttu-id="c4178-103">Обновите обогащение сообщений в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="c4178-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="c4178-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4178-104">SYNTAX</span></span>

### <span data-ttu-id="c4178-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4178-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4178-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c4178-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4178-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c4178-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4178-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4178-108">DESCRIPTION</span></span>
<span data-ttu-id="c4178-109">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c4178-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="c4178-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4178-110">EXAMPLES</span></span>

### <span data-ttu-id="c4178-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4178-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="c4178-112">Обновляет значение обогащения на значение updatedValue для ключа "newKey".</span><span class="sxs-lookup"><span data-stu-id="c4178-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="c4178-113">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c4178-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="c4178-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c4178-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="c4178-115">Обновляет конечную точку обогащения на "конечная точка1, конечная точка2, конечная точка3" для ключа "newKey".</span><span class="sxs-lookup"><span data-stu-id="c4178-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="c4178-116">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c4178-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="c4178-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4178-117">PARAMETERS</span></span>

### <span data-ttu-id="c4178-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4178-118">-DefaultProfile</span></span>
<span data-ttu-id="c4178-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4178-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4178-120">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="c4178-120">-Endpoint</span></span>
<span data-ttu-id="c4178-121">Конечные точки, к которые нужно применить обогащение.</span><span class="sxs-lookup"><span data-stu-id="c4178-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="c4178-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4178-122">-InputObject</span></span>
<span data-ttu-id="c4178-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="c4178-123">IotHub Object</span></span>

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

### <span data-ttu-id="c4178-124">-Key</span><span class="sxs-lookup"><span data-stu-id="c4178-124">-Key</span></span>
<span data-ttu-id="c4178-125">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="c4178-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="c4178-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c4178-126">-Name</span></span>
<span data-ttu-id="c4178-127">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="c4178-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c4178-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4178-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4178-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4178-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c4178-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4178-130">-ResourceId</span></span>
<span data-ttu-id="c4178-131">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="c4178-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c4178-132">-Значение</span><span class="sxs-lookup"><span data-stu-id="c4178-132">-Value</span></span>
<span data-ttu-id="c4178-133">Стоимость обогащения.</span><span class="sxs-lookup"><span data-stu-id="c4178-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="c4178-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4178-134">-Confirm</span></span>
<span data-ttu-id="c4178-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c4178-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4178-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4178-136">-WhatIf</span></span>
<span data-ttu-id="c4178-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4178-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4178-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4178-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4178-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4178-139">CommonParameters</span></span>
<span data-ttu-id="c4178-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4178-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4178-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4178-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4178-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4178-142">INPUTS</span></span>

### <span data-ttu-id="c4178-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c4178-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c4178-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c4178-144">System.String</span></span>

## <span data-ttu-id="c4178-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4178-145">OUTPUTS</span></span>

### <span data-ttu-id="c4178-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c4178-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="c4178-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4178-147">NOTES</span></span>

## <span data-ttu-id="c4178-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4178-148">RELATED LINKS</span></span>

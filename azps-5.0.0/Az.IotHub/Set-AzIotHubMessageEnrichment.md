---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250247"
---
# <span data-ttu-id="f44e7-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f44e7-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="f44e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f44e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f44e7-103">Обновите обогащение сообщений в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f44e7-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="f44e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f44e7-104">SYNTAX</span></span>

### <span data-ttu-id="f44e7-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f44e7-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f44e7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f44e7-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f44e7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f44e7-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f44e7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f44e7-108">DESCRIPTION</span></span>
<span data-ttu-id="f44e7-109">Подробное описание обогащения сообщений в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f44e7-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f44e7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f44e7-110">EXAMPLES</span></span>

### <span data-ttu-id="f44e7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f44e7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="f44e7-112">Обновляет значение обогащения на "updatedValue" для ключа "newKey".</span><span class="sxs-lookup"><span data-stu-id="f44e7-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="f44e7-113">Подробное описание обогащения сообщений в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f44e7-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="f44e7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f44e7-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="f44e7-115">Обновляет конечную точку обогащения на "endpoint1, Endpoint2, endpoint3" для ключа "newKey".</span><span class="sxs-lookup"><span data-stu-id="f44e7-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="f44e7-116">Подробное описание обогащения сообщений в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f44e7-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f44e7-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f44e7-117">PARAMETERS</span></span>

### <span data-ttu-id="f44e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44e7-118">-DefaultProfile</span></span>
<span data-ttu-id="f44e7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f44e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f44e7-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="f44e7-120">-Endpoint</span></span>
<span data-ttu-id="f44e7-121">Конечные точки, к которым нужно применить обогащенные элементы.</span><span class="sxs-lookup"><span data-stu-id="f44e7-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="f44e7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f44e7-122">-InputObject</span></span>
<span data-ttu-id="f44e7-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="f44e7-123">IotHub Object</span></span>

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

### <span data-ttu-id="f44e7-124">Клавиша</span><span class="sxs-lookup"><span data-stu-id="f44e7-124">-Key</span></span>
<span data-ttu-id="f44e7-125">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="f44e7-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="f44e7-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f44e7-126">-Name</span></span>
<span data-ttu-id="f44e7-127">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f44e7-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f44e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f44e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="f44e7-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f44e7-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f44e7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f44e7-130">-ResourceId</span></span>
<span data-ttu-id="f44e7-131">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="f44e7-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f44e7-132">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="f44e7-132">-Value</span></span>
<span data-ttu-id="f44e7-133">Значение обогащения.</span><span class="sxs-lookup"><span data-stu-id="f44e7-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="f44e7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f44e7-134">-Confirm</span></span>
<span data-ttu-id="f44e7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f44e7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f44e7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f44e7-136">-WhatIf</span></span>
<span data-ttu-id="f44e7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f44e7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f44e7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f44e7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f44e7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44e7-139">CommonParameters</span></span>
<span data-ttu-id="f44e7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f44e7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44e7-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44e7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44e7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f44e7-142">INPUTS</span></span>

### <span data-ttu-id="f44e7-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f44e7-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f44e7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f44e7-144">System.String</span></span>

## <span data-ttu-id="f44e7-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f44e7-145">OUTPUTS</span></span>

### <span data-ttu-id="f44e7-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f44e7-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="f44e7-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f44e7-147">NOTES</span></span>

## <span data-ttu-id="f44e7-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f44e7-148">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247776"
---
# <span data-ttu-id="7a784-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7a784-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="7a784-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a784-102">SYNOPSIS</span></span>
<span data-ttu-id="7a784-103">Создание обогащения сообщений для выбранных конечных точек в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7a784-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="7a784-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a784-104">SYNTAX</span></span>

### <span data-ttu-id="7a784-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a784-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a784-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a784-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a784-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7a784-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a784-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a784-108">DESCRIPTION</span></span>
<span data-ttu-id="7a784-109">Добавляйте до 10 обогащенных сообщений на центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7a784-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="7a784-110">Они добавляются в виде свойств приложения для сообщений, отправляемых в выбранные конечные точки.</span><span class="sxs-lookup"><span data-stu-id="7a784-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="7a784-111">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="7a784-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="7a784-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a784-112">EXAMPLES</span></span>

### <span data-ttu-id="7a784-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a784-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="7a784-114">Добавьте новое обогащение с помощью клавиши "newKey" и значения "newValue".</span><span class="sxs-lookup"><span data-stu-id="7a784-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="7a784-115">Это новое обогащение применяется к конечным точкам "endpoint1" и "Endpoint2".</span><span class="sxs-lookup"><span data-stu-id="7a784-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="7a784-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a784-116">PARAMETERS</span></span>

### <span data-ttu-id="7a784-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a784-117">-DefaultProfile</span></span>
<span data-ttu-id="7a784-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a784-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a784-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="7a784-119">-Endpoint</span></span>
<span data-ttu-id="7a784-120">Конечные точки, к которым нужно применить обогащенные элементы.</span><span class="sxs-lookup"><span data-stu-id="7a784-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a784-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a784-121">-InputObject</span></span>
<span data-ttu-id="7a784-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="7a784-122">IotHub object</span></span>

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

### <span data-ttu-id="7a784-123">Клавиша</span><span class="sxs-lookup"><span data-stu-id="7a784-123">-Key</span></span>
<span data-ttu-id="7a784-124">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="7a784-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="7a784-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a784-125">-Name</span></span>
<span data-ttu-id="7a784-126">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="7a784-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7a784-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a784-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a784-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7a784-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7a784-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a784-129">-ResourceId</span></span>
<span data-ttu-id="7a784-130">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="7a784-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7a784-131">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="7a784-131">-Value</span></span>
<span data-ttu-id="7a784-132">Значение обогащения.</span><span class="sxs-lookup"><span data-stu-id="7a784-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="7a784-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a784-133">-Confirm</span></span>
<span data-ttu-id="7a784-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a784-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a784-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a784-135">-WhatIf</span></span>
<span data-ttu-id="7a784-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a784-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a784-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a784-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a784-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a784-138">CommonParameters</span></span>
<span data-ttu-id="7a784-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a784-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a784-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a784-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a784-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a784-141">INPUTS</span></span>

### <span data-ttu-id="7a784-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7a784-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7a784-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7a784-143">System.String</span></span>

## <span data-ttu-id="7a784-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a784-144">OUTPUTS</span></span>

### <span data-ttu-id="7a784-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="7a784-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="7a784-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a784-146">NOTES</span></span>

## <span data-ttu-id="7a784-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a784-147">RELATED LINKS</span></span>
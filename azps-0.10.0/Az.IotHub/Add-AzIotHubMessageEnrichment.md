---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: caae747f7accd76db1424d14274416f0de97122d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911213"
---
# <span data-ttu-id="b6f65-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b6f65-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="b6f65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6f65-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f65-103">Создание обогащения сообщений для выбранных конечных точек в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="b6f65-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="b6f65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6f65-104">SYNTAX</span></span>

### <span data-ttu-id="b6f65-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6f65-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f65-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6f65-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f65-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b6f65-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f65-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6f65-108">DESCRIPTION</span></span>
<span data-ttu-id="b6f65-109">Добавляйте до 10 обогащенных сообщений на центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="b6f65-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="b6f65-110">Они добавляются в виде свойств приложения для сообщений, отправляемых в выбранные конечные точки.</span><span class="sxs-lookup"><span data-stu-id="b6f65-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="b6f65-111">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="b6f65-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="b6f65-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6f65-112">EXAMPLES</span></span>

### <span data-ttu-id="b6f65-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6f65-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="b6f65-114">Добавьте новое обогащение с помощью клавиши "newKey" и значения "newValue".</span><span class="sxs-lookup"><span data-stu-id="b6f65-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="b6f65-115">Это новое обогащение применяется к конечным точкам "endpoint1" и "Endpoint2".</span><span class="sxs-lookup"><span data-stu-id="b6f65-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="b6f65-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6f65-116">PARAMETERS</span></span>

### <span data-ttu-id="b6f65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f65-117">-DefaultProfile</span></span>
<span data-ttu-id="b6f65-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f65-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="b6f65-119">-Endpoint</span></span>
<span data-ttu-id="b6f65-120">Конечные точки, к которым нужно применить обогащенные элементы.</span><span class="sxs-lookup"><span data-stu-id="b6f65-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="b6f65-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6f65-121">-InputObject</span></span>
<span data-ttu-id="b6f65-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="b6f65-122">IotHub object</span></span>

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

### <span data-ttu-id="b6f65-123">Клавиша</span><span class="sxs-lookup"><span data-stu-id="b6f65-123">-Key</span></span>
<span data-ttu-id="b6f65-124">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="b6f65-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="b6f65-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6f65-125">-Name</span></span>
<span data-ttu-id="b6f65-126">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b6f65-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b6f65-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f65-127">-ResourceGroupName</span></span>
<span data-ttu-id="b6f65-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b6f65-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b6f65-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6f65-129">-ResourceId</span></span>
<span data-ttu-id="b6f65-130">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="b6f65-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b6f65-131">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="b6f65-131">-Value</span></span>
<span data-ttu-id="b6f65-132">Значение обогащения.</span><span class="sxs-lookup"><span data-stu-id="b6f65-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="b6f65-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6f65-133">-Confirm</span></span>
<span data-ttu-id="b6f65-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6f65-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f65-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f65-135">-WhatIf</span></span>
<span data-ttu-id="b6f65-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6f65-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f65-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6f65-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f65-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f65-138">CommonParameters</span></span>
<span data-ttu-id="b6f65-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6f65-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f65-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f65-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f65-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6f65-141">INPUTS</span></span>

### <span data-ttu-id="b6f65-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b6f65-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b6f65-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b6f65-143">System.String</span></span>

## <span data-ttu-id="b6f65-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6f65-144">OUTPUTS</span></span>

### <span data-ttu-id="b6f65-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="b6f65-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="b6f65-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6f65-146">NOTES</span></span>

## <span data-ttu-id="b6f65-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6f65-147">RELATED LINKS</span></span>

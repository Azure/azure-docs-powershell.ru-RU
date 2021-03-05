---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 2e024d3b82b6e553aa40bd6e570a848645538e11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997842"
---
# <span data-ttu-id="9ec2b-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9ec2b-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="9ec2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ec2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec2b-103">Обогащение сообщений для выбранных конечных точек в вашем центре IoT.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="9ec2b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ec2b-104">SYNTAX</span></span>

### <span data-ttu-id="9ec2b-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ec2b-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec2b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ec2b-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec2b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ec2b-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec2b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ec2b-108">DESCRIPTION</span></span>
<span data-ttu-id="9ec2b-109">До 10 обогащения сообщений на концентраторе IoT.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="9ec2b-110">Они добавляются в качестве свойств приложения к сообщениям, от отправленным на выбранные конечные точки.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="9ec2b-111">Чтобы узнать больше, см. https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="9ec2b-111">To know more, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="9ec2b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ec2b-112">EXAMPLES</span></span>

### <span data-ttu-id="9ec2b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ec2b-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="9ec2b-114">Добавление нового обогащения ключом "newKey" и значением "newValue".</span><span class="sxs-lookup"><span data-stu-id="9ec2b-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="9ec2b-115">Это новое обогащение применяется к конечным точкам "1" и "конечная точка2".</span><span class="sxs-lookup"><span data-stu-id="9ec2b-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="9ec2b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ec2b-116">PARAMETERS</span></span>

### <span data-ttu-id="9ec2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec2b-117">-DefaultProfile</span></span>
<span data-ttu-id="9ec2b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ec2b-119">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="9ec2b-119">-Endpoint</span></span>
<span data-ttu-id="9ec2b-120">Конечные точки, к которые нужно применить обогащение.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="9ec2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ec2b-121">-InputObject</span></span>
<span data-ttu-id="9ec2b-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="9ec2b-122">IotHub object</span></span>

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

### <span data-ttu-id="9ec2b-123">-Key</span><span class="sxs-lookup"><span data-stu-id="9ec2b-123">-Key</span></span>
<span data-ttu-id="9ec2b-124">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="9ec2b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9ec2b-125">-Name</span></span>
<span data-ttu-id="9ec2b-126">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="9ec2b-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9ec2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ec2b-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ec2b-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ec2b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ec2b-129">-ResourceId</span></span>
<span data-ttu-id="9ec2b-130">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="9ec2b-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9ec2b-131">-Значение</span><span class="sxs-lookup"><span data-stu-id="9ec2b-131">-Value</span></span>
<span data-ttu-id="9ec2b-132">Стоимость обогащения.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="9ec2b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ec2b-133">-Confirm</span></span>
<span data-ttu-id="9ec2b-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec2b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec2b-135">-WhatIf</span></span>
<span data-ttu-id="9ec2b-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec2b-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec2b-138">CommonParameters</span></span>
<span data-ttu-id="9ec2b-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec2b-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ec2b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec2b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ec2b-141">INPUTS</span></span>

### <span data-ttu-id="9ec2b-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9ec2b-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9ec2b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9ec2b-143">System.String</span></span>

## <span data-ttu-id="9ec2b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ec2b-144">OUTPUTS</span></span>

### <span data-ttu-id="9ec2b-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9ec2b-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="9ec2b-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ec2b-146">NOTES</span></span>

## <span data-ttu-id="9ec2b-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ec2b-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312452"
---
# <span data-ttu-id="8232f-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8232f-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="8232f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8232f-102">SYNOPSIS</span></span>
<span data-ttu-id="8232f-103">Удаление обогащения сообщений в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="8232f-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="8232f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8232f-104">SYNTAX</span></span>

### <span data-ttu-id="8232f-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8232f-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8232f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8232f-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8232f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8232f-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8232f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8232f-108">DESCRIPTION</span></span>
<span data-ttu-id="8232f-109">Подробное описание обогащения сообщений в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="8232f-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="8232f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8232f-110">EXAMPLES</span></span>

### <span data-ttu-id="8232f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8232f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="8232f-112">Удаляет обогащение сообщений "newKey".</span><span class="sxs-lookup"><span data-stu-id="8232f-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="8232f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8232f-113">PARAMETERS</span></span>

### <span data-ttu-id="8232f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8232f-114">-DefaultProfile</span></span>
<span data-ttu-id="8232f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8232f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8232f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8232f-116">-InputObject</span></span>
<span data-ttu-id="8232f-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="8232f-117">IotHub object</span></span>

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

### <span data-ttu-id="8232f-118">Клавиша</span><span class="sxs-lookup"><span data-stu-id="8232f-118">-Key</span></span>
<span data-ttu-id="8232f-119">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="8232f-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="8232f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8232f-120">-Name</span></span>
<span data-ttu-id="8232f-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="8232f-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8232f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8232f-122">-PassThru</span></span>
<span data-ttu-id="8232f-123">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="8232f-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="8232f-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8232f-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8232f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8232f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8232f-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8232f-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8232f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8232f-127">-ResourceId</span></span>
<span data-ttu-id="8232f-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="8232f-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8232f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8232f-129">-Confirm</span></span>
<span data-ttu-id="8232f-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8232f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8232f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8232f-131">-WhatIf</span></span>
<span data-ttu-id="8232f-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8232f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8232f-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8232f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8232f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8232f-134">CommonParameters</span></span>
<span data-ttu-id="8232f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8232f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8232f-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8232f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8232f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8232f-137">INPUTS</span></span>

### <span data-ttu-id="8232f-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8232f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8232f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8232f-139">System.String</span></span>

## <span data-ttu-id="8232f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8232f-140">OUTPUTS</span></span>

### <span data-ttu-id="8232f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8232f-141">System.Boolean</span></span>

## <span data-ttu-id="8232f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8232f-142">NOTES</span></span>

## <span data-ttu-id="8232f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8232f-143">RELATED LINKS</span></span>

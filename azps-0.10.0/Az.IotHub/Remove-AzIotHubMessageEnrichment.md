---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 5c30db1845fe135aad9ebb575a6b31f19e9598b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910327"
---
# <span data-ttu-id="33a91-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="33a91-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="33a91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33a91-102">SYNOPSIS</span></span>
<span data-ttu-id="33a91-103">Удаление обогащения сообщений в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="33a91-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="33a91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33a91-104">SYNTAX</span></span>

### <span data-ttu-id="33a91-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33a91-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a91-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="33a91-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a91-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33a91-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a91-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33a91-108">DESCRIPTION</span></span>
<span data-ttu-id="33a91-109">Подробное описание обогащения сообщений в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="33a91-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="33a91-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33a91-110">EXAMPLES</span></span>

### <span data-ttu-id="33a91-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33a91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="33a91-112">Удаляет обогащение сообщений "newKey".</span><span class="sxs-lookup"><span data-stu-id="33a91-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="33a91-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33a91-113">PARAMETERS</span></span>

### <span data-ttu-id="33a91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a91-114">-DefaultProfile</span></span>
<span data-ttu-id="33a91-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33a91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a91-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33a91-116">-InputObject</span></span>
<span data-ttu-id="33a91-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="33a91-117">IotHub object</span></span>

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

### <span data-ttu-id="33a91-118">Клавиша</span><span class="sxs-lookup"><span data-stu-id="33a91-118">-Key</span></span>
<span data-ttu-id="33a91-119">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="33a91-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="33a91-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33a91-120">-Name</span></span>
<span data-ttu-id="33a91-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="33a91-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="33a91-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33a91-122">-PassThru</span></span>
<span data-ttu-id="33a91-123">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="33a91-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="33a91-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="33a91-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33a91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a91-125">-ResourceGroupName</span></span>
<span data-ttu-id="33a91-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="33a91-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="33a91-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33a91-127">-ResourceId</span></span>
<span data-ttu-id="33a91-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="33a91-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="33a91-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33a91-129">-Confirm</span></span>
<span data-ttu-id="33a91-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="33a91-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a91-131">-WhatIf</span></span>
<span data-ttu-id="33a91-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="33a91-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a91-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="33a91-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a91-134">CommonParameters</span></span>
<span data-ttu-id="33a91-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33a91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a91-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a91-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a91-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33a91-137">INPUTS</span></span>

### <span data-ttu-id="33a91-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="33a91-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="33a91-139">System. String</span><span class="sxs-lookup"><span data-stu-id="33a91-139">System.String</span></span>

## <span data-ttu-id="33a91-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33a91-140">OUTPUTS</span></span>

### <span data-ttu-id="33a91-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33a91-141">System.Boolean</span></span>

## <span data-ttu-id="33a91-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="33a91-142">NOTES</span></span>

## <span data-ttu-id="33a91-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33a91-143">RELATED LINKS</span></span>

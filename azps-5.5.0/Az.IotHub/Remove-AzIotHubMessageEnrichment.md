---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226484"
---
# <span data-ttu-id="56ae6-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="56ae6-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="56ae6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="56ae6-103">Удалите обогащение сообщений в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="56ae6-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="56ae6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56ae6-104">SYNTAX</span></span>

### <span data-ttu-id="56ae6-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56ae6-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56ae6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="56ae6-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56ae6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="56ae6-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56ae6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56ae6-108">DESCRIPTION</span></span>
<span data-ttu-id="56ae6-109">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="56ae6-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="56ae6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56ae6-110">EXAMPLES</span></span>

### <span data-ttu-id="56ae6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56ae6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="56ae6-112">Удаляет обогащение сообщений newKey.</span><span class="sxs-lookup"><span data-stu-id="56ae6-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="56ae6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56ae6-113">PARAMETERS</span></span>

### <span data-ttu-id="56ae6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ae6-114">-DefaultProfile</span></span>
<span data-ttu-id="56ae6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56ae6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ae6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56ae6-116">-InputObject</span></span>
<span data-ttu-id="56ae6-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="56ae6-117">IotHub object</span></span>

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

### <span data-ttu-id="56ae6-118">-Key</span><span class="sxs-lookup"><span data-stu-id="56ae6-118">-Key</span></span>
<span data-ttu-id="56ae6-119">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="56ae6-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="56ae6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="56ae6-120">-Name</span></span>
<span data-ttu-id="56ae6-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="56ae6-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="56ae6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56ae6-122">-PassThru</span></span>
<span data-ttu-id="56ae6-123">Возвращает объект boolean.</span><span class="sxs-lookup"><span data-stu-id="56ae6-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="56ae6-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="56ae6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="56ae6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ae6-125">-ResourceGroupName</span></span>
<span data-ttu-id="56ae6-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="56ae6-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="56ae6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56ae6-127">-ResourceId</span></span>
<span data-ttu-id="56ae6-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="56ae6-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="56ae6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56ae6-129">-Confirm</span></span>
<span data-ttu-id="56ae6-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56ae6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ae6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ae6-131">-WhatIf</span></span>
<span data-ttu-id="56ae6-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56ae6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ae6-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56ae6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ae6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ae6-134">CommonParameters</span></span>
<span data-ttu-id="56ae6-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ae6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ae6-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ae6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ae6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56ae6-137">INPUTS</span></span>

### <span data-ttu-id="56ae6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="56ae6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="56ae6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="56ae6-139">System.String</span></span>

## <span data-ttu-id="56ae6-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56ae6-140">OUTPUTS</span></span>

### <span data-ttu-id="56ae6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56ae6-141">System.Boolean</span></span>

## <span data-ttu-id="56ae6-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56ae6-142">NOTES</span></span>

## <span data-ttu-id="56ae6-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56ae6-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518441"
---
# <span data-ttu-id="f815d-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f815d-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="f815d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f815d-102">SYNOPSIS</span></span>
<span data-ttu-id="f815d-103">Здесь перечислены все обогащения сообщений или определенное обогащение сообщений для вашего концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="f815d-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="f815d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f815d-104">SYNTAX</span></span>

### <span data-ttu-id="f815d-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f815d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f815d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f815d-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f815d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f815d-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f815d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f815d-108">DESCRIPTION</span></span>
<span data-ttu-id="f815d-109">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f815d-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f815d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f815d-110">EXAMPLES</span></span>

### <span data-ttu-id="f815d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f815d-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="f815d-112">Список всех обогащений сообщений в MyIotHub</span><span class="sxs-lookup"><span data-stu-id="f815d-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="f815d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f815d-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="f815d-114">Показать сведения о обогащении сообщений newKey.</span><span class="sxs-lookup"><span data-stu-id="f815d-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="f815d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f815d-115">PARAMETERS</span></span>

### <span data-ttu-id="f815d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f815d-116">-DefaultProfile</span></span>
<span data-ttu-id="f815d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f815d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f815d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f815d-118">-InputObject</span></span>
<span data-ttu-id="f815d-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="f815d-119">IotHub object</span></span>

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

### <span data-ttu-id="f815d-120">-Key</span><span class="sxs-lookup"><span data-stu-id="f815d-120">-Key</span></span>
<span data-ttu-id="f815d-121">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="f815d-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="f815d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f815d-122">-Name</span></span>
<span data-ttu-id="f815d-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="f815d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f815d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f815d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f815d-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f815d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f815d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f815d-126">-ResourceId</span></span>
<span data-ttu-id="f815d-127">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="f815d-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f815d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f815d-128">CommonParameters</span></span>
<span data-ttu-id="f815d-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f815d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f815d-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f815d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f815d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f815d-131">INPUTS</span></span>

### <span data-ttu-id="f815d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f815d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f815d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f815d-133">System.String</span></span>

## <span data-ttu-id="f815d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f815d-134">OUTPUTS</span></span>

### <span data-ttu-id="f815d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f815d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="f815d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="f815d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="f815d-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f815d-137">NOTES</span></span>

## <span data-ttu-id="f815d-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f815d-138">RELATED LINKS</span></span>

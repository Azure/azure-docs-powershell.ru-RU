---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94258013"
---
# <span data-ttu-id="31011-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="31011-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="31011-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31011-102">SYNOPSIS</span></span>
<span data-ttu-id="31011-103">В этой статье перечислены все обогащения сообщений или определено обогащение сообщений для центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="31011-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="31011-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31011-104">SYNTAX</span></span>

### <span data-ttu-id="31011-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31011-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31011-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31011-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31011-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31011-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31011-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31011-108">DESCRIPTION</span></span>
<span data-ttu-id="31011-109">Подробное описание обогащения сообщений в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="31011-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="31011-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31011-110">EXAMPLES</span></span>

### <span data-ttu-id="31011-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31011-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="31011-112">Список всех обогащений сообщений в MyIotHub</span><span class="sxs-lookup"><span data-stu-id="31011-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="31011-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="31011-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="31011-114">Показать подробные сведения о обогащении сообщений "newKey".</span><span class="sxs-lookup"><span data-stu-id="31011-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="31011-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31011-115">PARAMETERS</span></span>

### <span data-ttu-id="31011-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31011-116">-DefaultProfile</span></span>
<span data-ttu-id="31011-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31011-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31011-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31011-118">-InputObject</span></span>
<span data-ttu-id="31011-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="31011-119">IotHub object</span></span>

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

### <span data-ttu-id="31011-120">Клавиша</span><span class="sxs-lookup"><span data-stu-id="31011-120">-Key</span></span>
<span data-ttu-id="31011-121">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="31011-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="31011-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31011-122">-Name</span></span>
<span data-ttu-id="31011-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="31011-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="31011-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31011-124">-ResourceGroupName</span></span>
<span data-ttu-id="31011-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="31011-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="31011-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31011-126">-ResourceId</span></span>
<span data-ttu-id="31011-127">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="31011-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="31011-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31011-128">CommonParameters</span></span>
<span data-ttu-id="31011-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31011-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31011-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31011-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31011-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31011-131">INPUTS</span></span>

### <span data-ttu-id="31011-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="31011-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="31011-133">System. String</span><span class="sxs-lookup"><span data-stu-id="31011-133">System.String</span></span>

## <span data-ttu-id="31011-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31011-134">OUTPUTS</span></span>

### <span data-ttu-id="31011-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="31011-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="31011-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="31011-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="31011-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="31011-137">NOTES</span></span>

## <span data-ttu-id="31011-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31011-138">RELATED LINKS</span></span>

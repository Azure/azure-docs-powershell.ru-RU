---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569563"
---
# <span data-ttu-id="24bc5-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="24bc5-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="24bc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="24bc5-103">Возвращает клавиши для среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="24bc5-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24bc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24bc5-104">SYNTAX</span></span>

### <span data-ttu-id="24bc5-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24bc5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="24bc5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24bc5-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="24bc5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="24bc5-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="24bc5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24bc5-108">DESCRIPTION</span></span>
<span data-ttu-id="24bc5-109">Получение ключей для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="24bc5-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="24bc5-110">Ключи используются для регистрации узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="24bc5-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="24bc5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24bc5-111">EXAMPLES</span></span>

### <span data-ttu-id="24bc5-112">Пример 1: получение ключей среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="24bc5-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="24bc5-113">Командлет извлекает ключи для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="24bc5-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="24bc5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24bc5-114">PARAMETERS</span></span>

### <span data-ttu-id="24bc5-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24bc5-115">-DataFactoryName</span></span>
<span data-ttu-id="24bc5-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="24bc5-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bc5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24bc5-117">-InputObject</span></span>
<span data-ttu-id="24bc5-118">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="24bc5-118">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24bc5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24bc5-119">-Name</span></span>
<span data-ttu-id="24bc5-120">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="24bc5-120">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bc5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24bc5-121">-ResourceGroupName</span></span>
<span data-ttu-id="24bc5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24bc5-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bc5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24bc5-123">-ResourceId</span></span>
<span data-ttu-id="24bc5-124">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="24bc5-124">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="24bc5-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24bc5-125">INPUTS</span></span>

### <span data-ttu-id="24bc5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="24bc5-126">System.String</span></span>
<span data-ttu-id="24bc5-127">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="24bc5-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="24bc5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24bc5-128">OUTPUTS</span></span>

### <span data-ttu-id="24bc5-129">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="24bc5-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="24bc5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="24bc5-130">NOTES</span></span>

## <span data-ttu-id="24bc5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24bc5-131">RELATED LINKS</span></span>
[<span data-ttu-id="24bc5-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="24bc5-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()

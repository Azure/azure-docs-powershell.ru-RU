---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: eb248e1059da6dcab581e4fba8b3eac7f970bb30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565516"
---
# <span data-ttu-id="9ca5e-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="9ca5e-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="9ca5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ca5e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca5e-103">Возвращает клавиши для среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ca5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ca5e-104">SYNTAX</span></span>

### <span data-ttu-id="9ca5e-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ca5e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca5e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca5e-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca5e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9ca5e-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ca5e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ca5e-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca5e-109">Получение ключей для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="9ca5e-110">Ключи используются для регистрации узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="9ca5e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ca5e-111">EXAMPLES</span></span>

### <span data-ttu-id="9ca5e-112">Пример 1: получение ключей среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="9ca5e-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="9ca5e-113">Командлет извлекает ключи для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9ca5e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ca5e-114">PARAMETERS</span></span>

### <span data-ttu-id="9ca5e-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9ca5e-115">-DataFactoryName</span></span>
<span data-ttu-id="9ca5e-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-116">The data factory name.</span></span>

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

### <span data-ttu-id="9ca5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca5e-117">-DefaultProfile</span></span>
<span data-ttu-id="9ca5e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca5e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca5e-119">-InputObject</span></span>
<span data-ttu-id="9ca5e-120">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="9ca5e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ca5e-121">-Name</span></span>
<span data-ttu-id="9ca5e-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="9ca5e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca5e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ca5e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-124">The resource group name.</span></span>

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

### <span data-ttu-id="9ca5e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca5e-125">-ResourceId</span></span>
<span data-ttu-id="9ca5e-126">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9ca5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca5e-127">CommonParameters</span></span>
<span data-ttu-id="9ca5e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ca5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca5e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ca5e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca5e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ca5e-130">INPUTS</span></span>

### <span data-ttu-id="9ca5e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9ca5e-131">System.String</span></span>
<span data-ttu-id="9ca5e-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9ca5e-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="9ca5e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ca5e-133">OUTPUTS</span></span>

### <span data-ttu-id="9ca5e-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="9ca5e-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="9ca5e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ca5e-135">NOTES</span></span>

## <span data-ttu-id="9ca5e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ca5e-136">RELATED LINKS</span></span>

[<span data-ttu-id="9ca5e-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="9ca5e-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()

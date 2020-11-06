---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568325"
---
# <span data-ttu-id="ffcee-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ffcee-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="ffcee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffcee-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcee-103">Возвращает клавиши для среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="ffcee-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffcee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffcee-104">SYNTAX</span></span>

### <span data-ttu-id="ffcee-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffcee-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffcee-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ffcee-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffcee-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ffcee-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffcee-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffcee-108">DESCRIPTION</span></span>
<span data-ttu-id="ffcee-109">Получение ключей для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ffcee-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="ffcee-110">Ключи используются для регистрации узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ffcee-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="ffcee-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffcee-111">EXAMPLES</span></span>

### <span data-ttu-id="ffcee-112">Пример 1: получение ключей среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="ffcee-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="ffcee-113">Командлет извлекает ключи для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="ffcee-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ffcee-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffcee-114">PARAMETERS</span></span>

### <span data-ttu-id="ffcee-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ffcee-115">-DataFactoryName</span></span>
<span data-ttu-id="ffcee-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ffcee-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcee-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffcee-117">-InputObject</span></span>
<span data-ttu-id="ffcee-118">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="ffcee-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcee-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ffcee-119">-Name</span></span>
<span data-ttu-id="ffcee-120">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ffcee-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffcee-121">-ResourceGroupName</span></span>
<span data-ttu-id="ffcee-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffcee-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcee-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffcee-123">-ResourceId</span></span>
<span data-ttu-id="ffcee-124">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="ffcee-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcee-125">-DefaultProfile</span></span>
<span data-ttu-id="ffcee-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffcee-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcee-127">CommonParameters</span></span>
<span data-ttu-id="ffcee-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffcee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcee-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffcee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcee-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffcee-130">INPUTS</span></span>

### <span data-ttu-id="ffcee-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ffcee-131">System.String</span></span>
<span data-ttu-id="ffcee-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ffcee-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="ffcee-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffcee-133">OUTPUTS</span></span>

### <span data-ttu-id="ffcee-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="ffcee-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="ffcee-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffcee-135">NOTES</span></span>

## <span data-ttu-id="ffcee-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffcee-136">RELATED LINKS</span></span>

[<span data-ttu-id="ffcee-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ffcee-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()

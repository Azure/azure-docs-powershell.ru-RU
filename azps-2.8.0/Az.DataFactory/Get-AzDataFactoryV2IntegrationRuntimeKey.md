---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2a1aaef2532e8c0a00a04a42d857e2be0e2a0451
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721526"
---
# <span data-ttu-id="cfa20-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cfa20-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="cfa20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfa20-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa20-103">Возвращает клавиши для среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="cfa20-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="cfa20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfa20-104">SYNTAX</span></span>

### <span data-ttu-id="cfa20-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cfa20-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa20-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa20-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfa20-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cfa20-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa20-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfa20-108">DESCRIPTION</span></span>
<span data-ttu-id="cfa20-109">Получение ключей для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cfa20-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="cfa20-110">Ключи используются для регистрации узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cfa20-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="cfa20-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfa20-111">EXAMPLES</span></span>

### <span data-ttu-id="cfa20-112">Пример 1: получение ключей среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="cfa20-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="cfa20-113">Командлет извлекает ключи для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="cfa20-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cfa20-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfa20-114">PARAMETERS</span></span>

### <span data-ttu-id="cfa20-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cfa20-115">-DataFactoryName</span></span>
<span data-ttu-id="cfa20-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="cfa20-116">The data factory name.</span></span>

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

### <span data-ttu-id="cfa20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa20-117">-DefaultProfile</span></span>
<span data-ttu-id="cfa20-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa20-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa20-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfa20-119">-InputObject</span></span>
<span data-ttu-id="cfa20-120">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="cfa20-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="cfa20-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cfa20-121">-Name</span></span>
<span data-ttu-id="cfa20-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cfa20-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="cfa20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa20-123">-ResourceGroupName</span></span>
<span data-ttu-id="cfa20-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfa20-124">The resource group name.</span></span>

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

### <span data-ttu-id="cfa20-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa20-125">-ResourceId</span></span>
<span data-ttu-id="cfa20-126">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa20-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cfa20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa20-127">CommonParameters</span></span>
<span data-ttu-id="cfa20-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfa20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa20-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa20-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa20-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfa20-130">INPUTS</span></span>

### <span data-ttu-id="cfa20-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cfa20-131">System.String</span></span>

### <span data-ttu-id="cfa20-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cfa20-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cfa20-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfa20-133">OUTPUTS</span></span>

### <span data-ttu-id="cfa20-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="cfa20-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="cfa20-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfa20-135">NOTES</span></span>

## <span data-ttu-id="cfa20-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfa20-136">RELATED LINKS</span></span>

[<span data-ttu-id="cfa20-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cfa20-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()

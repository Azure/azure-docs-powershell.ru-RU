---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 166bae99bebbc5a1b1c25ffc79faa3a1f7254bbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732226"
---
# <span data-ttu-id="1c7bc-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="1c7bc-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="1c7bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c7bc-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7bc-103">Повторное создание ключа среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c7bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c7bc-104">SYNTAX</span></span>

### <span data-ttu-id="1c7bc-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c7bc-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1c7bc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c7bc-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="1c7bc-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1c7bc-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1c7bc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c7bc-108">DESCRIPTION</span></span>
<span data-ttu-id="1c7bc-109">Командлет **New-AzureRmDataFactoryV2IntegrationRuntimeKey** повторно создает ключ среды выполнения Integration с именем ключа, заданным параметром keyName.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="1c7bc-110">Предыдущий ключ не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="1c7bc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c7bc-111">EXAMPLES</span></span>

### <span data-ttu-id="1c7bc-112">Пример 1: создание нового ключа для среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="1c7bc-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="1c7bc-113">Командлет повторно создает ключ "authKey2" для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="1c7bc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c7bc-114">PARAMETERS</span></span>

### <span data-ttu-id="1c7bc-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c7bc-115">-Confirm</span></span>
<span data-ttu-id="1c7bc-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7bc-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1c7bc-117">-DataFactoryName</span></span>
<span data-ttu-id="1c7bc-118">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-118">The data factory name.</span></span>

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

### <span data-ttu-id="1c7bc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1c7bc-119">-Force</span></span>
<span data-ttu-id="1c7bc-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7bc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c7bc-121">-InputObject</span></span>
<span data-ttu-id="1c7bc-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="1c7bc-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1c7bc-123">-KeyName</span></span>
<span data-ttu-id="1c7bc-124">Имя ключа проверки подлинности в среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7bc-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c7bc-125">-Name</span></span>
<span data-ttu-id="1c7bc-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="1c7bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c7bc-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-128">The resource group name.</span></span>

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

### <span data-ttu-id="1c7bc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c7bc-129">-ResourceId</span></span>
<span data-ttu-id="1c7bc-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1c7bc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c7bc-131">-WhatIf</span></span>
<span data-ttu-id="1c7bc-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="1c7bc-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1c7bc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c7bc-133">INPUTS</span></span>

### <span data-ttu-id="1c7bc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1c7bc-134">System.String</span></span>
<span data-ttu-id="1c7bc-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c7bc-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="1c7bc-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c7bc-136">OUTPUTS</span></span>

### <span data-ttu-id="1c7bc-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="1c7bc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="1c7bc-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c7bc-138">NOTES</span></span>

## <span data-ttu-id="1c7bc-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c7bc-139">RELATED LINKS</span></span>
[<span data-ttu-id="1c7bc-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="1c7bc-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()

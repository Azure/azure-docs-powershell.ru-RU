---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: bf29e12292fba12cc6a5b4f99cef1e13f9d9fd8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566278"
---
# <span data-ttu-id="219de-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="219de-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="219de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="219de-102">SYNOPSIS</span></span>
<span data-ttu-id="219de-103">Удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="219de-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="219de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="219de-104">SYNTAX</span></span>

### <span data-ttu-id="219de-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="219de-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="219de-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="219de-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219de-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="219de-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="219de-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="219de-108">DESCRIPTION</span></span>
<span data-ttu-id="219de-109">Командлет Remove-AzureRmDataFactoryV2IntegrationRuntime удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="219de-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="219de-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="219de-110">EXAMPLES</span></span>

### <span data-ttu-id="219de-111">Пример 1: Удаление среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="219de-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="219de-112">Эта команда удаляет среду выполнения интеграции с именем "тест-зарезервирован-IR" из фабрики данных с именем "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="219de-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="219de-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="219de-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="219de-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="219de-114">PARAMETERS</span></span>

### <span data-ttu-id="219de-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="219de-115">-DataFactoryName</span></span>
<span data-ttu-id="219de-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="219de-116">The data factory name.</span></span>

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

### <span data-ttu-id="219de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="219de-117">-Force</span></span>
<span data-ttu-id="219de-118">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="219de-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="219de-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="219de-119">-InputObject</span></span>
<span data-ttu-id="219de-120">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="219de-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="219de-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="219de-121">-Name</span></span>
<span data-ttu-id="219de-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="219de-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="219de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219de-123">-ResourceGroupName</span></span>
<span data-ttu-id="219de-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="219de-124">The resource group name.</span></span>

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

### <span data-ttu-id="219de-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="219de-125">-ResourceId</span></span>
<span data-ttu-id="219de-126">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="219de-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="219de-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="219de-127">-Confirm</span></span>
<span data-ttu-id="219de-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="219de-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219de-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219de-129">-WhatIf</span></span>
<span data-ttu-id="219de-130">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="219de-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="219de-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219de-131">-DefaultProfile</span></span>
<span data-ttu-id="219de-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="219de-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="219de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219de-133">CommonParameters</span></span>
<span data-ttu-id="219de-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="219de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219de-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219de-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219de-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="219de-136">INPUTS</span></span>

### <span data-ttu-id="219de-137">System. String</span><span class="sxs-lookup"><span data-stu-id="219de-137">System.String</span></span>
<span data-ttu-id="219de-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="219de-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="219de-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="219de-139">OUTPUTS</span></span>

### <span data-ttu-id="219de-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="219de-140">System.Object</span></span>

## <span data-ttu-id="219de-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="219de-141">NOTES</span></span>
<span data-ttu-id="219de-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="219de-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="219de-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="219de-143">RELATED LINKS</span></span>

[<span data-ttu-id="219de-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="219de-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="219de-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="219de-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

